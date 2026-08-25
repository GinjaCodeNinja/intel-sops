# The AI Consulting Delivery Model
## Outpost, Frontier & Apex — the fractional AI-expert engagement, end to end

**Status:** Internal Working Document — Draft v0.4
**Purpose:** Define what the **AI Consulting** component of the Managed Intelligence Program (MIP) offering actually delivers — the hands-on path NCI leads a client down once they're past the foundation, through Copilot fluency, into agents, automation, and (at Frontier) Claude and third-party AI, with custom builds and ongoing optimization at Apex, while their data and process foundation keeps maturing underneath.
**Audience:** NCI delivery staff (the "fractional AI expert" role). A lighter client-facing view is produced separately (`NCA_Discovery_Journey_Map.html`).
**Scope:** the **Outpost, Frontier, and Apex** consulting stages only. This is *not* the whole-program map.
**v0.4 changes:** renames Walk/Run/Fly to **Pathfinder/Outpost/Frontier**; splits the former Fly scope into **Frontier** (tool graduation + integration readiness + governance groundwork) and a new **Apex** stage (custom build, managed digital workforce, ongoing optimization/roadmap planning); reflects the single **AI Consulting Pricing Model** that now prices all paid work, replacing separate per-stage pricing.

---

## Where this sits
- **The whole program** (Basecamp → Pathfinder → Outpost → Frontier → Apex, both rails, the core principles) lives in the **Program Overview** (`NCA_AI_Delivery_System_Overview.md`) — that's the map. Read it first.
- **Basecamp** (the intro workshop) and **Pathfinder** (the Foundation governance managed-service) each have their **own Overview + SOPs** — this document does *not* cover their delivery.
- **This document is the delivery model for the paid consulting stages — Outpost, Frontier & Apex.** It goes deepest there because that's where the AI-capability work concentrates. The whole-journey visual companion is the Journey Map (`NCA_Discovery_Journey_Map.html`).

---

## 1. What this is, and why it exists

Basecamp teaches people that AI is useful. Pathfinder — starting with the AI Readiness Assessment — makes their environment safe and gets Copilot activated for first users. **This model picks up from there:** the Outpost → Frontier → Apex part where a client moves from "we've tried Copilot and we like it" to "AI is changing how we work."

It fills three gaps flagged as *not written* in the May 2026 State of Play: the Outpost service description, the fractional expert's monthly session format, and the declarative-agent support scope. It is the **curriculum and delivery layer** underneath the Outpost stage's `AI Adoption & Analytics` and `Task Automation` MI components, extending into Frontier and Apex.

### The core stance
The client is the domain expert; NCI is the guide. A 150-person engineering firm knows its own workflows, its own pain, and its own opportunities far better than we ever will. Our job is not to tell them what to automate — it's to **give them a safe way to discover it themselves, a language to reason about it, and the guardrails to do it without getting hurt.** They will find uses we would never have thought of. We make sure they find them safely and can tell which ones are worth keeping.

This is the consult-construct model applied to discovery: **we advise, structure, and de-risk; the client explores, decides, and owns.**

### The design principle: spine + pull-menu
- The **spine** is a loose progression — a suggested path from fluency to automation. It is a *default suggestion, not a gate.*
- The **pull-menu** is a catalog of experiments the client's working group draws from whenever they want. This is what lets them "discover what lands" rather than sit through a course.

Structure is available on demand, never imposed.

---

## 2. How this fits the existing MIP frameworks

This is **not a fourth framework.** It is the delivery layer under the three that already exist. One story, three views:

| Existing framework | Role | This framework's relationship |
|---|---|---|
| **AI Readiness Levels 1–5** | Client-facing maturity axis | Each rail milestone maps to a Level — *under review; see Pathfinder register §K (Levels vs. Pathfinder/Outpost/Frontier/Apex)* |
| **Pathfinder / Outpost / Frontier / Apex** | Customer-journey stages | The journey lives mostly in Outpost, extends into Frontier and Apex |
| **9-component Managed Intelligence Model** | Capability building blocks | The two rails *are* the curriculum that builds those components |

> **Coordinate, don't pre-empt:** the MI Model component design (State of Play Decision 5) is still an open NCI design session. This framework is an **input** to that session, not a competing definition. Where it implies a component name or boundary, flag it for that discussion.

