# Pathfinder — Open Decisions Register
## AI Discovery Journey · Pathfinder Stage (Foundation)

**Status:** Internal Working Draft v0.1 — *decisions are the weekly group's to make*
**Purpose:** The running list of *probable decisions* for Pathfinder delivery. Each carries why it matters and a few potential options — **starting points, not answers.** The weekly coordination group works the list and records the calls in "Decided."
**How to use:** Pull items into the weekly agenda. When decided, move to **Decided** and update the Pathfinder SOPs (`NCA_Pathfinder_Onboarding_SOP.md`, `NCA_Pathfinder_AI_Readiness_Assessment_SOP.md`, `NCA_Pathfinder_Cleanup_Activation_Cycle_SOP.md`), which carry matching `⟨PENDING⟩` flags.
**No owners are pre-assigned** — the group decides who takes what.
**Note:** Pathfinder is the Foundation stage — the governance managed-service (workspace cleanup → sign-off → Copilot indexing) + basic Copilot activation. It **excludes** the AI-Expert monthly hour (that's Outpost). Some items here are cross-stage — flagged where they touch Outpost or the assessment.

---

## A. Assessment → Pathfinder entry & commercial

**A1 · How does a client move from the Stage 2 Assessment into Pathfinder, and what transfers?**
- Why it matters: a clean handoff means Pathfinder starts with findings, not a blank page.
- Transfers to consider: assessment findings, "who gets Copilot first," source-of-truth notes, governance gaps.
- Status: Open

**A2 · Is the Assessment folded into Pathfinder, or billed separately?** ✅ **DECIDED**
- Decision: the **AI Readiness Assessment is included in signing up for Pathfinder — not a separate billable item.** It's the first step of Pathfinder onboarding (`NCA_Pathfinder_Onboarding_SOP.md` §3).
- Residual: whether Month 1 is priced identically via the standard **AI Consulting Pricing Model** formula or handled as a distinct onboarding line — ⟨open, confirm with the group⟩.

**A3 · What must be true before starting the cleanup cycle?**
- Why it matters: sets the line between onboarding and the ongoing cycle (see the Onboarding SOP Ready-for-Cycle checklist).
- Draft: assessment presented · AvePoint governance side configured · ≥1 Data Owner named · AUP signed · pilot licenses assigned · first workspace picked.
- Status: Open

**A4 · What's in the AI Readiness Assessment (Pathfinder's first onboarding step)?** *(placeholder to flesh out)*
- Why it matters: it's the first step of every Pathfinder engagement — needs a defined, repeatable process.
- Draft shape: set up AvePoint (DSPM/scan) → let run ~2 days → run the Claude assessment process → generate & present the report. The final deliverable is leaner than the very original assessment plans.
- To define: scan scope · the Claude prompt/pipeline (extend `NCA_Assessment_Engine_POC_Prompt.md`) · report template.
- Status: Open

---

## B. Who delivers Pathfinder & cadence

**B1 · Which role delivers Pathfinder day-to-day?**
- Why it matters: Pathfinder excludes the AI-Expert hour — so who runs it? Shapes the whole Delivery SOP.
- Options: (a) a governance/service technician; (b) the AM with NCI service support; (c) light AI-Expert involvement; (d) a dedicated "Pathfinder delivery lead."
- Status: Open

**B2 · Does Pathfinder have a scheduled check-in cadence, or is it managed-service + reactive?**
- Why it matters: determines whether there's a client-facing rhythm at all in Pathfinder.
- Options: (a) a light periodic check-in (e.g., monthly progress review); (b) purely managed-service + reactive Copilot support; (c) milestone-based touchpoints (per N workspaces signed off).
- Lean: (a) a light monthly progress review — keeps exec buy-in during cleanup months.
- Status: Open

**B3 · Who processes sign-offs and enables Copilot indexing?**
- Why it matters: the operational core of Pathfinder; needs a clear hands-on owner.
- Options: (a) governance/service tech in AvePoint; (b) shared with the AM; (c) automated where possible.
- Status: Open

---

## C. Governance setup (Data Owners & AUP)

**C1 · How are Data Owners identified, appointed, and supported?**
- Why it matters: no Data Owner = no sign-off = the cycle stalls.
- Reuse: `NCA_Data_Owner_Role.html`. Options: (a) client names them at kickoff; (b) NCI proposes from the assessment; (c) blend.
- Status: Open

**C2 · Who runs the AUP decision session, and who signs it?**
- Why it matters: NCI drafts, but 3–4 calls are the client's; needs the right room.
- Reuse: `NCI_AI_Acceptable_Use_Policy_Example_v2.docx`. Options: (a) exec session (per Executive Sessions design); (b) async review + sign; (c) AM-led.
- Status: Open

