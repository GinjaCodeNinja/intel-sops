# Third-Party Platform & Integration Inventory
## Rail B · Milestones B5–B6 — AI Discovery Journey

**Status:** Internal Working Draft v0.1
**Purpose:** Catalogue the third-party / line-of-business platforms that hold a client's business data, decide which ones AI may need to reach, and triage *how* each could connect. This is where the "can AI use the data in our other systems?" question gets a concrete, per-app answer — and it feeds Rail A's Extend & Orchestrate stage (A6) and the third-party-AI-access governance conversation.

**How to use:** Fill Part 1 broadly (catalogue everything that holds business data). Then, only for the apps flagged "AI-relevant," complete Part 2 (connection triage). Don't triage integrations nobody needs.

---

## Part 1 — Platform inventory

| Platform / app | What it's used for | Data it holds | Who owns it | AI may need it? | Sensitivity |
|---|---|---|---|---|---|
| _(e.g. project management tool)_ | | | | High / Med / Low / No | Low / Med / High |
| | | | | | |
| | | | | | |
| | | | | | |

**AI-relevance test:** would answering a real question or automating a real task require this system's data? If no, it stays in the inventory for governance visibility but skips the triage below.

---

## Part 2 — Connection triage *(AI-relevant apps only)*

For each app AI needs, work down the options in rough order of preference and record the verdict.

| Platform | Native integration? | MCP server? | Public API? | Chosen path | Who approves access | Governance / consent notes | Verdict |
|---|---|---|---|---|---|---|---|
| | ☐ Copilot ☐ Claude ☐ none | ☐ vendor ☐ community ☐ none | ☐ yes ☐ no | native / MCP / API / build / **none yet** | | | ready / needs work / not feasible yet |
| | | | | | | | |
| | | | | | | | |

### How to read the connection options (best-to-heaviest)
1. **Native integration** — the app has an official Copilot and/or Claude connector. Lowest effort, best-governed. *Prefer this when it exists.*
2. **MCP server** — a Model Context Protocol server (vendor-published or reputable community) exposes the app to Claude/agents. Good option; check who maintains it and what it exposes.
3. **Public API** — the app has an API we could connect to with a custom build. More effort; an Apex engagement.
4. **None yet** — no clean path today. Log it, park it, and let the Emerging Capabilities lane catch it if a connector ships later. A perfectly valid "not now."

### Governance & consent — always, regardless of path
- **Who approves** the connection to company data (should route to an admin, not any user — ties to the third-party app-consent governance).
- **What data** the connection can reach, and whether that's scoped appropriately.
- **Attended or unattended** use on the far side — unattended triggers the heavier gate.
- **Whether it leaves the M365 boundary** — note it explicitly (e.g. data flowing to a third-party AI service).

---

## Roll-up for the journey
- **Apps catalogued:** ___  · **AI-relevant:** ___  · **Ready to connect:** ___  · **Parked (no path yet):** ___
- **Highest-value integration to pursue next:** _____________
- **Anything that needs a governance decision before proceeding:** _____________

> This inventory is a living document. Revisit it when the client adopts a new platform, or when the Emerging Capabilities lane surfaces a new connector for something previously parked.