**Naming discipline:** stage names (Pathfinder / Outpost / Frontier / Apex) are decided. All rail/milestone names below remain working, outcome-language placeholders — no client-facing name below the stage level is final until marketing signs off.

---

## 3. The two rails

A client matures along **two different axes at once**, and keeping them distinct is what stops the program from going vague:

- **Rail A — AI Capability:** how well the client understands and *uses* AI. (Fluency → workflow thinking → builds → agents.)
- **Rail B — Data & Process Foundation:** how well the client understands and *manages their own data and processes* — where data lives, what's authoritative, what their core processes are, and which third-party systems hold data AI may need.

**Rail B is the enabler and the rate-limiter of Rail A.** You cannot safely build on data nobody has organized, and you cannot connect AI to systems nobody has inventoried. Much of Rail B is already in the MIP program — Stage 2's "two questions," the Data Owner role, and the Pathfinder workspace cycle are all Rail B — but it has never been named as a tracked stream. This framework makes it explicit and gives it its own progress tracking.

### The rails meet at the governance gates
The gates in Rail A (§9) don't invent new checks — they *read Rail B's progress*. A workspace that Rail B has cleaned and signed off is what unlocks a Rail A build on that data. This handshake is what makes the two rails one journey instead of two to-do lists.

| Rail B milestone reached… | …unlocks in Rail A |
|---|---|
| Workspace cleaned & signed off (B3) | Builds/experiments on that data (Stage 4, standard gate) |
| Core process documented 20/80 (B4) | Meaningful Workflow Thinking + automation of that process (Stage 3–4) |
| Third-party app inventoried & integration triaged (B5–B6) | Extend & Orchestrate / integrations (Stage 6); unattended work (heavier gate) |

### Terminology (keep these straight)
- **Rails** = the two kinds of *work* (A: AI Capability, B: Data & Process). They advance together and answer *"what are we doing?"*
- **Pathfinder / Outpost / Frontier / Apex** = the client's *position* on the journey (Foundation → Adoption → Scale-Readiness → Custom Build). They answer *"how far have we gotten?"* Rails and stages describe the **same journey**, so they can't conflict.
- **Tool** = Copilot is the spine tool for Pathfinder/Outpost; Claude and other third-party AI enter at Frontier (see §5); custom builds happen at Apex.

### The journey aligns to Pathfinder / Outpost / Frontier / Apex
This is the canonical mapping. The rails run through all four stages; the *balance* shifts. Nothing turns off — stages stack (Apex sits on top of Frontier, Outpost, and Pathfinder).

| Band | Character | Rail B — Data & Process | Rail A — AI Capability | Readiness Level |
|---|---|---|---|---|
| **Pathfinder** · Foundation | Foundation-heavy | Know your data · Source of truth & owners · Clean & sign off (ongoing) | Foundations · Copilot Fluency | 1 → 3 |
| **Outpost** · Adoption | Capability-heavy | Document core processes (20/80) | Workflow Thinking · First Builds · Prove & Productionize | 4 |
| **Frontier** · Scale-Readiness | Integration-readiness on both rails | Inventory platforms · Assess integrations | Claude + third-party AI arrives | 5 |
| **Apex** · Custom Build & Optimization | Build & operate on both rails | Integration triage acted on | Extend & Orchestrate · custom agents/solutions · ongoing optimization | 5+ |

**Start anywhere — but complete the foundation as catch-up, never skip it.** A client can enter or jump to any stage (some arrive already using Claude). Entering high changes the *starting position*, not the *required foundation*: the earlier-stage basics still get done, compressed if the client is capable. This is enforced two ways — (1) **the gates don't care what stage you bought into** (an Apex-stage Claude/agent build on real data still requires the relevant workspace cleaned & signed off and governance in place, §9); and (2) an **explicit per-client Foundation Catch-Up Backlog** keeps the outstanding basics visible so nothing gets glossed over (`NCA_Data_Process_Readiness_Tracker.md`).

---

## 4. Rail A — The Spine (AI Capability)

Six stages in client-outcome language. Each answers "what is different for the client after this stage."

### Stage A1 — Foundations
*Basic AI literacy, prompting, and a safe-use mindset.* Delivered by Stage 1 Basecamp (complete). Level 1 · pre-Pathfinder/Pathfinder.

