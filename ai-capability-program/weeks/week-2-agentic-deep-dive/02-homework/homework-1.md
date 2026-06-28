# Week 2 — Homework: Build Your Agent (v1) + the Design Doc
**Time:** ~3 hrs · **Due:** before the Week 3 session · **Hand in:** post to the Teams channel and bring a copy to Week 3, Hour 1.

> This is the **second advance on the one problem you carry through the whole program.** In Week 1 you spec'd it; in today's session you learned the mechanics by building a *ready-made* agent. Now you run that exact loop on **your own** problem — the one from your Week-1 architecture doc. You'll harden it in Week 3 and deploy it in Week 4, so build the version that's genuinely worth four weeks of your time.

## What you're producing
Two things:
1. **A working v1 agent** — your own problem, built as a **Claude Project** (instructions + knowledge), tested on real inputs. Same mechanic you used on the ready-made agent in the session.
2. **A 1-page design doc**, shaped like the agent lifecycle you saw today — **design → build → test → deploy → monitor** — that states the goal, the least-autonomy choice, where the human checkpoint sits, and what you found when you tested it.

## Why it matters
The judgement you're paid for isn't operating an agent — it's **sponsoring** one: choosing the least autonomy that works, deciding what it may touch, and owning the human checkpoint. This doc is you making those calls on a problem you own. It's also the brief your **Week-3 hardening** works from.

---

## Do it in four steps

**1 — Restate the problem and choose the pattern (≈20 min).**
Start from your Week-1 architecture doc — the **agent part**. In 3–4 sentences: what's the goal (an outcome, not a question), who has it, what does "done" look like? Then name the **least-autonomous pattern that solves it** (chaining · routing · parallel · ReAct · plan-and-execute · reflection), and one line on **why not the pattern to its left**. The rule from today: *the least autonomy that works, wins.*

**2 — Build it as a Claude Project (≈60 min).**
Repeat the session mechanic on your own problem:
- **Instructions** — role · the loop it runs · guardrails · the **stopping rule** · the **human checkpoint** line.
- **Knowledge** — the standard, rubric, or reference documents it must reason from.
- (No tools wired — in no-code, *you* are the tool: you paste the input. The loop, grounding and checkpoint are all real.)

**3 — Test it on real inputs, including the awkward one (≈40 min).**
Run **at least three** real inputs — and make one of them **deliberately awkward** (a missing field, an off-topic case, an un-owned decision). The real test: does it **flag and refuse to guess**, or does it hallucinate? Note what broke.

**4 — Write the 1-page design doc (≈40 min).**
Fill the template below. Keep it to **one page** — concision is part of the skill.

---

## Template (paste into a 1-page doc)

```
AGENT: [name]                                            OWNER: [you]

DESIGN
  • Goal (an outcome, not a question): …
  • Least-autonomy pattern chosen: …  — why not the one to its left: …
  • Human checkpoint sits at: …
  • Data that must NOT go near a public AI tool: …

BUILD
  • Instructions (role · loop · guardrails · stopping rule · checkpoint): [link or paste]
  • Knowledge it reasons from: …
  • Claude Project link: …

TEST  (≥3 inputs, one deliberately awkward)
  Input            | What it did            | Held up? / How it failed
  -----------------|------------------------|--------------------------
  1 (clean)        | …                      | …
  2 (clean)        | …                      | …
  3 (awkward)      | …                      | flagged / hallucinated?

DEPLOY (plan — not done yet)
  • First small slice it would run on (one user / one work-type): …

MONITOR (plan — not done yet)
  • What you'd watch over time (cost · drift · errors): …
  • Where the human checkpoint stays live: …
```

## Your own quality bar (no grades — this is for you)
Capability shows in the artifact, not a score. Before you hand in, check:
- [ ] The goal is **outcome-shaped**, not a chatbot question.
- [ ] You chose the **least autonomy that works** — with a *why-not-higher* line.
- [ ] The instructions carry a **stopping rule** *and* a **human checkpoint**.
- [ ] You ran **≥3 real inputs**, one deliberately awkward, and recorded what broke.
- [ ] The agent **refuses to invent** on the awkward input (or you noted that it didn't).
- [ ] It fits on **one page**.

## Stuck?
Blockers go to the **mid-week clinic** (~3 days after the session) or the **Teams doubt channel** — trainer responds within 1 business day. Don't burn an hour stuck; that's what the support layer is for.

## What this feeds
Week 3 opens by **hardening these agents**: stress-testing the failure modes you found, tightening the guardrails and the checkpoint, and moving from a v1 to something robust enough to deploy. Bring this design doc — it's your hardening brief.
