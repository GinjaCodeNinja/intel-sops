# Experiment Cards — The Pull-Menu
## AI Discovery Journey — Working Group Deck

**Status:** Internal Working Draft v0.1
**How to use:** The working group pulls a card whenever they want to try something. Pick by curiosity, time available, or what you want to learn. Most experiments are throwaways — that's the point. Log what landed (`NCA_Experiment_Log_Template.md`).

---

## Card format

Every card carries the same fields so the group can choose and self-assess without an NCI person in the room:

- **Category** — Create · Find & Recall · Analyze · Automate · Agent · Integrate
- **Level** — Explore (~15 min) · Build (~half-day) · Advanced (multi-session)
- **Track / stage** — Copilot cards carry the early journey (**Pathfinder/Outpost**); Claude and other third-party-AI cards are a **Frontier** capability; any unattended experiment is a **Frontier** evaluation
- **Prereqs** — tool/license needed, and **⚠ Gate** if it touches real company data or runs unattended
- **What it teaches** — the concept behind the activity
- **What "good" looks like** — how to tell it worked

---

## Starter deck

### C1 · Draft an image for a proposal
- **Category:** Create · **Level:** Explore · **Track:** Either
- **Prereqs:** Copilot/Designer or Claude; no real data → no gate
- **What it teaches:** how generative tools take direction, and where they're strong (concepts, diagrams-as-ideas) vs. weak (precise/technical accuracy).
- **What good looks like:** you produced a usable concept image and can describe *why* a second prompt got a better result.

### C2 · Find that thing you half-remember
- **Category:** Find & Recall · **Level:** Explore · **Track:** Copilot
- **Prereqs:** full Copilot license; touches real M365 data → **⚠ standard gate** (workspace signed off)
- **What it teaches:** Copilot as org memory — "what was the deck we made for the marina retaining-wall job last spring?"
- **What good looks like:** you found something in one query that would have taken 10 minutes of folder-digging.

### C3 · Turn a meeting into action items
- **Category:** Find & Recall · **Level:** Explore · **Track:** Copilot
- **Prereqs:** Copilot in Teams; internal meeting → **⚠ standard gate**
- **What it teaches:** summarization + extraction; how to prompt for *decisions and owners*, not just a transcript recap.
- **What good looks like:** the summary is accurate enough to send, and you caught a decision you'd have forgotten.

### C4 · Analyze a spreadsheet
- **Category:** Analyze · **Level:** Build · **Track:** Either
- **Prereqs:** Copilot in Excel, or Claude with an uploaded file; use a *non-sensitive* export first, real data → **⚠ standard gate**
- **What it teaches:** AI as an analyst — asking questions of data in plain language, and the discipline of *checking* what it claims.
- **What good looks like:** you got an insight you'd have missed, and you verified one number by hand before trusting it.

### C5 · Ask questions of a long document
- **Category:** Analyze · **Level:** Explore · **Track:** Claude **(Frontier)**
- **Prereqs:** Claude Project; upload a spec, contract, or standard → **⚠ standard gate** if real
- **What it teaches:** long-context reasoning; grounding answers in a specific source instead of general knowledge.
- **What good looks like:** you got a cited answer from *your* document, not a generic one.

### C6 · Build a simple Q&A agent
- **Category:** Agent · **Level:** Build · **Track:** Copilot
- **Prereqs:** Copilot Studio; point it at one clean, signed-off site → **⚠ standard gate**
- **What it teaches:** the anatomy of a declarative agent — instructions, a bounded knowledge source, and testing. Demystifies "agents."
- **What good looks like:** a colleague asked it a real policy/process question and got a correct, sourced answer.

### C7 · Write a reusable prompt for a recurring task
- **Category:** Automate · **Level:** Explore · **Track:** Either
- **Prereqs:** none; use a real-but-generic task
- **What it teaches:** the first step of automation — turning a repeated ad-hoc request into a reliable, shareable prompt.
- **What good looks like:** two different people ran the same prompt and got consistent, useful output.

### C8 · Deconstruct one real workflow
- **Category:** Automate · **Level:** Build · **Track:** Either
- **Prereqs:** the Workflow Deconstruction worksheet
- **What it teaches:** *the* core skill — breaking a task into steps and tagging each as rules / judgment / human (see the triage aid).
- **What good looks like:** you identified at least one step that's a candidate for automation and one that must stay human.

### C9 · Try an autonomous / "Co-work"-style task *(safe sandbox only)*
- **Category:** Agent · **Level:** Advanced · **Track:** Either **(Frontier — unattended)**
- **Prereqs:** sandbox environment, dummy data only → **⚠ heavier gate** — do not point at real data or real actions
- **What it teaches:** what unattended AI can and can't do reliably, and *why* the safety bar is higher when no one checks each step.
- **What good looks like:** you can answer two questions — could we run this safely, and is it actually useful enough to be worth governing?

### C10 · Compare Copilot vs Claude on the same task
- **Category:** Analyze · **Level:** Explore · **Track:** Copilot + Claude **(Frontier)**
- **Prereqs:** both tools
- **What it teaches:** the two tools have different strengths; choosing the right one is a skill.
- **What good looks like:** you can say which tool you'd reach for next time, and why.

---

## Adding cards
New cards come from two places: experiments the group invents (log them and formalize the winners), and the **Emerging Capabilities lane** — new features NCI evaluates, governs, and folds in (`NCA_New_Capability_Evaluation_Template.md`). The deck is meant to grow.