### Stage A2 — Copilot Fluency
*Master the full license — get real daily value out of what they already pay for.* Org-wide recall ("find that thing we worked on for the marina job"), meeting summaries, cross-app drafting. Most of the ROI a client ever gets is here — don't let a working group chase agents while the org still can't get a good summary. MI: Copilot Activation → AI Adoption · Pathfinder→Outpost · Level 3–4.

### Stage A3 — Workflow Thinking
*Learn to see work as processes, and to tell what should be AI, what should be plain code, and what should stay human.* The single most important conceptual leap — the one the client explicitly lacked. Core tools: the AI/Deterministic/Human triage aid and the Workflow Deconstruction worksheet. **Depends on Rail B having named the process (B4).** MI: bridges AI Adoption → Task Automation · Outpost · Level 4.

### Stage A4 — First Builds (guided experiments)
*The working group pulls experiments from the menu and discovers what lands.* Generate an image, analyze a spreadsheet, build a simple declarative agent in Copilot Studio. Most are throwaways — that's the point. (Claude-based experiments live at Frontier — see §5.) **Builds on real data require the relevant Rail B workspace sign-off (B3).** MI: Task Automation · Outpost · Level 4.

### Stage A5 — Prove & Productionize
*An experiment that landed graduates from "play" to a supported build* — with data access, guardrails, an owner, and measured value. The **graduation gate** prevents shiny-toy sprawl and is a clean Outpost→Frontier moment. MI: Task Automation → Advanced Agents / AI Ops · Outpost→Frontier · Level 5.

### Stage A6 — Extend & Orchestrate
*Beyond M365 — connect AI to the rest of the business and let capable, well-governed systems do more.* Claude arrives and integration readiness is assessed at Frontier; MCP connections, multi-agent work, and the proper home for **unattended / autonomous AI** get built at Apex once B5–B6 and the heavier gate are in place. MI: Systems Integration, Advanced Agents, AI Ops, Orchestration · Frontier→Apex · Level 5+.
> **On the radar (placeholder):** agents alone don't always carry a workflow. Some workflows need a **custom AI-integrated web app** — a purpose-built app with AI inside (structured UI, forms, state, human steps) to keep the workflow moving. This is an Apex capability we'll need to develop an approach for — see §14 and the Apex Open Decisions register.

---

## 5. The tool sequence: Copilot first, Claude at Frontier

**Copilot is the spine tool for Pathfinder and Outpost; Claude and other third-party AI (ChatGPT, xAI) arrive at Frontier.** This is a deliberate sequence, not an accident of pricing.

| | Copilot / M365 (Pathfinder → Outpost) | Claude + third-party AI (Frontier → Apex) |
|---|---|---|
| **Role** | The safe space to build governance and skills — deepest in the client's existing workflow | The advanced payoff — long-document reasoning, custom projects, code, flexible workflows/MCP |
| **Governs via** | M365 permissions + AvePoint (Rail B) | Claude safe-configuration (Stage 2 governance) + Systems Integration governance |
| **Agent path** | Copilot Studio declarative agents | Claude Projects → MCP → custom agents |

**Why this sequence (internal rationale — keep out of client copy):** Copilot carries the early journey because it's the familiar tool already embedded in their day. That deliberately concentrates the early learning-curve friction on Copilot, so that when a client reaches Frontier, Claude lands as a step-change — *it feels like magic* rather than "another tool." Client-facing copy says only *"build your skills on Copilot, then graduate to Claude and advanced AI."*

**The exception is real and expected:** some clients arrive already using Claude and effectively jump to Frontier or Apex. That changes their *position*, not their *foundation* — they still complete the Pathfinder/Outpost basics as catch-up (§3, and the Foundation Catch-Up Backlog). Nudging a jumped-ahead client back to shore up governance and Copilot fluency is a core account-management job.

---

## 6. Rail B — Data & Process Foundation

Where the client learns to manage the raw material AI runs on. Less a strict sequence than a set of milestones that mature over time and gate Rail A. Progress is tracked in `NCA_Data_Process_Readiness_Tracker.md`.

### Milestone B1 — Know where your data is
*A map of where content actually lives* — SharePoint sites, Azure Files archive, email, Teams, local drives, and third-party apps. Kicks off in the Stage 2 Assessment. MI: Data Foundation & Quality · Level 1–2.