**C3 · Do we need a standalone "workspace owner playbook" deliverable?**
- Why it matters: referenced in the Executive Sessions but never written; Data Owners need a simple how-to.
- Options: (a) a short client-facing one-pager; (b) fold into the Data Owner Role doc; (c) cover live at kickoff.
- Status: Open

---

## D. The cleanup cycle

**D1 · How do we prioritize which workspace goes first?**
- Why it matters: early wins build momentum; wrong first pick stalls.
- Options: (a) AvePoint risk/ROT findings; (b) business priority (the team that wants Copilot most); (c) quick wins first; (d) blend.
- Status: Open

**D2 · Cleanup aggressiveness — delete vs. archive, and who decides?**
- Why it matters: data-quality vs. loss risk; it's the Data Owner's call, but we need guidance.
- Reuse the **non-indexed "versions archive"** pattern for superseded files. Options: (a) archive-by-default, delete rarely; (b) delete ROT, archive versions; (c) Data Owner discretion with guidance.
- Status: Open

**D3 · What exactly does "signed off" attest to?**
- Why it matters: sign-off is what unlocks Copilot indexing — it must mean something specific.
- Draft: content is current/authoritative, permissions are correct, nothing stale or over-shared remains. Confirm wording.
- Status: Open

**D4 · How many cycles / workspaces per period is a healthy pace?**
- Why it matters: sets client expectations and NCI capacity.
- Options: model from AvePoint LOE; pick a target (e.g., N workspaces/month).
- Status: Open

---

## E. Copilot activation in Pathfinder

**E1 · "Who gets Copilot first" — how is the pilot cohort chosen, and who decides?**
- Why it matters: an AvePoint assessment output; limited licenses mean this is a real choice.
- Options: (a) NCI recommends from M365 activity profiles; (b) client picks; (c) blend.
- Status: Open

**E2 · Pilot-user licensing — how many Copilot seats to start, and who buys?**
- Why it matters: **first users need full Copilot licenses** (client-purchased); count drives cost.
- Options: (a) small pilot (e.g., 3–5); (b) by department; (c) client's call with NCI guidance.
- Status: Open

**E3 · Light user training for first users — reuse Stage 1 Basecamp?**
- Why it matters: activation without skill = wasted licenses.
- Options: (a) point them at Stage 1 Basecamp; (b) a short Pathfinder-specific primer; (c) rely on self-serve.
- Status: Open

**E4 · What does "basic Copilot Chat support" include vs. exclude?**
- Why it matters: scope-creep guard; Pathfinder isn't consulting.
- Draft: included = prompt help, day-to-day questions; excluded = agent dev, workflow consulting, Claude/third-party (those are Outpost/Frontier).
- Status: Open

---

## F. AvePoint tooling

**F1 · Who owns AvePoint setup/config, and what's automated vs. manual?**
- Why it matters: the tool does the heavy lifting for the base price to work.
- Options: (a) NCI service tech configures; (b) shared; (c) mostly automated via AvePoint Elements.
- Status: Open

**F2 · Health-monitoring cadence — who watches AvePoint, how often?**
- Why it matters: ongoing workspace health is a Pathfinder promise.
- Options: (a) continuous/automated with periodic review; (b) monthly manual check.
- Status: Open

---

## G. Progress, reporting & Outpost-readiness

**G1 · How do we show progress to the client during the unglamorous cleanup months?**
- Why it matters: the program's known failure mode is losing exec buy-in here.
- Options: (a) a short monthly "workspaces signed off / value unlocked" report; (b) verbal at check-in; (c) a live tracker view (later).
- Lean: (a).
- Status: Open

**G2 · What are the "earned" Outpost-readiness signals, and who watches/raises them?** *(cross-stage — aligns with Outpost register B1)*
- Why it matters: makes Pathfinder→Outpost natural, not a re-sell.
- Signals: enough workspaces signed off, active Copilot use, exec engaged, appetite for agents.
- Status: Open — *keep aligned with Outpost B1.*

**G3 · Who updates the readiness tracker / B3 sign-off log — NCI or the Data Owner?**
- Why it matters: determines whether progress is actually captured.
- Options: (a) NCI maintains; (b) Data Owner attests, NCI records; (c) shared.
- Status: Open

---

## H. Capacity, coverage & escalation

**H1 · How many Pathfinder clients can one delivery person carry?**
- Why it matters: pricing/margin sanity under the AI Consulting Pricing Model.
- Options: model from AvePoint LOE + cycle pace; pick a ceiling.
- Status: Open

**H2 · Coverage when the delivery person is away; escalation path when things go wrong?**
- Why it matters: continuity + relationship protection.
- Options: (a) named backup; (b) AM covers reactive support; escalation → AM → a sales lead.
- Status: Open

