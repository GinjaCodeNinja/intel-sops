# Pathfinder — AI Readiness Assessment SOP *(placeholder)*
## AI Discovery Journey · Pathfinder Stage (Foundation) · For the Pathfinder delivery lead

**Status:** Internal Working Draft v0.1 — **placeholder, to flesh out.** Points marked `⟨PENDING → Register §X⟩` / `⟨OPEN⟩` await the weekly group. No named owners.
**What this covers:** the **AI Readiness Assessment** — Pathfinder's first onboarding step. It is **included in signing up for Pathfinder, not a separate billable item** (decided). It's a mostly-automated readiness scan + report; the final deliverable is **leaner than the very original assessment plans — same assessment, just lighter.**
**Called from:** `NCA_Pathfinder_Onboarding_SOP.md` §3. Its output (the readiness report) is what the rest of onboarding runs on.

> **AvePoint note:** this uses the **scan/DSPM side** (Insights) to *feed the report.* It is distinct from the AvePoint **Workspace Management/Elements** governance config that runs the ongoing cleanup cycle (that's set up later in onboarding).

---

## 1. Purpose & boundary
- Produce a plain-language **AI Readiness report** that tells the client where they stand and shapes the rest of Pathfinder onboarding.
- Runs after the Kickoff (Onboarding Session 1) and before the Report Review (Onboarding Session 2).
- Not a standalone paid engagement, not a gate to a proposal — it's the front door of Pathfinder.

## 2. Preconditions
- Client signed up for Pathfinder; primary contact + exec sponsor confirmed.
- AvePoint subscription active on the tenant; scan access agreed.
- Kickoff done (the three questions framed, the Reflection Guide handed out — see Onboarding Session 1).

## 3. Run the scan
- **Set up AvePoint (DSPM / Insights)** on the tenant.
- **Let it run ~2 days** to collect: permissions & over-sharing, ROT/stale content, and M365 activity profiles.
- **Permissions realities to account for:** over-sharing often hides in **broken permission inheritance** (a library/folder with its own permissions) and **unique "anyone with the link" sharing links**, and access flows through **security groups**. **Treat the report as a lead, not gospel — verify reported permissions against the actual site + security-group config** before relying on them. ⟨reported ≠ actual; tool accuracy → Register §L4, §L5⟩
- ⟨OPEN: exact scan scope / which signals we pull.⟩

## 4. Generate the report
- **Run the Claude assessment process** to turn the scan (plus the Kickoff inputs) into a plain-language readiness report. *(reuse/extend `NCA_Assessment_Engine_POC_Prompt.md`.)*
- Keep it **lean** — findings a business owner can act on, not a heavyweight compliance document. ⟨OPEN: report template + how light.⟩

## 5. What the report surfaces *(this is what feeds onboarding)*
- **Governance gaps** — where ownership / source-of-truth / permissions are unclear.
- **"Who gets Copilot first"** — a suggested pilot cohort from the activity profiles.
- **Source-of-truth notes** — where authoritative copies do (and don't) live.
- **ROT / risk hotspots** — the messiest, highest-risk areas.
- **Scope inputs** — what's in M365 vs. held in other systems (feeds the Roadmap scope table).
- **Top 5–10 workspaces to start** — the highest-value/highest-signal workspaces to run first. Pathfinder does **not** try to clean every site at once; AI access stays **off by default** everywhere until each workspace is reviewed and signed off (governance posture set at Onboarding §7 / enforced in the Cleanup cycle). ⟨→ Register §L1, §D1⟩
- **Current Readiness Level (1–3)** — Level 3 is the activation target. ⟨Levels naming under review → Register §K⟩

## 6. Present the report
- Present it to the client — this *is* Onboarding **Session 2 (Report Review)**: reactions first, then a findings walk. See `NCA_Pathfinder_Onboarding_SOP.md`.
- Presenting the report **triggers Session 3 (Roadmap Planning)**, where scope, data owners, and the first workspaces get decided.

## 7. Handback to onboarding
- The report's findings flow into Roadmap Planning (scope table, Data Owner registry, first-workspace priority). Then onboarding hands the client to the **Cleanup & Activation Cycle SOP**.

## 8. Open items *(to flesh out)*
- Exact scan scope and signals; the Claude prompt/pipeline; the report template and its (lean) length; how much of the "who gets Copilot first" logic is automated vs. advised. ⟨scope → Register §A4⟩
