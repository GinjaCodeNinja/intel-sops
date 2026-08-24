# Workspace Review Checklist
## Reviewing one workspace before AI is switched on

**Status:** Internal Working Draft v0.1 — from the AvePoint field test; refine with data-owner feedback as we run it.
**Who it's for:** a **Data Owner**, working with NCI, reviewing **one** SharePoint site / Teams workspace.
**The job:** decide, for this workspace, whether to **clean it up · archive it · or exclude it from AI** — then sign off.
**Pairs with:** the Data Owner Role (`NCA_Data_Owner_Role.md`) and the Cleanup & Activation Cycle SOP's REVIEW → SIGN-OFF → ENABLE loop.

> **Start here:** AI access is **off** for this workspace until you sign off. Nothing you review here is exposed to Copilot (or Claude / ChatGPT / search) while it's off. Take your time.

---

## The 10-point review

1. **What is this workspace for — and is it still active?**
   Name its purpose in a sentence. If it's dead/abandoned, the answer may simply be *archive it and exclude from AI* — skip to step 9.

2. **Who should have access — and does the current access match?**
   Compare who *should* see this with who *can*. Watch the three things that quietly widen access: **old "anyone with the link" sharing links**, **broken permission inheritance** (a library or folder with its own permissions), and **security-group membership** (people inherit access through a group). If the picture looks wrong, flag it — the automated report doesn't always show the real state.

3. **Is there one authoritative version — or duplicates and old copies?**
   If the same thing exists in three places, decide which one is the source of truth. Copilot can't tell which copy you trust unless the environment makes it clear.

4. **Old files — archive or delete?**
   A practical starting filter: **files not opened in ~4 years.** Archive what's no longer relevant; keep what still matters. **Delete only after confirming a backup exists.** When in doubt, archive rather than delete.

5. **Is there sensitive or restricted content that should be excluded from AI entirely?**
   Some content shouldn't be in scope for AI at all (regardless of cleanup). Mark the workspace — or a specific library — to **stay excluded**.

6. **Working data vs. published data — should they be separated?**
   If a workspace mixes rough/working files with finished/authoritative ones, consider splitting them so AI sees only the **clean, published** set. This is a site/library-level decision (SharePoint controls AI access at that level, not per-file).

7. **Is the content current and accurate enough to trust AI answers on it?**
   AI will confidently repeat whatever it finds. If the workspace is full of stale or contradictory material, it isn't ready — clean first.

8. **Sharpen relevance (Copilot):**
   Once it's clean, **mark the authoritative library** and use a simple **Status metadata column** (e.g., *Current / Superseded / Draft*) so Copilot prioritizes the right documents. *(This tuning helps Copilot specifically; it doesn't apply to Claude.)*

9. **Make the call for this workspace:**
   - **Clean up in place** — fix access, remove/retire ROT, then sign off.
   - **Move clean data to a new site** — bring only the good, organized data forward; leave the old site as a **non-indexed archive**.
   - **Exclude from AI for now** — leave AI off until it's ready (or permanently, for sensitive areas).

10. **Sign off → NCI enables AI access (recorded).**
    Your sign-off attests the workspace is current, correctly permissioned, and safe. NCI validates, then **lifts the AI-access restriction for this workspace only — and records the decision** (what was approved, by whom, when). That audit trail is part of the governance model.

---

*Draft note: this checklist came out of NCI's first hands-on run of the AvePoint/permissions process. Expect it to tighten as real data owners use it — capture what confuses or frustrates them and feed it back here. Several supporting questions (permission-report accuracy, granular library views, non-Copilot AI scoping) are open items in `NCA_Pathfinder_Open_Decisions.md` §L.*