---

## I. Onboarding & materials

**I1 · Onboarding timeline / SLA — how fast from signed to first workspace in the cycle?**
- Why it matters: momentum; long setup kills early enthusiasm.
- Options: (a) within ~2 weeks; (b) within 30 days; (c) no set target.
- Status: Open

**I2 · What does NCI need to provision/access, and who supplies it?**
- Why it matters: avoids a stalled setup.
- Draft list: AvePoint provisioned · tenant access scoped · Copilot licenses for pilot users · named client admin + Data Owners.
- Status: Open

**I3 · Do we need client-facing Pathfinder onboarding materials / a Data Owner training lesson?**
- Why it matters: Data Owners are non-technical and need a simple on-ramp.
- Options: (a) a Pathfinder onboarding one-pager + short Data Owner lesson; (b) cover live at the governance kickoff; (c) rely on the Data Owner Role doc.
- Status: Open

---

## J. Onboarding delivery *(adapted from the internal session design v3)*

**J1 · Confirm the onboarding session cadence.** *(flagged for the group)*
- Why it matters: the Onboarding SOP adopts a **3-session shape** (Kickoff → [Assessment] → Report Review → Roadmap Planning). Some clients may want fewer/combined touchpoints.
- Options: (a) full 3-session flow as drafted; (b) combine Report Review + Roadmap into one; (c) a single governance kickoff + the roadmap working session.
- Status: Open — *drafted as (a); group to confirm.*

**J2 · "Your AI Advantage" exec-productivity content — if/when to add it.** *(future item)*
- Why it matters: a motivational exec-value beat (meeting prep, doc review, scenario planning, leading through change, a deliberate "wow moment") exists in the older session design; it's **back-burnered for go-to-market**.
- To decide later: whether it lives in Pathfinder onboarding (kickoff/roadmap) or better fits Outpost adoption, and when we build it.
- Status: Open — *future; not built now.*

**J3 · Legacy from the old session design — confirm dropped.** *(from the v3 review)*
- Drop (proposed): "executive sessions" program branding · "Stage 2/3" language · the proposal/commercial-sale motion · persona/mortgage examples (genericized) · heavyweight "hand it to your lawyer" report positioning. PIPEDA / Bill C-27 left out.
- Status: Open — *proposed dropped; group to confirm.*

---

## K. Program naming — Readiness Levels vs. Pathfinder/Outpost/Frontier/Apex *(cross-stage / program-level — for group discussion)*

**K1 · Do the AI Readiness Levels (1–5) stay as a journey metric, get re-scoped to a 1→3 assessment gauge, or retire?**
- **Why it matters:** the program runs **two parallel progress scales** — Pathfinder/Outpost/Frontier/Apex + Rail A/B (the *position* + the *work*) **and** the AI Readiness Levels 1–5 (a client-facing maturity scale). Today the Levels are wired in *both* as the assessment's output *and* as the journey's maturity axis (Journey Map bands, Framework milestone tags, stage overviews). That dual use reads as competing ladders.
- **Context:** the Levels were originally designed as the **client-facing** "where you are" scale, deliberately distinct from the delivery stages ("what NCI delivers"). The AI Readiness Assessment already scopes **Levels 4–5 as out of scope** ("focuses on the path to Level 3"), and **Level 3 = Ready to Pilot = the Pathfinder activation milestone.**
- **Options:**
  - **(a)** **Re-scope to a 1→3 assessment gauge.** Journey language = Pathfinder/Outpost/Frontier/Apex + rails only. The Readiness Levels live *only* inside the AI Readiness Assessment as a **Level 1 (normal start) → Level 3 (Ready to Pilot = activation)** environment-readiness score that hands off to the journey. Retire Levels 4–5; strip Level tags from the Journey Map, Framework, and stage overviews; trim the handout to 1–3.
  - **(b)** **Retire the Levels entirely.** One convention everywhere; the assessment reports **Rail B foundation progress + a plain "ready to activate Copilot?" gate** — no numeric ladder. Archive the Readiness Levels handout.
  - **(c)** **Keep both + add a Level↔stage crosswalk.** Least change; keeps two client-facing ladders alive (the status quo that prompted this).
- **Recommendation: (a).** The readiness score answers a question the journey doesn't — a *point-in-time* "how ready is your tenant for Copilot" — and the "Level 1 is normal → Level 3 target in 8–10 weeks" framing is a proven client device. Bounding the Levels to 1→3 keeps that value while ending the competing-ladder confusion.
- **Status:** Open — *for the weekly group.*

---

## L. AI access control, permissions tooling & tenant governance *(from the AvePoint field test — Kennedy · Brenden · Matthew)*

