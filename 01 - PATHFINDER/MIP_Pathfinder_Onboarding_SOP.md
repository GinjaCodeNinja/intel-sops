# Pathfinder — Onboarding SOP *(placeholder)*
## AI Discovery Journey · Pathfinder Stage (Foundation) · For the Pathfinder delivery lead

**Status:** Internal Working Draft v0.1 — **placeholder.** EOS-style (20/80, point form). Points marked `⟨PENDING → Register §X⟩` await the weekly group. No named owners.
**Delivery role:** role-neutral "Pathfinder delivery lead" ⟨PENDING → Register §B1⟩. (Pathfinder excludes the AI-Expert monthly hour — that's Outpost.)
**What this covers:** the **one-time setup** from **Pathfinder sign-up → ready for the cleanup cycle.** Pathfinder *starts with* the AI Readiness Assessment (its own SOP), included in sign-up — **not a separate billable item** (decided). Onboarding then sets up governance and hands off to the **Cleanup & Activation Cycle SOP** (`NCA_Pathfinder_Cleanup_Activation_Cycle_SOP.md`).
**Stance:** Consult-construct — we run the assessment and set up governance/tooling; the client owns the decisions (ownership, what's allowed, what's authoritative).

> **How we deliver it — a 3-session shape** (adapted from the internal session design; the old "executive sessions" branding is dropped). **The exact cadence is ⟨PENDING → Register §J1 — for the group to confirm⟩** — some clients may want fewer/combined touchpoints.
> **Kickoff → [Assessment runs] → Report Review → Roadmap Planning → hand to the cleanup cycle.**

---

## 1. Purpose & boundary
- Get a new Pathfinder client from *signed up* to *ready for the cycle*, consistently.
- One-time. The ongoing workspace cycle lives in the **Cleanup & Activation Cycle SOP**.
- Pathfinder is **Rail B foundation** (framework milestones B1–B3) + a light Copilot activation entry. Target: Readiness **Level 3** (activation).

## 2. Trigger & sign-up
- Trigger: client signs up for **Pathfinder**. The AI Readiness Assessment is the first thing Pathfinder does, not a separate purchase. ⟨→ Register §A2 (Decided)⟩
- Confirm the primary client contact and exec sponsor.

## 3. Session 1 — Kickoff *(~45–60 min · owner + key execs)*
Frame it: *"Before the technical assessment, there are three questions only you can answer — your answers shape what we look at, what we prioritize, and what Copilot actually does for your business."*
- **The Three Questions:**
  1. **What should Copilot have access to?** Walk the categories — client files, internal operations (HR/finance), email & calendar, Teams conversations. Goal: move them from *default access* to *intentional access*.
  2. **What's your source of truth for each area?** *"If there are three copies of the same doc in three folders, Copilot doesn't know which one you trust — you do, but you've never had to write it down."*
  3. **Does each area have a responsible owner — and do they know it?** The accountability gap; this seeds the Roadmap session.
- **Vocabulary Bridge** *(~10 min):* name the four terms the report will use so there are no surprises — **Information Scope · Source of Truth · Data Ownership · Shadow AI / AI Acceptable Use Policy.** Not a governance lesson.
- **Reflection Guide:** hand over the short between-sessions guide (reuse `NCA_Reflection_Guide_BetweenSessions.html`) — a few honest questions (what wouldn't you want Copilot to read · where does time disappear · who do people go to for the real answer · potential data owners by area · your honest concern · what success looks like in 6 months). Framed as leadership prep, never "homework."
- Introduce the **Readiness Level (1–3)** framing before they ever see a number: *"Most orgs your size are at Level 1 — it's a starting line, not a grade."*

## 4. The AI Readiness Assessment runs → see the Assessment SOP
- Kick off and run the assessment — **`NCA_Pathfinder_AI_Readiness_Assessment_SOP.md`** (AvePoint scan → Claude report → present). Its output feeds Sessions 2 and 3.

## 5. Session 2 — Report Review *(~30–45 min · owner + delivery lead)*
- **Reactions first** (~10 min): what landed, what surprised them.
- **Findings walk** (~20 min): the plain-language report — governance gaps, "who gets Copilot first," source-of-truth notes, ROT/risk hotspots, current Readiness Level. Nothing to decide today.
- Confirm Session 3 and close.

## 6. Session 3 — Roadmap Planning *(~60–90 min · owner + likely data owners · a working session)*
- **Scope table:** for each area — *In scope for Copilot?* and *Data in Microsoft 365?* In-scope M365 areas enter the cleanup queue; non-M365 data is flagged for a **separate integration discussion** (migration / MCP / other — ties to Rail B B5–B6 and Frontier).
- **Name the Data Owners** (registry — reuse `NCA_Data_Owner_Role.html`): **one named person per workspace/area.** *"An owner who doesn't know they're an owner is not an owner."* **No owner, no access** — an area with no owner does not get enabled. For **client-facing sites**, the natural owner is often the **account manager or service lead** who keeps that client's data accurate. ⟨assignment process still being defined → Register §L9, §C1⟩
- **Prioritize the first workspaces** — start with the **top 5–10 high-value** ones (value / readiness / owner-motivation); bias to an early win. AI access stays **off for the rest** until each is reviewed and signed off (see §7). ⟨→ Register §D1, §L1⟩
- **Copilot licensing:** confirm seats for the **pilot cohort** — first users need full Copilot licenses; count drives cost. ⟨cohort & count → Register §E1, §E2⟩
- **AUP handover:** first ask *"what's most important about how AI is used here — and what would be completely unacceptable?"*, then hand over the AUP as an **example only** — *not a draft policy, not legal advice; develop it with your own counsel.* (Reuse `NCI_AI_Acceptable_Use_Policy_Example_v2.docx`.) The client makes the few calls that are theirs. ⟨who runs/signs → Register §C2⟩
- Deliverables handed over: Data Owner registry · first-workspace priority order · example AUP · Data Owner one-pager.

> **AvePoint — two distinct touchpoints:** the **scan/DSPM** side feeds the assessment (§4, Assessment SOP); the **Workspace Management/Elements** side (below) runs the ongoing cleanup/sign-off cycle.

## 7. Provisioning & governance tooling
- **Configure AvePoint Workspace Management/Elements** for the ongoing cycle — Data Owner tracking, workspace health, sign-off workflow. ⟨ownership/automation → Register §F1⟩
- Confirm tenant/workspace access scoped for NCI; named client admin + Data Owners confirmed.
- **Set the tenant governance baseline** (before the cleanup cycle starts):
  - **AI access default-OFF** — turn off Restricted Content Discovery across all sites; it gets lifted per-workspace on sign-off (Cleanup SOP). Tool-agnostic (also gates Claude/ChatGPT/search). ⟨toggling at scale needs a tool → Register §L1, §L2⟩
  - **Curb sprawl** — restrict who can create sites/groups (each M365 group auto-spawns a SharePoint site, Planner, mailbox…), and decide who holds site-access-restriction control (delegate to site admins?). ⟨→ Register §L3, §L8⟩
  - **Client comms** — flag that uncontrolled site/group creation (and deleting groups) risks data loss; set expectations on the governance model. ⟨→ Register §L8⟩

## 8. Open tracking
- Open the **readiness tracker** (`NCA_Data_Process_Readiness_Tracker.md`) — the **B3 sign-off log** is the cleanup cycle's tracker. ⟨who updates → Register §G3⟩
- Set where the client record lives (IT Glue / SharePoint list / spreadsheet for now).

## 9. Ready-for-Cycle checklist *(handoff to the Cleanup & Activation Cycle SOP)*
- [ ] Signed up; Kickoff done (three questions, vocabulary bridge, reflection guide)
- [ ] Assessment run and report presented (Report Review)
- [ ] Roadmap done: scope table, Data Owner registry (no major area ownerless), first workspaces prioritized
- [ ] AUP handed over (example-only); client's calls made
- [ ] Pilot cohort chosen and **Copilot licenses assigned**
- [ ] AvePoint governance side configured; tracker / B3 sign-off log open
- → Proceed to the **Cleanup & Activation Cycle SOP**.

## 10. Open decisions & flags
- Points marked `⟨PENDING⟩` map to `NCA_Pathfinder_Open_Decisions.md`.
- ⟨**FUTURE — group to discuss**⟩ **"Your AI Advantage" exec-productivity beat** (meeting prep, doc review, scenario planning, leading the team through change, a deliberate "wow moment"). Rich material exists in the older session design; **back-burnered for go-to-market** — a future option to add to the kickoff/roadmap, not built now.

---

*Provenance & legacy notes:* adapted from the internal session design **v3** (`NCA_Executive_Sessions_Design_v3.html`), de-branded. Deliberately dropped as legacy: the "executive sessions" program branding, "Stage 2/Stage 3" language (Stage 3 mechanics = the Pathfinder cleanup cycle), the proposal / commercial-sale motion (Pathfinder is a subscription; the assessment is included), and persona-specific (mortgage/Ridgeline) examples. PIPEDA / Bill C-27 context is omitted for now. *Cross-stage:* a client who jumped past Pathfinder carries the outstanding basics on the **Foundation Catch-Up Backlog**, not a fresh Pathfinder onboarding.