### Milestone B2 — Establish source of truth & ownership
*For each area, which copy is authoritative, and who owns it.* This is Stage 2's second "question" plus the Data Owner role made real. Kills the "three versions of the lender guidelines" problem that makes AI answers unreliable. MI: Governance & Policy + Data Foundation · Pathfinder · Level 2.

### Milestone B3 — Clean & sign off workspaces *(rolling — never "done")*
*The Pathfinder cycle:* remove ROT/stale content, fix permissions, Data Owner signs off → the workspace is safe for Copilot indexing. This is **not a roadblock and not a whole-environment gate**: the client signs off *some* workspaces, proceeds, and the cycle keeps running in the background indefinitely — for many clients it's never fully complete, and that's fine. **It's the primary handshake with Rail A, but it unlocks Rail A one workspace at a time** — you build on the workspaces that are cleaned, while cleanup continues elsewhere. Track continued progress in the sign-off log rather than treating it as a milestone that must finish. MI: Data Foundation & Quality · Pathfinder · Level 2–3.

### Milestone B4 — Name & document core processes (20/80)
*Identify the handful of processes that run the business and document each at the EOS-style 20/80 level* — the 20% of steps that drive 80% of the outcome, kept lean. Prioritize the processes AI is most likely to touch. **Directly feeds Rail A Workflow Thinking (A3)** — you can't deconstruct a workflow nobody has named. MI: feeds AI Adoption + Task Automation · Outpost · Level 3–4.

### Milestone B5 — Inventory third-party platforms & their data
*Catalogue the SaaS/line-of-business apps that hold business data* (CRM, project/PM tools, accounting, document management, etc.), and flag for each whether AI may need to reach it. Tracked in `NCA_ThirdParty_Integration_Inventory.md`. MI: precursor to Systems Integration · Outpost→Frontier · Level 4.

### Milestone B6 — Assess integration readiness
*For each app AI needs, triage how it could connect* — MCP server available? public API? native Copilot/Claude integration? none yet? — plus the governance/consent posture (who approves the connection, what data it exposes). **Feeds Rail A Extend & Orchestrate (A6)** and connects to the third-party-AI-access governance conversation. MI: Systems Integration · Frontier · Level 5.

> **Watch the scope on B4.** Don't let a 150-person firm try to document every process. Core processes only, 20/80 depth, AI-relevant ones first. Boiling the ocean here kills momentum faster than anything.

---

## 7. Attended vs. unattended AI — the governance dividing line

The client asked about "Co-work" and other **unattended** AI. This distinction sets how much guardrail a use needs.

| | **Attended AI** | **Unattended / autonomous AI** |
|---|---|---|
| **Definition** | A human reviews each output before use | Acts across steps without per-step review |
| **Examples** | Copilot drafting; Claude summarizing | "Co-work"-class autonomy; scheduled agents; pipelines |
| **Risk** | Contained — a person is the last check | Elevated — errors compound before anyone sees |
| **Gate** | Standard governance handoff | **Heavier gate** (§9) |
| **Home** | Stages A2–A4 · Pathfinder/Outpost · Copilot | Stages A5–A6 · Frontier prepares, Apex builds · Claude & third-party |

The client's posture — *try it safely, then decide if it's even useful* — is exactly what we design for: an isolated sandbox experiment plus a stronger checkpoint, **not** a production rollout. Help them answer, in order: (1) *Can we run this safely, contained?* then (2) *Is it useful enough to be worth governing?* Many autonomous tools fail Q2 cheaply — a good outcome.

---

## 8. The Pull-Menu (experiment catalog)

The deck the working group draws from — the engine of "discover what lands." (`NCA_Experiment_Cards.md`.) Every card carries: **Category** (Create/Find & Recall/Analyze/Automate/Agent/Integrate) · **Level** (Explore/Build/Advanced) · **Track** (Copilot/Claude/Either) · **Prereqs** (incl. ⚠ which gate applies) · **What it teaches** · **What "good" looks like.** Starter deck includes the client's explicit asks — generate an image, analyze an Excel dataset, build a simple agent — plus Copilot recall and Claude-track cards.

---

## 9. Governance gates

Two lightweight checkpoints that keep discovery safe. They **read Rail B's progress** rather than inventing new checks, and reference (don't duplicate) the Stage 2 governance work and Claude safe-configuration.

**Standard gate — before any experiment touches real company data.** Confirms: the data's workspace has an owner and is signed off (Rail B / B3), permissions are correct, and outputs will be human-reviewed before use. Sandbox/dummy-data experiments skip it.

