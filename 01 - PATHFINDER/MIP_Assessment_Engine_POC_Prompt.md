# NCA Assessment Engine — Claude Code Scaffold Prompt

> **Instructions:** Paste everything below this line into Claude Code in the CIPP project.

---

## Task: Scaffold an AI Readiness Assessment Data Pipeline (POC)

### What You're Building
A data collection pipeline called the NCA Assessment Engine. It gathers M365 tenant health data from two sources — AvePoint Elements API and Microsoft Graph — and stores raw JSON responses in Azure SQL. This is the first phase of an AI readiness scoring tool.

**Today's scope:** API scaffolds only. Call each endpoint, store the raw JSON response, return a summary. No scoring logic, no transformations, no report generation yet.

---

### Step 1 — Discover Before You Build
Before writing any new code, read the existing project and answer:
1. What language/runtime are the existing Function App functions? (PowerShell, C#, JavaScript/TypeScript, Python?)
2. How does the existing code authenticate to Microsoft Graph for client tenants via GDAP? Find the token acquisition pattern and the Key Vault/secret access pattern — all new functions must follow these exactly.
3. What tables already exist in Azure SQL? What is the naming convention?
4. What is the existing folder/project structure for Function App functions?

Use these patterns throughout. Do not introduce new patterns for auth, secrets, or database access.

---

### New Database Tables
Add these if they don't already exist. Match the existing naming conventions if they differ.

```sql
CREATE TABLE nca_clients (
    id                   INT IDENTITY PRIMARY KEY,
    avepoint_customer_id NVARCHAR(100) NOT NULL,
    avepoint_tenant_id   NVARCHAR(100),
    m365_tenant_id       NVARCHAR(100),
    org_name             NVARCHAR(255) NOT NULL,
    owner_email          NVARCHAR(255),
    is_active            BIT DEFAULT 1,
    created_at           DATETIME2 DEFAULT GETUTCDATE(),
    updated_at           DATETIME2 DEFAULT GETUTCDATE()
);

CREATE TABLE nca_assessments (
    id              INT IDENTITY PRIMARY KEY,
    client_id       INT NOT NULL REFERENCES nca_clients(id),
    assessment_date DATE NOT NULL,
    status          NVARCHAR(50) DEFAULT 'in_progress',
    created_at      DATETIME2 DEFAULT GETUTCDATE()
);

CREATE TABLE nca_assessment_data (
    id            INT IDENTITY PRIMARY KEY,
    assessment_id INT NOT NULL REFERENCES nca_assessments(id),
    data_source   NVARCHAR(100) NOT NULL,
    raw_json      NVARCHAR(MAX),
    collected_at  DATETIME2 DEFAULT GETUTCDATE(),
    error_message NVARCHAR(MAX)
);
```

---

### Source 1: AvePoint Elements API

**Authentication — OAuth 2.0 Client Credentials:**
- Token URL: `https://identity.avepointonlineservices.com/connect/token`
- Method: POST, Content-Type: `application/x-www-form-urlencoded`
- Body: `client_id={value}&client_secret={value}&scope={value}&grant_type=client_credentials`
- Token TTL: 1 hour — cache it
- Secrets to add: `AVEPOINT_CLIENT_ID`, `AVEPOINT_CLIENT_SECRET` (use existing Key Vault / App Settings pattern)
- Base URL: `https://graph.avepointonlineservices.com`
- Request all scopes in one token (space-separated): `elements.customers.read.all elements.license.read.all elements.wm.read.all elements.rm.read.all`

**Endpoint 1 — Bootstrap: List All Customers**
```
POST /partner/external/v3/general/customers/batch
Body: {}
Scope: elements.customers.read.all
Returns: data[].id (customerId), data[].organization, data[].tenants[].id (tenantId), data[].tenants[].name
Purpose: Populates nca_clients. Upsert on avepoint_customer_id.
```

**Endpoint 2 — Workspace Overview**
```
GET /partner/external/v3/wm/customers/{customerId}/tenants/{tenantId}/overview/workspace
Scope: elements.wm.read.all
Returns: teams, sharePointSites, oneDrives, activeWorkspaces, inactiveWorkspaces,
         orphanedWorkspaces, orphanedTeams, orphanedSharePointSites,
         workspacesWithGuestUsers, teamsWithGuestUsers, sharePointSitesWithGuestUsers
Store as: data_source = 'avepoint_workspace_overview'
```

**Endpoint 3 — Workspace Compliance**
```
GET /partner/external/v3/wm/customers/{customerId}/tenants/{tenantId}/overview/data-protection/compliance-rate
Scope: elements.wm.read.all
Returns: workspacesInCompliance, workspacesOutOfCompliance
Store as: data_source = 'avepoint_compliance'
```

**Endpoint 4 — Data Security Posture (DSPM)**
```
GET /partner/external/v3/wm/customers/{customerId}/tenants/{tenantId}/overview/dspm/insights
Scope: elements.wm.read.all
Returns: sensitiveItemsSharedViaAnyoneLink, sensitiveItemsSharedViaOrganizationLink,
         sensitiveItemsSharedViaLinkForSpecificExternalUsers,
         sensitiveItemsSharedWithEveryone, sensitiveItemsSharedWithEveryoneExceptExternalUsers
Store as: data_source = 'avepoint_dspm'
```

**Endpoint 5 — Ransomware / Unusual Activity**
```
GET /partner/external/v3/wm/customers/{customerId}/tenants/{tenantId}/overview/data-protection/ransomware-detection
Scope: elements.wm.read.all
Returns: *UnderPotentialRansomwareAttack, *WithUnusualActivities, *WithSuspiciousObjects
         per workspace type (Teams, SharePoint, OneDrive, Groups) — last 7 days
Store as: data_source = 'avepoint_ransomware'
```

**Endpoint 6 — Risk Rules**
```
GET /partner/external/v3/rm/customers/{customerId}/tenants/{tenantId}/detection/rules?status=1
Scope: elements.rm.read.all
Returns: result[].ruleName, result[].dataSource (int: 3=Teams, 4=SharePoint, 5=OneDrive, 6=Users),
         result[].hitItemCount
Examples of rules: "Users without MFA enabled", "Global administrator without a password expiration date"
Store as: data_source = 'avepoint_risk_rules'
```

---

### Source 2: Microsoft Graph API (via existing GDAP pattern)

Use the same GDAP token acquisition the existing project already uses. Each call targets a specific client tenant using the `m365_tenant_id` from `nca_clients`. If `m365_tenant_id` is null for a client, skip Graph collection and return a message indicating it needs to be populated.

**Endpoint 1 — MFA Registration Status**
```
GET https://graph.microsoft.com/v1.0/reports/getCredentialUserRegistrationDetails
Returns: per-user MFA registration and method details
Store as: data_source = 'graph_mfa'
```

**Endpoint 2 — Conditional Access Policies**
```
GET https://graph.microsoft.com/v1.0/identity/conditionalAccess/policies
Returns: id, displayName, state (enabled/disabled/enabledForReportingButNotEnforced), conditions
Store as: data_source = 'graph_ca_policies'
```

**Endpoint 3 — Entra Role Assignments**
```
GET https://graph.microsoft.com/v1.0/roleManagement/directory/roleAssignments?$expand=principal&$select=id,roleDefinitionId,principalId,principal
Returns: all directory role assignments with principal details
Handle pagination via @odata.nextLink
Store as: data_source = 'graph_role_assignments'
```

**Endpoint 4 — SharePoint Tenant Settings**
```
GET https://graph.microsoft.com/v1.0/admin/sharepoint/settings
Returns: sharingCapability (tenant external sharing setting) and other SPO config
Store as: data_source = 'graph_spo_settings'
```

**Endpoint 5 — Guest Users**
```
GET https://graph.microsoft.com/v1.0/users?$filter=userType eq 'Guest'&$select=id,displayName,userPrincipalName,createdDateTime,accountEnabled
Returns: all guest accounts with creation dates
Handle pagination via @odata.nextLink
Store as: data_source = 'graph_guests'
```

**Endpoint 6 — Copilot Usage Detail**
```
GET https://graph.microsoft.com/v1.0/reports/getMicrosoft365CopilotUsageUserDetail(period='D30')
Returns: per-user Copilot activity — prompts submitted, active days, last activity per app
Store as: data_source = 'graph_copilot_usage'
```

**Endpoint 7 — M365 Active User Detail**
```
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserDetail(period='D30')
Returns: per-user M365 app adoption (Exchange, SharePoint, OneDrive, Teams)
Store as: data_source = 'graph_m365_users'
```

**Endpoint 8 — Microsoft Secure Score**
```
GET https://graph.microsoft.com/v1.0/security/secureScores?$top=1
Returns: currentScore, maxScore, averageComparativeScores, controlScores per category
Store as: data_source = 'graph_secure_score'
```

---

### Source 3: Purview / Compliance API (stubs only)
Create placeholder functions that return `{"status": "not_implemented", "endpoint": "..."}`. No implementation needed yet.
- DLP policies: `https://api.security.microsoft.com/api/dlppolicies`
- Retention policies: endpoint TBD

---

### Functions to Create

**`NcaBootstrapCustomers`** — HTTP trigger, no required params
- Calls AvePoint /customers/batch
- Upserts results into nca_clients (on avepoint_customer_id)
- Returns the full client list with internal IDs

**`NcaCollectAvePoint`** — HTTP trigger, required param: `clientId` (nca_clients.id)
- Looks up avepoint_customer_id and avepoint_tenant_id from nca_clients
- Calls all 6 AvePoint endpoints sequentially
- Creates or reuses an nca_assessments record for today's date
- Stores each raw response as a row in nca_assessment_data
- Returns: `{ clientId, assessmentId, results: { workspaceOverview: "ok"|"error", compliance: "ok"|"error", dspm: "ok"|"error", ransomware: "ok"|"error", riskRules: "ok"|"error" } }`

**`NcaCollectGraph`** — HTTP trigger, required param: `clientId` (nca_clients.id)
- Looks up m365_tenant_id from nca_clients
- If null, returns `{ error: "m365_tenant_id not set for this client" }`
- Calls all 8 Graph endpoints using the existing GDAP token pattern
- Stores each raw response in nca_assessment_data
- Returns same summary structure as NcaCollectAvePoint

**`NcaTriggerAssessment`** — HTTP trigger, required param: `clientId`
- Creates a new nca_assessments row (status = 'in_progress')
- Runs NcaCollectAvePoint and NcaCollectGraph (inline or via invocation)
- Updates nca_assessments status to 'complete' or 'error'
- Returns assessmentId and full collection summary

**`NcaPurviewStub`** — HTTP trigger
- Returns `{"status": "not_implemented", "endpoints": ["dlppolicies", "retention"]}`

---

### Constraints
- POC only — no retry logic, rate limiting, or production hardening needed yet
- Follow all existing project patterns for auth, secrets, and database access exactly
- Do not modify any existing functions or routes
- Store raw JSON exactly as returned — no transformation or scoring
- Log errors clearly so we can see which endpoints succeed vs. fail on first run
- The `m365_tenant_id` field in nca_clients starts empty — note where it will need to be populated (likely matches the AvePoint tenantId GUID, to be confirmed from first real data)
