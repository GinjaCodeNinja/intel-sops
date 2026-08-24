# Data & Process Readiness Tracker
## Rail B — AI Discovery Journey

**Status:** Internal Working Draft v0.1
**Purpose:** Track a client's progress on the foundation that AI actually runs on — where their data is, what's authoritative, who owns it, what their core processes are, and which third-party systems hold data AI may need. This is **Rail B** of the journey; it enables and rate-limits **Rail A** (AI Capability).
**How it connects:** the governance gates in Rail A read this tracker. A workspace signed off here (B3) unlocks a build there. A process documented here (B4) unlocks meaningful workflow automation there.

> Much of B1–B3 is produced by the Stage 2 Assessment and the Pathfinder workspace cycle — this tracker **references and rolls up** that work, it doesn't replace it. B4–B6 are the newer pieces this journey adds.

**How we record this (for now):** keep this tracker per-client in a lightweight tool — IT Glue, a SharePoint list, or a spreadsheet. Not ideal, but real. Keep the structure clean and consistent so it could later feed a client-facing progress portal (a long-term someday, not built yet).

---

## Milestone status at a glance

| Milestone | What "done" means | Status | Owner | Notes |
|---|---|---|---|---|
| **B1 · Know where your data is** | A map of every place content lives (M365 sites, Azure Files, email, Teams, local, 3rd-party apps) | ☐ not started ☐ in progress ☐ done | | |
| **B2 · Source of truth & ownership** | Each area has an authoritative location + a named Data Owner | ☐ / ☐ / ☐ | | |
| **B3 · Clean & sign off workspaces** | ROT removed, permissions correct, owner signed off → safe to index | *ongoing — track per workspace below* | | |
| **B4 · Core processes documented (20/80)** | The handful of core processes each have a lean SOP | *ongoing — track per process below* | | |
| **B5 · Third-party platforms inventoried** | Apps holding business data catalogued; AI-relevance flagged | ☐ / ☐ / ☐ | | see Integration Inventory |
| **B6 · Integration readiness assessed** | Connection path triaged per AI-relevant app | ☐ / ☐ / ☐ | | see Integration Inventory |

---

## B3 — Workspace sign-off log
*The Pathfinder cycle. Each signed-off row unlocks Rail A builds on that data.*
*"Permissions checked" = verified against the actual site + security-group config, broken inheritance, and sharing links (not just the report). "Copilot indexing enabled" = the AI-access restriction was lifted for this workspace, recorded as an audit trail (who approved, when).*

| Workspace / site | Data Owner | Cleaned | Permissions checked | Signed off | Copilot indexing enabled | Date |
|---|---|---|---|---|---|---|
| | | ☐ | ☐ | ☐ | ☐ | |
| | | ☐ | ☐ | ☐ | ☐ | |
| | | ☐ | ☐ | ☐ | ☐ | |

---

## B4 — Core process documentation (20/80)
*Identify the processes that run the business; document each at the 20% of steps that drive 80% of the outcome. Prioritize the ones AI is most likely to touch. Keep them lean — an EOS-style Documented-and-Followed SOP, not a manual.*

| Core process | Owner | AI-relevant? | 20/80 SOP status | Feeds which AI experiment? | Notes |
|---|---|---|---|---|---|
| _(e.g. new project setup)_ | | High / Med / Low | ☐ drafted ☐ followed | | |
| | | | | | |
| | | | | | |

**Prioritization hint:** a process is a strong early candidate when it's (a) frequent, (b) tedious, (c) fairly repeatable, and (d) touches data that's already signed off (B3).

---

## Foundation Catch-Up Backlog
*Only for clients who entered above Pathfinder (arrived directly at Outpost/Frontier/Apex, or jumped straight to Claude).* Entering high changes their **position**, not their **foundation** — the earlier-stage basics still have to get done. They may move through them fast, but this list keeps them **visible so nothing gets glossed over.** Track each to done; the governance gates (§9 of the framework) will block real-data builds until the relevant items are cleared, regardless of stage entered at.

| Foundation item they still owe | Rail | Why it matters | Status | Target | Notes |
|---|---|---|---|---|---|
| Basic AI governance / AUP in place | B | Nothing safe runs without it | ☐ | | |
| Data ownership assigned | B | No accountable owner = no sign-off | ☐ | | |
| Cleanup + sign-off on the workspaces they're *actually using* | B | They're already building on this data | ☐ | | |
| Copilot fluency basics | A | Skills the advanced work assumes | ☐ | | |
| Workflow-thinking basics (AI vs automation vs human) | A | Or they automate the wrong things | ☐ | | |
| _(add client-specific gaps)_ | | | ☐ | | |

> **AM note:** for a jumped-ahead client, nudging them back to shore up these basics is a core account-management job — do it while the excitement of the advanced tools is carrying momentum.

---

## Progress narrative (for the monthly session & leadership)

- **This period's foundation wins:** _(outcome language — "the estimating team's files are now in one signed-off site, so Copilot stops surfacing old versions")_
- **What this unlocked on the AI side:** _____________
- **Biggest remaining foundation gap:** _____________
- **Next foundation milestone we're pushing:** _____________

---

## The two rails, side by side
Keep a rough read on where the client sits on each so the monthly session can balance them.

| | Behind | On track | Ahead |
|---|---|---|---|
| **Rail A — AI Capability** | | | |
| **Rail B — Data & Process** | | | |

*If Rail A is running ahead of Rail B, slow the builds and shore up the foundation — building on unorganized data produces unreliable results and erodes trust.*
