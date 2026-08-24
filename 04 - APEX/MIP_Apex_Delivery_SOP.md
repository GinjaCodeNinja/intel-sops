# Apex — Delivery SOP *(placeholder)*
## AI Discovery Journey · Apex Stage (Custom Build & Optimization) · For the AI Expert + build team

**Status:** Internal Working Draft v0.1 — **placeholder.** EOS-style (20/80, point form). Points marked `⟨PENDING → Register §X⟩` await the weekly group — see `NCA_Apex_Open_Decisions.md`.
**Delivery team:** AI Expert designs/advises; build resource (PS/dev) builds. ⟨model → Register §B1⟩
**Assumes onboarding is complete** — see `NCA_Apex_Onboarding_SOP.md` (Frontier handoff confirmed: integration map done, Claude/third-party configured, autonomous-agent governance stood up, first engagement scoped).
**Three things run at once in Apex:** (1) **engagements** — scoped builds (integrations, custom/autonomous agents, and **custom AI-integrated web apps** — placeholder), delivered per initiative; (2) **operations** — the ongoing managed digital workforce (monitoring, lifecycle) for everything already deployed; and (3) **ongoing optimization & roadmap planning** — a standing review of what's live and what's next. All sit **on top of a continuing Outpost + Frontier base.**

---

## 1. The engagement loop *(per initiative)*
Each Apex initiative — an integration, a custom/autonomous agent, or a **custom AI-integrated web app** *(placeholder — approach TBD; see Open Decisions §J)* — runs this loop:
1. **Scope** — confirm outcome, boundaries, price, approver (SOW). ⟨template → Register §I1⟩
2. **Design** — the AI Expert designs; client approves. Consult-construct.
3. **Build** — the build resource builds the integration/agent. ⟨who builds → Register §B1⟩
4. **Gate** — run the **appropriate governance gate** before it touches real data/actions:
   - Attended → standard gate.
   - **Unattended/autonomous → heavier gate** (bounded scope · named owner · kill switch · monitoring · blast-radius note · signed-off data only) — using the gate Frontier stood up. *(framework §9; `NCA_Unattended_AI_Starter_Kit.md`.)* ⟨→ Register §D1⟩
5. **Deploy** — release to production; register it (§3).
6. **Verify & hand over** — confirm it works; confirm the client owner understands and accepts accountability. ⟨owner → Register §D4⟩

## 2. Integration work (MCP / API / native)
- Work from the **Third-Party Integration Inventory** triage completed at Frontier. *(reuse `NCA_ThirdParty_Integration_Inventory.md`.)*
- Vet connectors: native → vetted vendor MCP → reputable community → custom; **security review before real data.** ⟨→ Register §C2⟩
- Confirm the **consent/approval** for AI reaching each system, and document the data flow (esp. data leaving the M365 boundary). ⟨→ Register §C3⟩

## 3. Managed digital workforce *(ongoing operations)*
- Keep an **agent/integration registry** — what's live, what it touches, who owns it. ⟨owner → Register §F3; where → §G2⟩
- **Monitor** deployed agents/integrations; watch for drift, failures, and degradation. ⟨tooling → Register §D2; cadence → §F1⟩
- **Failure response:** alert → defined response → **kill switch** if needed → root-cause + fix. ⟨→ Register §F2, §H1⟩
- **Lifecycle:** review, update, or retire agents as the business changes.

## 4. Ongoing optimization & roadmap planning *(standing thread — not one-off)*
- On the cadence agreed in Onboarding §5: review what's live, what's underused, what needs tuning, and what the client should build next.
- Feeds the client's roadmap the same way the Experiment Log feeds Outpost's ROI story. ⟨format → Register §F2⟩

## 5. Unattended / "Co-work"-class AI
- Uses the heavier gate stood up at Frontier: sandbox-first (dummy data, no real actions) → usefulness rubric ("useful enough to govern?") → real use. *(reuse `NCA_Unattended_AI_Starter_Kit.md` — placeholder.)* ⟨→ Register §D3⟩
- Many autonomous tools should fail the usefulness test cheaply in the sandbox — that's a good, cheap outcome.

## 6. Claude & third-party AI
- Uses the **Claude safe-config** Frontier put in place (Stage 2 governance). ⟨→ Register §E1⟩
- Support scope for Claude / ChatGPT / xAI and Copilot Studio per what's agreed. ⟨→ Register §E3⟩

## 7. Emerging capabilities
- New connectors/agents/features flow through the **New Capability Evaluation** (sandbox → govern → adopt/park/reject). *(reuse `NCA_New_Capability_Evaluation_Template.md`.)* Survivors become candidate engagements.

## 8. Progress & reporting
- Per-engagement **outcome report** (what it does, value delivered, what changed for the client). ⟨format → Register §G1⟩
- Ongoing operations status for the deployed workforce (health, incidents) + the optimization/roadmap review. Outcome language.

## 9. The Outpost + Frontier base continues
- Apex is additive: the **Outpost** monthly hour, declarative-agent support, and Frontier's tool-graduation/governance groundwork keep running underneath. Don't let an Apex build eclipse that momentum.

## 10. Boundaries (consult-construct do / don't)
- **Do:** design, build, integrate, govern, monitor, advise, de-risk, optimize.
- **Don't:** own the client's business decisions, approve production autonomy on their behalf, or guarantee outcomes/performance. A named **client** owner is accountable for each production agent's actions.

## 11. Roles, coverage & escalation
- Build resourcing & capacity ⟨→ Register §B2, §H2⟩; production failure coverage/escalation ⟨→ Register §H1⟩ — higher stakes than Outpost: a broken production integration/agent can affect live operations.

## 12. Exit / steady state
- Apex has no "graduation up" — it's the top of the journey. Steady state = a growing, well-governed digital workforce operating reliably, plus a standing optimization/roadmap rhythm, with the Frontier, Outpost, and Pathfinder foundations intact beneath it.
- North star: *"our technology partner doesn't just manage our IT — they manage our intelligence infrastructure."*

## 13. Open decisions index
- Points marked `⟨PENDING⟩` map to `NCA_Apex_Open_Decisions.md`. As the group decides, update this SOP and drop the flag.
