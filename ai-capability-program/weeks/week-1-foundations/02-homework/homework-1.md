# Week 1 — Homework: Map the Stack
**Time:** ~3 hrs · **Due:** before the Week 2 session · **Hand in:** post to the Teams channel and bring a copy to Week 2, Hour 1.

> This is the **first advance on the one problem you carry through the whole program.** The agent spec you wrote in Hour 5 is the seed; this homework turns it into a clear plan across the AI stack. You'll *build* it in Week 2, harden it in Week 3, and deploy it in Week 4 — so pick the version of the problem that's genuinely worth four weeks of your time.

## What you're producing
A **2-page architecture document**: one real, complex problem from your function, decomposed across the AI Evolution Stack — showing which parts need a prompt alone, which need RAG, which need an agent, and (rarely) which need multi-agent.

It includes **3 production-quality prompts**, written and tested on Claude, for the LLM-only parts.

## Why it matters
An AI-capable leader's core judgement is *which layer a problem needs* — it decides cost, risk, and whether the thing works at all. This document is you making that judgement on a problem you own. It's also the brief your Week-2 build works from.

---

## Do it in four steps

**1 — Restate the problem (≈15 min).**
Start from your Hour-5 agent spec. In 3–4 sentences: what's the problem, who has it, what does "solved" look like? Choose for **organisational impact**, not just personal convenience.

**2 — Decompose across the stack (≈45 min).**
Break the problem into its parts. For each part, name the **lowest layer that solves it** and one line of *why not the layer above*:
- **LLM** — generate / rewrite / summarise text you supply.
- **RAG** — answer from *your own* documents, with sources.
- **Agent** — multi-step work that *takes actions* in tools and loops to a goal.
- **Multi-Agent** — coordinate several distinct specialised jobs (you likely won't need this — say so if you don't).

Use the decision lens from Preread 5. The rule stands: **the cheapest layer that works, wins.**

**3 — Write & test 3 prompts (≈60 min).**
For the LLM-only parts, write **3 production-quality prompts** using the anatomy from Hr 3 — *role · task · context · constraints · output format · examples.* **Run each on Claude, critique it against the anatomy, and improve it.** Paste the final version *and* one sentence on what you changed and why.

**4 — Spec the RAG and agent parts (≈30 min).**
You're not building these yet — just specifying. For each:
- **RAG part:** what documents would it draw on? What must it refuse to answer?
- **Agent part:** what's the goal, what steps/actions does it take, what data does it need, and **where does a human stay in the loop?** (Carry your Hr-4 data-sensitivity thinking through here.)

---

## Template (paste into a 2-page doc)

```
PROBLEM
  • One paragraph: the problem, who has it, what "solved" means.

STACK MAP
  Part of the problem        | Layer        | Why this layer, not the one above
  ---------------------------|--------------|-----------------------------------
  …                          | LLM/RAG/…    | …

THREE PROMPTS (LLM-only parts)  — tested on Claude
  1. [final prompt]   — changed: …
  2. [final prompt]   — changed: …
  3. [final prompt]   — changed: …

RAG SPEC
  • Source documents: …
  • Must refuse to answer when: …

AGENT SPEC
  • Goal: …
  • Steps / actions: 1) … 2) … 3) …
  • Data it needs: …
  • Human-in-the-loop at: …

DATA SENSITIVITY
  • Data in this problem that must NOT go into a public AI tool: …
```

## Your own quality bar (no grades — this is for you)
Capability shows in the artifact, not a score. Before you hand in, check:
- [ ] Every part of the problem is mapped to a layer, each with a *why-not-higher* reason.
- [ ] You resisted over-reaching — nothing is on a higher layer than it needs.
- [ ] All 3 prompts were **actually run on Claude** and improved, not just written.
- [ ] The agent part names where a **human stays in the loop**.
- [ ] It fits on **2 pages**. Concision is part of the skill.

## Stuck?
Blockers go to the **mid-week clinic** (~3 days after the session) or the **Teams doubt channel** — trainer responds within 1 business day. Don't burn an hour stuck; that's what the support layer is for.

## What this feeds
Week 2 opens (Hr 1) by critiquing these stack maps as a group, then you **build the agent part** as a no-code **Gem**. Bring this document — it's your build brief.