**Heavier gate — before any unattended/autonomous use.** Everything above, plus: a bounded written scope of what it can touch and do, a named accountable human owner, a kill switch, monitoring so failures are noticed, and a written "what could go wrong + blast radius" note. Nothing autonomous touches production data or real actions without this. For anything reaching a third-party system, B6's integration + consent triage must be complete.

> The client's Claude safe-configuration ask connects here: it's a prerequisite feeding these gates, delivered under Stage 2 governance — not a separate workstream in this framework.

---

## 10. The Emerging Capabilities lane (standing)

New AI features arrive constantly — Co-work today, something else next quarter. A fixed curriculum is stale on arrival. So there's a **permanent intake lane owned by the fractional expert:** evaluate in a sandbox → assess governance → decide (adopt / park / reject) → fold survivors into the experiment deck and training. Uses the **New Capability Evaluation template** (`NCA_New_Capability_Evaluation_Template.md`). This turns "keeping up with AI" from a scramble into a repeatable, deliverable service — a strong standing justification for the ongoing subscription. It's a permanent agenda item in the monthly session.

---

## 11. The Fractional AI Expert role

Guide, not driver. Consult-construct. Standing frame: *"You're the domain experts — we help you structure and de-risk what you find."*

**Monthly session format** (`NCA_Fractional_Expert_Session_Format.md`) — recurring ~1-hour advisory with per-stage variants. Every session tracks **both rails**: what landed on Rail A, and what data/process/integration progress happened on Rail B. The **ROI loop** (Experiment Log → monthly value story) counters the program's known failure mode of losing exec buy-in during unglamorous months.

---

## 12. The Working Group operating model

Deliberately light. The client already started a working group; we give it just enough structure:
- **Roles:** an executive **sponsor**, one or two **champions**, and rotating **testers** from different departments (the domain experts who find the uses — and who know where the data and processes really live, which is why they also feed Rail B).
- **Cadence:** a short regular working-group meeting between our monthly sessions.
- **Backlog:** a simple shared list — experiments to try (Rail A) and data/process/integration items to resolve (Rail B). For a client who entered above Pathfinder, this includes the **Foundation Catch-Up Backlog** (the outstanding earlier-stage basics), tracked with the AM so nothing gets glossed over (`NCA_Data_Process_Readiness_Tracker.md`).
- **The self-navigation bar:** the group should run itself from the guides and pull-menu alone, calling us when they hit something interesting or need a gate.

---

## 13. Where to find everything (index)

The deliverables that support this framework — and the whole program — are indexed in the **AI Delivery System Hub** and in each stage's **Overview** page (each Overview carries that stage's deliverables list). Use the Hub sidebar as the live index rather than a static list here, so it stays current as docs are added. The shared tools this framework references (pull-menu / experiment cards, the triage aid and workflow-deconstruction worksheet, the experiment log, the readiness tracker, the integration inventory, the session format, the New Capability Evaluation, and the Unattended AI starter kit) all live in the Hub's **Reference · shared tools** section.

---

## 14. Open items to resolve
- **Feed into MI Model design session (Decision 5)** — reconcile both rails' milestones against final component names/boundaries.
- **Session-format review** — confirm the monthly session format and consult-construct boundaries are deliverable.
- **Final naming below the stage level** — defer all client-facing rail/milestone names to marketing.
- **Claude safe-config handoff** — confirm the checklist lives in Stage 2 governance and is referenced, not rebuilt, here.
- **Rail B ↔ Stage 2/Pathfinder overlap** — much of Rail B (B1–B3) already lives in the Assessment + Pathfinder cycle. Confirm this framework *references* those deliverables rather than duplicating them; B4–B6 are the genuinely new pieces.
- **Unattended AI starter kit** — develop from placeholder once we've sandboxed a "Co-work"-class tool ourselves.
- **Custom AI-integrated web apps (placeholder — on the radar)** — develop an approach/solution for purpose-built web apps with embedded AI, for workflows that agents alone can't carry. Apex capability; significant R&D (tech stack, hosting, build/maintain model, pricing) still to define.
- **Apex SOW pricing vs. the AI Consulting Pricing Model** — confirm custom-build engagements are quoted per SOW on top of the standing formula-priced relationship, not folded into it.
