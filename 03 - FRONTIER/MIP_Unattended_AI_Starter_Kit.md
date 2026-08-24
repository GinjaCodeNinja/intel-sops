# Unattended / Autonomous AI — Starter Kit
## AI Discovery Journey — Frontier · Heavier Gate

> **STATUS: PLACEHOLDER — to be developed.**
> This scaffold captures the intent and structure. Flesh it out once we've sandboxed a "Co-work"-class autonomous tool ourselves and know the real governance surface. Do not use with a client until developed and reviewed.

**Purpose:** Give a client a safe way to try unattended AI — tools that act across multiple steps without a person checking each one — and a clear-eyed way to decide whether it's actually useful to them. Built for the posture a real client described: *"try it out safely and figure out how, if at all, it could be useful."*

**Why this needs its own kit:** attended AI has a human as the last check on every output. Unattended AI doesn't — errors compound before anyone notices. The bar for letting it touch real data or take real actions is materially higher.

---

## The two questions, in order

We help the client answer these in sequence. Most autonomous tools should fail cheaply at Q1 or Q2 in a sandbox — reaching a confident "not yet" is a good, cheap outcome.

1. **Can we run this safely in a contained way?** (sandbox, dummy data, no real actions)
2. **Is it actually useful enough to be worth governing for real?**

---

## Part A — Safe sandbox setup  *(TODO: develop)*
- [ ] Isolated environment / test tenant or project
- [ ] Dummy or fully non-sensitive data only
- [ ] No connection to production systems or real actions (email send, file delete, payments, etc.)
- [ ] Defined, bounded scope of what the tool may touch
- [ ] A clear "how to stop it" / kill switch understood before starting
- [ ] _...specifics per tool once evaluated_

## Part B — Usefulness rubric  *(TODO: develop)*
- What task did it attempt autonomously?
- How often did it succeed without intervention?
- What did it get wrong, and how bad would that have been on real data?
- Did it save meaningful time/effort vs. an attended approach?
- Verdict: worth governing for real? / not yet / no

## Part C — Governance checklist before any real use (the heavier gate)  *(TODO: expand)*
- [ ] Bounded, written scope of what it can touch and do
- [ ] Named human owner accountable for its actions
- [ ] Kill switch / how to stop it
- [ ] Monitoring so a failure is actually noticed
- [ ] Written "what could go wrong + blast radius" note
- [ ] Data access follows Stage 2 governance (signed-off workspaces only)
- [ ] Ties to Claude safe-configuration where relevant (Stage 2 governance)

## Part D — Where it's likely useful for an engineering / project firm  *(TODO: research with client)*
_Placeholder for domain-specific candidate uses — the client's working group are the domain experts and will surface these. Capture and evaluate rather than prescribe._

---

## Dependencies before developing this kit
- Hands-on evaluation of at least one "Co-work"-class tool via the New Capability Evaluation flow.
- Confirmation of the Claude safe-configuration checklist location in Stage 2 governance.
- Alignment with the MI Model AI Operations & Optimization component (governs autonomous systems) — feed into Decision 5.
