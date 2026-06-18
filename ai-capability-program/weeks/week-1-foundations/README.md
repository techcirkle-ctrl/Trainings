# Week 1 — AI Foundations
### From ML to Multi-Agent — the conceptual map

**Objective:** Understand the full AI stack — LLM → RAG → Agents with tools → Multi-agent systems.

**Participant artifact:** A 2-page architecture document mapping **the one problem each leader carries through all four weeks** across the whole stack — scoped here, built (W2), hardened (W3), deployed (W4). Includes 3 tested prompts + an agent spec.

## The week at a glance

| Phase | ~Time | Where |
|---|---|---|
| Pre-work | ~2–3 hrs | [`00-preread/week-1-prework.html`](00-preread/week-1-prework.html) — one interactive file, 6 sections |
| Session | 5 hrs | 3 projectable decks + 1 hands-on helper (see below) — 13 movements |
| Homework | ~3 hrs | [`02-homework/homework-1.md`](02-homework/homework-1.md) |

## Session outline (5 hrs, trainer-led)

1. **Pre-work debrief + LLMs deeper** — level-set AI/ML/GenAI/LLM; transformers, attention, context windows, model selection (Claude family).
2. **The AI Evolution Stack** — LLM → RAG → Agents with tools → Multi-agent. The backbone of the program.
3. **Prompt engineering masterclass** — systematic prompt design; hands-on, 3 prompts per participant on Claude.
4. **RAG deep dive** — how retrieval-augmented generation works; live demo with a Claude Project on sample docs.
5. **Concept of agents** — agent vs chatbot; each participant writes a 1-paragraph agent spec for Week 2.

> **Session delivery is 3 projectable decks + 1 circulated hands-on helper** (see ADR 0002). The trainer projects the decks (concept movements, with the prework's widgets driven live); leaders open `hands-on-movements.md` on their laptops to copy the prompts for the hands-on movements. It re-teaches from zero (no dependence on prework). Every movement shares one shape: **goal → do → judgment.** The unit across both is the **movement** (M1–M13).
>
> | File | Movements | What |
> |---|---|---|
> | [`deck-1-fundamentals.html`](01-workshop/deck-1-fundamentals.html) | M1–M5 | engine predicts · inside the model · the stack · *(M4–M5 bridge to the helper)* |
> | [`deck-2-prompting.html`](01-workshop/deck-2-prompting.html) | M6–M9 | prompt anatomy · *(M7–M8 hands-on)* · patterns & failure modes |
> | [`deck-3-rag-agents.html`](01-workshop/deck-3-rag-agents.html) | M10–M13 | RAG on/off · data-rule sorter · agent loop · *(M13 hands-on)* |
> | [`hands-on-movements.md`](01-workshop/hands-on-movements.md) | M4·M5·M7·M8·M11·M13 | the circulated copy-paste working sheet |
>
> Concept movements live in the decks; hands-on movements live in the helper (bridged from each deck). `run-of-show.md` and `facilitator-room-kit.md` are retained as background source and retired once fully absorbed. Week 1 is the de-facto template for Weeks 2–4. Formats: `.claude/skills/teach/DECK-FORMAT.md` (decks + helper) · `LESSON-FORMAT.md` (prework).
