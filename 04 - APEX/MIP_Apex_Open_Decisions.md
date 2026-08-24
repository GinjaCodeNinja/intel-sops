# Apex — Open Decisions Register
## AI Discovery Journey · Apex Stage (Custom Build & Optimization)

**Status:** Internal Working Draft v0.1 — *decisions are the weekly group's to make*
**Purpose:** The running list of *probable decisions* for Apex delivery. Each carries why it matters and a few potential options — **starting points, not answers.** The weekly coordination group works the list and records calls in "Decided."
**How to use:** Pull items into the weekly agenda. When decided, move to **Decided** and update the Apex SOPs (`NCA_Apex_Onboarding_SOP.md`, `NCA_Apex_Delivery_SOP.md`), which carry matching `⟨PENDING⟩` flags.
**No owners are pre-assigned** — the group decides who takes what.
**Note:** Apex is the Custom Build & Optimization stage — advanced AI & integration: **MCP/API integration builds, custom & autonomous agents, the managed digital workforce, and ongoing optimization/roadmap planning.** It's **engagement-based** (scoped per initiative, additive) and **runs on top of a continuing Outpost + Frontier base.** Highest stakes in the program — autonomous agents in production and AI reaching into line-of-business systems.

---

## A. Entry & commercial

**A1 · What are the Apex-readiness signals, and who decides?** *(cross-stage — aligns with Frontier register F1–F2)*
- Why it matters: Apex should be a natural next step, not a re-sell.
- Signals: Frontier's Ready-for-Apex checklist complete, and the client has a concrete build in mind.
- Status: Open — *keep aligned with Frontier F1–F2.*

**A2 · How is Apex priced and scoped?**
- Why it matters: Apex is variable/additive — needs a clean commercial model.
- ✅ **Working decision:** the client's standing price runs on the AI Consulting Pricing Model regardless of stage; each Apex build is additionally scoped and quoted **per-engagement SOW on top of that base.** Confirm recurring-add-on-hours or blended alternatives are genuinely off the table.
- Status: Open

**A3 · Does the Outpost + Frontier base always continue underneath Apex?**
- Why it matters: "nothing turns off" — but confirm the commercial mechanics.
- Lean: yes — the Outpost + Frontier relationship continues as the base; Apex is additive.
- Status: Open

---

## B. Who delivers Apex & the build team

**B1 · Who scopes/designs Apex engagements, and who builds them?**
- Why it matters: Apex needs both advisory (AI Expert) and hands-on build (dev/PS) capacity.
- Options: (a) AI Expert scopes/designs, PS/dev builds MCP/custom agents; (b) a dedicated Apex build team; (c) AI Expert does light builds, partners for complex.
- Status: Open

**B2 · Apex engagement capacity & resourcing?**
- Why it matters: builds are lumpy and skill-intensive; affects lead times & margin.
- Options: model per-engagement effort; decide how many concurrent Apex builds NCI can carry.
- Status: Open

---

## C. Integration builds (MCP / API / native)

**C1 · Who builds from the Integration Inventory triage handed off by Frontier, and when?**
- Why it matters: Frontier maps and triages; Apex is where the actual connection gets built. *(reuse `NCA_ThirdParty_Integration_Inventory.md`.)*
- Options: (a) immediately on Apex onboarding; (b) queued per-engagement priority; (c) per client request.
- Status: Open

**C2 · How do we vet third-party connectors / MCP servers at build time?**
- Why it matters: security & reliability of anything we connect to client data.
- Draft: prefer native → vetted vendor MCP → reputable community → custom build; security review before any connector touches real data.
- Status: Open

**C3 · Who approves connecting AI to a third-party system, and how is consent governed?**
- Why it matters: data leaving the M365 boundary is a real governance event *(ties to the third-party-app-consent governance).*
- Draft: admin-approved, scoped access, documented data flow; the client owns the approval.
- Status: Open

---

## D. Advanced & unattended agents

**D1 · Who runs the heavier gate at build/deploy time, and what's mandatory before an autonomous agent touches real data/actions?** *(reuse framework §9 + `NCA_Unattended_AI_Starter_Kit.md`)*
- Why it matters: unattended agents compound errors before anyone sees them — highest risk in the program. The gate itself was stood up at Frontier; this is about running it correctly at deploy time.
- Mandatory (draft): bounded written scope · named accountable human owner · kill switch · monitoring · "what could go wrong + blast radius" note · signed-off data only.
- Status: Open

