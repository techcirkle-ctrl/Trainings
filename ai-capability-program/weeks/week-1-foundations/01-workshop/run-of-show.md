# Week 1 — Run of Show
### AI Foundations · 5 hrs, trainer-led · in person

> Facilitator script. The session is **flipped**: every hour builds on the five prereads, and **Hour 1 opens by consuming their outputs** — the trust/not-trust call (P1), the blocking LLM-limit (P2), the data-sensitivity input (P3), the agent-shaped task (P4), and the workflow→layer mapping (P5). Each leader pasted these into the Teams channel before the session; have them open in front of you.
>
> **The depth move, every hour:** trainer demos the technical internals live in **Claude Code (run as a Claude Project — the program's build engine)**; leaders touch the *outputs*, not the terminal. The no-code build surface leaders will use from Week 2 is **Gems**. Week 1 is Understand — concepts, prompting, and the first connected project — so the build itself is light here.
>
> **Materials to prep:** slides per hour; the prereads open for reference; a shared Claude workspace with leader access provisioned (Week 0); a sample-docs pack for the RAG demo (non-sensitive); the Stack one-pager (from `reference/glossary.html`); printed copies of the Week-1 homework brief.

**Objective:** every leader leaves able to (1) place any problem on the AI Evolution Stack, (2) write a production-quality prompt, (3) explain what RAG and an agent add — and (4) walk out with a **one-paragraph agent spec for the single problem they carry through all four weeks.**

---

## Hr 1 — Pre-work debrief + LLMs, deeper
**Goal of the hour:** close the flipped loop, level-set the cohort, and surface the real problems leaders brought.

**Opens with the prereads (0:00–0:25) — this is non-negotiable.**
- Round the room on **Preread 5**: each leader reads their *workflow → lowest layer → why not the layer above*. Capture all five on a visible board under LLM / RAG / Agent / Multi-Agent. (This board stays up all day — every later hour points back to it.)
- Pull in **Preread 1** (trust / don't-trust) and **Preread 2** (the limit that blocks a task) as you go — they explain *why* each problem sits where it does.
- Park **Preread 3** outputs (data sensitivity) for Hr 4, and **Preread 4** outputs (agent-shaped task) for Hr 5. Tell them you're parking these, so they know they'll be used.

**Talk track (0:25–0:55):**
- Level-set the vocabulary the half-day workshop left them with: AI / ML / GenAI / LLM — one clean slide, no dwelling. Most of this was the prereads; confirm, don't re-teach.
- Go one level deeper than the prereads on the engine: **transformers & attention** at a leader's altitude (the model weighs which earlier words matter most when predicting the next), **context window** as working memory, and **why outputs vary**.
- **Model selection — the Claude family.** When to reach for a faster/cheaper model vs. the most capable one; cost/speed/capability trade-off. Frame it as a leadership decision, not an engineering one.

**Output of the hour:** the populated Stack board — the cohort's real problems, mapped. Photograph it.

---

## Hr 2 — The AI Evolution Stack
**Goal of the hour:** make the stack the permanent mental model of the program. This is the backbone everything else hangs on.

**Talk track (0:00–0:35):**
- Walk the four rungs from Preread 5, but now *live* and with the cohort's own board from Hr 1. For each rung: what it adds, the ceiling it hits, the example already on the board.
- Hammer the rule of thumb: **the cheapest layer that works, wins.** Climbing too high is the most common and most expensive mistake — name it now so it governs every build decision in Weeks 2–4.

**Demo (0:35–0:55) — the depth move:**
- In **Claude Code**, show the same simple task solved at two layers: a plain prompt vs. the same task grounded in a document. Leaders see the *difference in behaviour*, not the code. Point out: "you'll build the no-code version of this in a Gem from next week."

**Exercise (0:55–1:00):** each leader re-confirms or *moves* their problem on the board now that they've seen the rungs live. Movement is the point — it means the model is landing.

**Output of the hour:** a settled layer assignment for each leader's problem (feeds Hr 5 and the homework).

---

## Hr 3 — Prompt engineering masterclass
**Goal of the hour:** the highest-leverage skill — turn a vague ask into a reliable, reusable prompt. Hands-on.

**Talk track (0:00–0:20):**
- The anatomy of a production prompt: **role · task · context · constraints · output format · examples.** One slide, one worked example built live.
- Why structure beats cleverness: the model continues from what you give it, so specificity is control. (Ties back to Preread 2.)
- Preview that the full systematic guide is Week 3's deep dive — today is the working subset.

**Hands-on (0:20–0:55) — 3 prompts per leader, on Claude:**
- Each leader writes **3 prompts for the LLM-only parts of their own problem** (the parts they mapped to Layer 1 on the board).
- Iterate live: draft → run → critique against the anatomy → improve. Trainer circulates; pair leaders to critique each other's.
- Bank these — they become part of the Week-1 homework (the 3 production prompts) and seed the Week-2 build.

**Output of the hour:** 3 working, critiqued prompts per leader, saved to their workspace.

---

## Hr 4 — RAG deep dive
**Goal of the hour:** make "ground it in our own documents" concrete — and connect it to responsible use.

**Open with Preread 3 (0:00–0:10):** round on the *data-sensitivity* inputs leaders brought. Build a shared first-draft list: **what data can / can't go into an AI tool.** This is the leaders' contribution to Sandvik's Week-0 data rule — capture it; it's a real artifact, not a warm-up.

**Talk track (0:10–0:30):**
- How RAG works at a leader's altitude: retrieve the relevant pieces of *your* content at question time → hand them to the model → grounded answer **with sources**. Contrast with the LLM-alone failure mode from Preread 1 (confident and wrong).
- When RAG is the right layer and when it isn't (no actions taken — that's the agent's job).

**Demo (0:30–0:55) — the depth move:**
- Trainer builds a **connected Claude Project** over the non-sensitive sample-docs pack, live. Ask it a question; show the grounded, cited answer; then show it refusing/flagging when the answer isn't in the docs.
- Name the tooling explicitly: "this connected project is rung 2 of your ladder — every leader stands one up in Week 1–2. The trainer wires the connectors via Claude Code; you use the result."

**Output of the hour:** the shared data-can/can't list + each leader has seen a grounded project answer a real question with sources.

---

## Hr 5 — Concept of agents → write your spec
**Goal of the hour:** converge the day onto **one problem each leader will carry through all four weeks**, captured as a one-paragraph agent spec.

**Open with Preread 4 (0:00–0:15):** round on the *agent-shaped tasks* leaders brought. Test each against the bar: multi-step? takes actions? loops to a goal? Kill the ones that are really just chatbot questions — be ruthless, it saves them three weeks on the wrong problem.

**Talk track (0:15–0:30):**
- Agent vs. chatbot, now with authority: goal not question, tools to act, a loop to completion (Layer 3). Reuse the board.
- Set the **single-thread rule** out loud: *the problem you spec now is the one you build in Week 2, harden in Week 3, and deploy in Week 4.* Choose for organisational impact, not just personal convenience.

**Exercise (0:30–0:55) — the agent spec:**
- Each leader writes a **one-paragraph spec** for their chosen problem: who it's for · the goal · the steps/actions it takes · what data it needs · where a human stays in the loop (ties to Hr 4).
- Trainer pressure-tests two or three live; pair the rest for peer critique.

**Close (0:55–1:00):** hand out the Week-1 homework brief (`02-homework/homework-1.md`). The spec written here *is* the seed of the homework's architecture doc. Point them to the mid-week clinic and Teams channel for blockers.

**Output of the hour → the week's hand-off:** a one-paragraph agent spec per leader = the chosen problem for the whole program. Pasted to Teams; consumed by the homework and by Week 2 Hr 1.

---

### The day's through-line
Stack board (Hr 1) → settled layers (Hr 2) → working prompts (Hr 3) → grounded project + data rule (Hr 4) → **agent spec for the one problem they carry forward (Hr 5)**. Nothing is busywork; each hour feeds the homework and the next week.
