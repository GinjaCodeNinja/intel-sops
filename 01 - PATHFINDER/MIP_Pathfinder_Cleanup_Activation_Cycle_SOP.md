# Pathfinder — Cleanup & Activation Cycle SOP *(placeholder)*
## AI Discovery Journey · Pathfinder Stage (Foundation) · For the Pathfinder delivery lead

**Status:** Internal Working Draft v0.1 — **placeholder.** EOS-style (20/80, point form). Points marked `⟨PENDING → Register §X⟩` await the weekly group — see `NCA_Pathfinder_Open_Decisions.md`.
**What this covers:** the **ongoing, post-onboarding work** — the rolling workspace **cleanup → sign-off → Copilot indexing** cycle, plus incremental Copilot activation. (The assessment + governance setup happen first, in `NCA_Pathfinder_Onboarding_SOP.md`.)
**Delivery role:** role-neutral "Pathfinder delivery lead" ⟨PENDING → Register §B1⟩. **Pathfinder is a governance managed-service, not a consulting engagement** — there is no AI-Expert monthly session (that's Outpost).
**Assumes onboarding is complete** — see `NCA_Pathfinder_Onboarding_SOP.md` (assessment presented, Data Owners in place, AUP signed, AvePoint governance configured, pilot users licensed, first workspace picked).
**One-line job:** run the workspace cleanup cycle so Copilot has clean, governed data to stand on — and activate Copilot for first users as each workspace is signed off.

---

## 1. The Pathfinder cycle *(the core loop — rolling, never "done")*
Repeats across workspaces (Sales, Finance, HR, Operations, projects…). One workspace at a time; a sign-off unlocks Copilot on *that* workspace while cleanup continues elsewhere. *(= framework milestone B3; matches the Pathfinder one-pager's 4-node cycle.)*

> **Default-OFF posture:** AI access starts **off for every workspace** (Restricted Content Discovery off across all sites — set at Onboarding §7). The cycle is what turns it **on**, one signed-off workspace at a time. This is tool-agnostic — RCD also gates Claude / ChatGPT / enterprise search, not just Copilot. ⟨toggling at scale needs a tool, PowerShell-only today → Register §L1, §L2⟩

1. **SELECT** the next workspace — start with the **top 5–10 high-value** ones, not every site. ⟨prioritization → Register §D1⟩
2. **REVIEW & clean up** — the Data Owner works the **Workspace Review Checklist** (`NCA_Workspace_Review_Checklist.md`): confirm purpose/access, find the source of truth, clear ROT/superseded files, and decide clean / archive / exclude-from-AI. ⟨delete vs archive → Register §D2, §L10⟩
3. **SIGN-OFF** — the Data Owner attests the workspace is current, correctly permissioned, and safe. ⟨what sign-off attests → Register §D3⟩
4. **ENABLE** — **lift the AI-access restriction (RCD) for the signed-off workspace, and record the decision** (who approved, when) as an audit trail; Copilot indexing follows for that workspace. ⟨→ Register §L1⟩
5. **Repeat.** Track pace. ⟨cycles per period → Register §D4⟩

## 2. Data quality on the way through
- Remove redundant/outdated/trivial (ROT) content; retire stale files. A useful starting filter: **files not opened in ~4 years.**
- For version sprawl (`…v1/v2/v3`), use a **non-indexed "versions archive" folder** so history stays available but is invisible to Copilot/search.
- **Heavily cluttered workspace?** Rather than sort a swamp in place, **stand up a new clean site, move only the good/organized data into it, and leave the old site as a non-indexed archive.** Often the faster path to a trustworthy result.
- **Working vs. published data:** where a workspace mixes rough working files with finished/authoritative ones, consider **separating them at the site/library level** so AI sees only the clean, published set (SharePoint controls AI access at that level, not per file).
- **Retiring a Teams/group workspace? Archive — don't delete.** Deleting an M365 group can destroy channel conversation history; **archive the channels/site** instead (and note some groups carry deletion restrictions, e.g. Viva Engage). ⟨→ Register §L8⟩
- Delete-vs-archive is the **Data Owner's call**, with our guidance — **archive by default; delete only once a backup is confirmed.** ⟨→ Register §D2, §L10⟩

## 3. Copilot activation & basic support
- **Activate incrementally:** enable pilot users on each workspace as it signs off — value builds cycle by cycle, not in one go.
- **Basic Copilot Chat support:** prompt help and day-to-day questions. ⟨included vs excluded → Register §E4⟩ Not included: agent dev, workflow consulting, Claude/third-party (Outpost/Frontier).
- **Light user enablement** for first users. ⟨reuse Stage 1 Kickstart? → Register §E3⟩
- **Sharpen relevance (Copilot):** on a signed-off workspace, **mark the authoritative library** and use a simple **Status metadata column** (Current / Superseded / Draft) so Copilot prioritizes the right documents. *(Copilot-specific — this tuning doesn't apply to Claude.)* ⟨granular metadata control → Register §L6⟩

## 4. AvePoint health monitoring
- Keep workspace health/automation running (AvePoint Elements does the heavy lifting).
- Watch for new risk/ROT/over-sharing surfaced over time. ⟨who watches, cadence → Register §F1, §F2⟩
- **Permission-report caveat:** the report can miss the real state — verify against the **actual site + security-group config**, broken inheritance, and unique sharing links; library-level (granular) views are weak in the tool today. ⟨→ Register §L4, §L5⟩

## 5. Cadence & client touchpoints
- Whether Pathfinder has a scheduled check-in or is purely managed-service + reactive is ⟨PENDING → Register §B2⟩.
- Working assumption: a **light monthly progress review** (keeps exec buy-in during cleanup months).

## 6. Progress reporting *(beat the "unglamorous months" risk)*
- The program's known failure mode is losing exec buy-in during cleanup. Counter it: each period, show **workspaces signed off** and **value unlocked** (e.g., "the estimating team's site is clean and live — Copilot now surfaces current specs, not old versions"). ⟨format → Register §G1⟩
- Use outcome language, not task counts.

## 7. Watch for Outpost-readiness *(the "earned" trigger)*
- Signals: enough workspaces signed off, active/eager Copilot use, exec engaged, appetite for agents/automation.
- Raise the Pathfinder→Outpost conversation when they show. ⟨signals & who raises → Register §G2 — keep aligned with Outpost register B1⟩

## 8. Tracking
- Keep the **B3 sign-off log** current in the readiness tracker (`NCA_Data_Process_Readiness_Tracker.md`) — signed-off workspaces, Data Owners, dates, indexing enabled. ⟨who updates → Register §G3⟩
- Record notes in the client record (IT Glue / SharePoint list / spreadsheet for now).

## 9. Boundaries (consult-construct do / don't)
- **Do:** run the cycle, advise on cleanup/governance, process sign-offs, enable indexing, basic Copilot help.
- **Don't:** make the client's ownership/deletion decisions for them, build agents, deliver workflow consulting or Claude/third-party work (those are Outpost/Frontier), or guarantee outcomes.

## 10. Roles, coverage & escalation
- Who processes sign-offs / enables indexing ⟨→ Register §B3⟩; capacity per delivery person ⟨→ Register §H1⟩; coverage + escalation ⟨→ Register §H2⟩.

## 11. Exit / graduation to Outpost
- When Outpost-readiness signals hold (§7), hand to the **Outpost onboarding** (`NCA_Outpost_Onboarding_SOP.md`). Pathfinder's foundation work continues underneath — nothing turns off.

## 12. Open decisions index
- Points marked `⟨PENDING⟩` map to `NCA_Pathfinder_Open_Decisions.md`. As the group decides, update this SOP and drop the flag.