**D2 · Tooling for agent governance (registry, approval, monitoring, lifecycle) — using what Frontier stood up?**
- Why it matters: the "managed digital workforce" promise needs real tooling, not goodwill.
- Options: (a) AvePoint agent-governance features; (b) third-party monitoring; (c) native/manual for now.
- Status: Open

**D3 · Who is accountable for an autonomous agent's actions in production?**
- Why it matters: consult-construct — the client owns decisions; but production autonomy needs a named human.
- Draft: a named client owner per agent; NCI advises/monitors, doesn't own operations.
- Status: Open

---

## E. AI Operations / digital workforce

**E1 · Who operates deployed agents/integrations ongoing, and at what cadence?**
- Why it matters: agents degrade; integrations break; "managed" means monitored.
- Options: (a) NCI-managed operations (monitoring, lifecycle); (b) client-run with NCI advisory; (c) blended.
- Status: Open

**E2 · How is agent performance degradation / failure handled in production?**
- Why it matters: higher stakes than Outpost — a broken production agent has real impact.
- Draft: monitoring + alerts → defined response → kill switch if needed → root-cause + fix.
- Status: Open

**E3 · Who owns the agent/integration registry?**
- Why it matters: you can't manage a digital workforce you can't see.
- Status: Open

---

## F. Ongoing optimization & roadmap planning

**F1 · How often does the standing optimization/roadmap review run, and who runs it?**
- Why it matters: this is a recurring thread distinct from one-off engagements — it needs its own cadence, not just whatever falls out of the last build.
- Status: Open

**F2 · How is Apex value/ROI reported — per engagement, or rolled into one ongoing view?**
- Why it matters: Apex investment is larger; leadership needs to see the return, and it may span multiple concurrent/past engagements.
- Options: (a) per-engagement outcome report; (b) ongoing operations dashboard (later); (c) blended.
- Status: Open

---

## G. Capacity, coverage & escalation

**G1 · Coverage and escalation when a production integration or agent fails?**
- Why it matters: highest-stakes stage; a failure can affect live business operations.
- Draft: monitoring → on-call/defined response → kill switch → AI Expert/dev → AM → a sales lead.
- Status: Open

**G2 · How many concurrent Apex engagements can NCI carry?** *(see also B2)*
- Why it matters: protects delivery quality and lead times.
- Status: Open

---

## H. Onboarding & materials

**H1 · Apex SOW / scoping template — what's the standard engagement scoping doc?**
- Why it matters: Apex is per-engagement; each needs clear scope, price, and boundaries.
- Status: Open

**H2 · Onboarding timeline and provisioning for an Apex engagement?**
- Why it matters: sets expectations for the first integration/agent.
- Draft list: Frontier handoff confirmed · Claude/third-party licensing · access to the target LOB system.
- Status: Open

**H3 · Client-facing Apex materials / cut-sheets?** *(marketing + delivery workstream)*
- Why it matters: sales enablement for the top-of-journey stage without over-promising (no outcome guarantees).
- Status: Open

---

## J. Custom AI-integrated web apps *(placeholder — on the radar, approach TBD)*

*Agents alone don't always carry a workflow. Some workflows need a purpose-built web app with AI inside — structured UI, forms, state, human-in-the-loop steps — to keep things moving. This is a distinct Apex capability that will take real R&D to define. Captured here so it stays on the radar.*

**J1 · Do we offer custom AI-integrated web apps as an Apex capability, and when do we raise it?**
- Why it matters: it's the answer when a chat agent can't support the workflow; but it's a much heavier build than an agent or integration.
- Likely trigger: at/after the Autonomous Agents stage (step 6 of the maturity journey), when a workflow clearly needs a real app, not a chatbot.
- Status: Open — *on the radar; not yet developed.*

**J2 · What's our build approach / tech stack / hosting model?**
- Why it matters: this is software development — we need a repeatable, supportable approach, not one-off bespoke builds.
- To define: stack, hosting, security review, how AI is embedded, who builds (PS/dev/partner), and the build-vs-maintain model.
- Status: Open — *significant R&D needed.*

**J3 · How is it scoped, priced, and supported over time?**
- Why it matters: custom apps carry ongoing maintenance, not just a one-time build.
- To define: SOW model, pricing, and who owns lifecycle/support after launch.
- Status: Open

---

## Decided
*Move items here as the group makes the call, with the date and the decision. Then update the Apex SOPs.*

| Ref | Decision | Date | Notes |
|---|---|---|---|
| | | | |
