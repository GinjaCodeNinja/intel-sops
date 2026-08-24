# Frontier — Open Decisions Register
## AI Discovery Journey · Frontier Stage (Scale-Readiness)

**Status:** Internal Working Draft v0.1 — *decisions are the weekly group's to make*
**Purpose:** The running list of *probable decisions* for Frontier delivery. Each carries why it matters and a few potential options — **starting points, not answers.** The weekly coordination group works the list and records calls in "Decided."
**How to use:** Pull items into the weekly agenda. When decided, move to **Decided** and update the Frontier SOPs (`NCA_Frontier_Onboarding_SOP.md`, `NCA_Frontier_Delivery_SOP.md`), which carry matching `⟨PENDING⟩` flags.
**No owners are pre-assigned** — the group decides who takes what.
**Note:** Frontier is the Scale-Readiness stage — **tool graduation (Copilot → Claude/third-party), third-party integration readiness (inventory + triage), and unattended-AI governance groundwork.** It's **engagement-based**, runs **on top of a continuing Outpost base**, and hands bespoke build work to Apex.

---

## A. Entry & commercial

**A1 · What are the Frontier-readiness signals, and who decides?** *(cross-stage — aligns with Outpost register F3)*
- Why it matters: Frontier should be a natural next step, not a re-sell.
- Signals: mature Copilot use, first agents live & valued, wants Claude/third-party/integration, has a specific LOB system to connect.
- Status: Open — *keep aligned with Outpost F3.*

**A2 · How is Frontier priced and scoped?**
- Why it matters: needs a clean commercial model consistent with the rest of the journey.
- Lean: priced via the standing AI Consulting Pricing Model like every other stage; any bounded Frontier-specific setup work (e.g. the integration triage pass) may still carry its own SOW.
- Status: Open

**A3 · Does the Outpost base always continue underneath Frontier?**
- Why it matters: "nothing turns off" — but confirm the commercial mechanics.
- Lean: yes — the Outpost relationship continues as the base; Frontier is additive.
- Status: Open

---

## B. Who delivers Frontier

**B1 · Who runs tool graduation and integration triage?**
- Why it matters: Frontier needs both advisory (Claude/third-party rollout) and technical triage capacity.
- Options: (a) AI Expert runs both; (b) a dedicated readiness role; (c) AI Expert + PS/dev for the technical triage.
- Status: Open

**B2 · Frontier engagement capacity & resourcing?**
- Why it matters: affects lead times & how many clients can be graduated at once.
- Options: model per-client effort; decide how many concurrent Frontier engagements NCI can carry.
- Status: Open

---

## C. Integration readiness (MCP / API / native)

**C1 · Who completes the Third-Party Integration Inventory & triage, and when?**
- Why it matters: it's the map that Apex builds from. *(reuse `NCA_ThirdParty_Integration_Inventory.md`.)*
- Options: (a) during Frontier onboarding; (b) started in Outpost as prep; (c) per-integration as needed.
- Status: Open

**C2 · Build vs. buy vs. community — how do we vet third-party connectors / MCP servers at the triage stage?**
- Why it matters: security & reliability of anything we'll later connect to client data.
- Draft: prefer native → vetted vendor MCP → reputable community → custom build; security review before any connector touches real data.
- Status: Open

**C3 · Who approves connecting AI to a third-party system, and how is consent governed?**
- Why it matters: data leaving the M365 boundary is a real governance event *(ties to the third-party-app-consent governance).*
- Draft: admin-approved, scoped access, documented data flow; the client owns the approval.
- Status: Open

---

## D. Unattended-AI governance groundwork

**D1 · What's mandatory before the heavier gate is considered "stood up" and ready for Apex to use?** *(reuse framework §9 + `NCA_Unattended_AI_Starter_Kit.md`)*
- Why it matters: unattended agents compound errors before anyone sees them — highest risk in the program.
- Mandatory (draft): bounded written scope · named accountable human owner · kill switch · monitoring · "what could go wrong + blast radius" note · signed-off data only.
- Status: Open

**D2 · Do we have tooling for agent governance (registry, approval, monitoring, lifecycle)?**
- Why it matters: the "managed digital workforce" promise Apex makes needs real tooling stood up here, not goodwill.
- Options: (a) AvePoint agent-governance features; (b) third-party monitoring; (c) native/manual for now.
- Status: Open

**D3 · Unattended / "Co-work"-class AI — who runs the sandbox-first evaluation, and when?**
- Why it matters: try safely, then decide if it's even useful (the client's posture) — this groundwork happens at Frontier even though production use happens at Apex.
- Draft: sandbox on dummy data → usefulness rubric → heavier gate before any real use. *(reuse Unattended AI Starter Kit — still a placeholder to flesh out.)*
- Status: Open

---

## E. Claude & third-party AI

**E1 · Claude safe-configuration — how is it set up and governed?** *(the client's original ask; folds into governance)*
- Why it matters: Claude enters at Frontier; it must be configured safely before real use.
- Options: (a) a standard Claude safe-config checklist (from Stage 2 governance); (b) per-client.
- Status: Open

**E2 · Claude / third-party licensing — who buys, how many seats?**
- Why it matters: Frontier adds Claude/third-party AI users.
- Status: Open

**E3 · Support scope for Claude / ChatGPT / xAI and Copilot Studio?**
- Why it matters: defines what "third-party AI support" and "Copilot Studio support" actually include.
- Status: Open

---

## F. Handoff to Apex

**F1 · What exactly must be true for the "Ready-for-Apex" checklist to pass?**
- Why it matters: this is the gate that keeps Apex from building on ungoverned ground.
- Status: Open

**F2 · Who raises the Frontier→Apex handoff, and to whom?**
- Why it matters: makes the progression natural, not a re-sell.
- Status: Open

---

## I. Onboarding & materials

**I1 · Client-facing Frontier materials / cut-sheets?** *(marketing + delivery workstream)*
- Why it matters: sales enablement for the graduation step without over-promising (no outcome guarantees).
- Status: Open

**I2 · Onboarding timeline for tool graduation + integration triage?**
- Why it matters: sets expectations for how long it takes to get Apex-ready.
- Draft list: Outpost base active · integration inventory done · governance/gate tooling ready · Claude/third-party licensing.
- Status: Open

---

## Decided
*Move items here as the group makes the call, with the date and the decision. Then update the Frontier SOPs.*

| Ref | Decision | Date | Notes |
|---|---|---|---|
| | | | |