*Provenance: the first hands-on run of the AvePoint permissions/data-owner process (largely on NCI's own tenant). The settled calls are in **Decided**; these are the parts still to work.*

**L1 · AI access default-OFF → per-workspace enable with an audit trail.** *(direction decided; mechanics open)*
- Decided direction: AI/Restricted Content Discovery (RCD) is **off for all sites** during review; lifted per-workspace on sign-off. Open: **where the "recorded decision / audit trail" lives** (IT Glue? SharePoint list? AvePoint?) and the exact approval record format.
- Status: Open.

**L2 · Toggling AI access at scale needs a tool.** Changing RCD across many sites is **PowerShell-only today — no friendly web app.** Do we build one? *(ties to the Apex custom-AI-web-apps radar, Apex register §J.)*
- Status: Open.

**L3 · Who holds site-access-restriction control** — delegate to client **site administrators**, or NCI-held? Affects support load and client autonomy.
- Status: Open.

**L4 · Permission-report accuracy.** Reports don't reliably reflect **security-group membership, broken inheritance, or unique sharing links** — reported ≠ actual. Define a **"verify reported vs. actual" step** before relying on a report for sign-off.
- Status: Open.

**L5 · Permissions-tool gaps.** No clear **library-level (granular) permission view**; UI truncates long resource names; users need **training** on the tool.
- Status: Open — *tooling/vendor + enablement.*

**L6 · Metadata / authoritative tuning for Copilot relevance.** A **Status metadata column** + marking a library **authoritative** sharpens Copilot results — **Copilot-only, not Claude.** Granular metadata control for Copilot is unresolved.
- Status: Open.

**L7 · AI-access scoping for non-Copilot clients.** RCD is **tool-agnostic** (also gates Claude / ChatGPT / enterprise search), so the governance applies even without Copilot — but how we **scope and message** it for non-Copilot clients isn't settled.
- Status: Open.

**L8 · Curbing site/group sprawl + preserving history.** Restrict who can **create sites/groups** (each M365 group auto-spawns a SharePoint site, Planner, mailbox…); **educate** on security-group purpose; **archive channels rather than delete groups** (deleting destroys conversation history; some groups carry deletion restrictions, e.g. Viva Engage); **client comms** on the data-loss risk. *(direction decided; lockdown extent open)*
- Status: Open.

**L9 · Data-owner assignment process.** Still unclear. Leaning: **one owner per workspace**; **AM / service lead** as owner for client-facing sites; owners need **training** on the role. *(aligns with C1.)*
- Status: Open.

**L10 · Old / irrelevant data approach.** Leaning: **~4-year not-accessed** starting filter; **archive-by-default, delete only after backup**; **new clean site + old → non-indexed archive** for swamps; **working vs. published separation** at site/library level. Thresholds + defaults to confirm. *(aligns with D2.)*
- Status: Open.

---

## Decided
*Move items here as the group makes the call, with the date and the decision. Then update the Pathfinder SOPs.*

| Ref | Decision | Date | Notes |
|---|---|---|---|
| K0 | **Program naming finalized:** Walk/Run/Fly renamed to Pathfinder/Outpost/Frontier; new Apex stage added for custom build & optimization | recorded 2026-08-14 | Supersedes the Walk/Run/Fly placeholders used throughout the program. The Readiness Levels vs. stage-naming crosswalk (K1) is still open. |
| A2 | AI Readiness Assessment is **included in Pathfinder sign-up** — not separately billable | recorded 2026-07-22 | First step of Pathfinder onboarding (SOP §3). Month-1 pricing mechanics still open. |
| L1 | **AI access default-OFF** — RCD off for all sites during review; lifted per-workspace on Data-Owner sign-off, **with a recorded decision/audit trail** | recorded 2026-07-23 | AvePoint field test. Where the record lives = open (L1). Cleanup SOP §1 ENABLE. |
| L/D1 | **Start with the top 5–10 high-value workspaces**, not all sites | recorded 2026-07-23 | Assessment SOP §5; Cleanup §1 SELECT; Onboarding §6. |
| L10 | **~4-year not-accessed** review filter; archive-by-default, delete only after backup | recorded 2026-07-23 | Cleanup SOP §2; Data Owner Role #2; Workspace Review Checklist. Thresholds still open (L10). |
| L8 | **Restrict site/group creation** to curb sprawl (direction) | recorded 2026-07-23 | Onboarding §7. Lockdown extent open (L8). |
| L6 | Use **metadata (Status column) + authoritative library** to sharpen Copilot relevance | recorded 2026-07-23 | Cleanup SOP §3. Copilot-only. Granular control open (L6). |
| | | | |
