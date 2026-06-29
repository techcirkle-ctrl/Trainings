# PLAYBOOK — turning a week's PPT spec into shipped teaching files

This is the **source of truth** for *how we teach* in the AI Capability Program. It sits
above the per-artifact format files (`LESSON-FORMAT.md`, `DECK-FORMAT.md`, etc.) and
encodes the doctrine, the translation method, and the quality bar that every week must
clear. Read it first when building any week.

> **The reference reality is shipped Week 1, not the older docs.** Where any other file in
> this skill (or `overview.md`) disagrees with what `weeks/week-1-foundations/` actually
> shipped, **the shipment wins and this playbook records the correction.** The two known
> drifts are reconciled at the end of this file.

---

## 0. The job in one sentence

Each week we are handed a **PPT spec** (one slide: topics, the 5-hour breakdown, the one
artifact) and a **reference shipment** (Week 1). Our job is to translate the spec into the
same three finished, interactive, leader-friendly deliverables Week 1 has — **pre-read,
session, homework** — for a non-technical senior cohort, advancing the *one problem each
leader carries across all four weeks*.

---

## 1. Doctrine — the teaching beliefs (non-negotiable)

These hold for every week and every artifact.

1. **Teach a little, do a lot.** Hands-on time is deliberately longer than teach time.
   Reading is a cost; interaction is the product.
2. **Out-judge the machine.** The leader's scarce skill is judgement, not operation. Every
   artifact hands them a *call to make*, never just information to absorb.
3. **The cheapest layer that works wins.** Over-building is the most common and most
   expensive mistake. We teach restraint as the core competence.
4. **One escalating artifact, not four.** The problem picked in Week 1 is scoped → built →
   hardened → deployed across all four weeks. **No week reseeds a new use case.** Every
   homework advances that single thread.
5. **Leader altitude, no jargon.** Concepts land through plain-English analogies (LLM =
   autocomplete, context window = a desk, RAG = ground it in your docs) and are always tied
   to a decision the leader owns — cost, risk, where the human stays in the loop.
6. **No false simplifications.** Never teach a clean hierarchy that breaks under an expert's
   eye (the stack is *composable capabilities on one engine*, not a containment ladder).
   Clarity must never cost correctness.
7. **Use before explain.** Let them drive the tool before opening the internals.
8. **Tool reality: Claude chat + Projects** (no-code, on the program workspace account).
   Claude Code is the *trainer's* instrument shown live; leaders touch its outputs, not the
   terminal. (See reconciliation §7.)
9. **Test-your-understanding everywhere.** Every concept beat closes with an instant-feedback
   check (MCQ that teaches on right *and* wrong, or a binary sorter with per-item verdicts).
   Engagement is kept up by interaction, not willpower.
10. **British spelling, executive register** (behaviour, summarise, organised). Self-contained
    HTML, local-only state, print-friendly — always.

---

## 2. The translation — define COVERAGE once, then derive all three

**The key insight: pre-read and session teach the *same concept set* for the week.** They
differ only in *mode*, not topics — the pre-read builds intuition before the room; the session
applies that same material and produces something on the leader's own problem. So we don't
split content three ways. We **define one canonical coverage for the week, agree it, then
derive the deliverables from it.**

**Step 1 — Define the week's COVERAGE (do this first, grill it before building anything).**
From the PPT slide (its pre-work list + the five session hours) write the **canonical concept
list** for the week: the ordered set of ideas this week teaches, in cognitive sequence, each in
one line of leader language. This single list is the contract. *This is the thing we finalize
together before any HTML is written.*

**Step 2 — Derive the three deliverables from that one coverage:**

| Deliverable | Relationship to the coverage | Mode |
|---|---|---|
| **Pre-read** | One section per concept in the coverage. | Teach the *intuition* by doing — driveable widget + a check, generic (no leader's own data). |
| **Session (5 hr)** | The *same* concepts, mapped onto the PPT's hours as movements. | *Apply* + *produce* — trainer drives the widget live, leaders build on their *own* problem (hands-on). |
| **Homework** | Draws on the *whole* week's coverage. | *Advance the one artifact* by one stage — brief + template + self-check bar + due date. |

**Rules that keep it coherent:**
- Every concept in the coverage appears in *both* the pre-read (as intuition) and the session
  (as application). If a concept is in the session but not the pre-read, the coverage or the
  pre-read is incomplete.
- A mechanism ("how X works") is taught in the pre-read as a **driveable visual**, so the
  session spends its time on *application*, not first explanation.
- Anything needing the leader's own data/problem lives in the **session or homework only** —
  the pre-read is generic.
- The homework is **the artifact advancing one stage** — the next state of the same problem,
  never a fresh exercise.

---

## 3. The three deliverables and the bar each clears

Each defers to its format file for mechanics; here is *what it is* and *when it's done*.

### 3a. Pre-read — `weeks/week-N-<theme>/00-preread/week-N-prework.html`
One self-contained, tabbed, interactive HTML file. Teach-by-doing per section. → **`PRE-READ-PLAYBOOK.md`** is the **primary source of truth for pre-reads** (supersedes `LESSON-FORMAT.md` for them; read it before building any pre-read).
- **Done when:** every section is `why-this-matters → ≤3-min teaching-through-an-interaction →
  "keep this" recap → instant-feedback self-check → mark-complete`; every session topic is
  covered; every widget runs on every path; progress persists locally; prints clean.

### 3b. Session — `weeks/week-N-<theme>/01-workshop/`
**Two decks of the same slides: an `…-audience.html` and a `…-presenter.html`** (the presenter
copy adds the per-slide script: *Remember → Move(timing) → Say(verbatim) → Do(facilitation) →
Bridge →*). Movement-based (goal → do → judgment); dark goal slide → light do/widget slide;
hands-on prompts inline with copy buttons. → `DECK-FORMAT.md` *(reconciled — see §7)*
- **Done when:** every hour of the PPT spec is a movement or block; concept movements carry a
  live widget ported from the pre-read; hands-on movements have copyable prompts; the presenter
  deck carries timing + talk-track + facilitation + the backup bank; re-teaches from zero.

### 3c. Homework — `weeks/week-N-<theme>/02-homework/homework-1.md`
The brief that advances the one artifact. → mirror Week 1's homework shape.
- **Done when:** it states the output, the steps, a paste-in template, a *self-check quality
  bar* (no grades), the due date + where it's handed in (Teams + bring to next session), and
  names exactly how it feeds the next week.

---

## 4. Benchmarks — the measurable bar (from Week 1)

Concrete, checkable. If a week misses these, it isn't shipped.

**Pre-read**
- [ ] ~½ of section time is interaction, not reading. No section is a wall of prose with a
      widget bolted on the end.
- [ ] Every section has ≥1 *genuine* interaction that teaches the mechanism (driveable
      machine, node-graph step-through, build-up composer, sorter — not a quiz in disguise).
- [ ] Every section ends with an instant-feedback check (4-option MCQ that explains both
      right and wrong, or a binary sorter).
- [ ] Every mechanism ends with a one-line **"Leader's read"** tying it to a decision.
- [ ] Callbacks sit *adjacent* to their setup. No concept used before it's introduced.

**Session**
- [ ] Every movement is **goal → do → judgment**; nothing passive.
- [ ] On-glass text passes "could the trainer *say* this rather than show it?"
- [ ] Hands-on blocks are longer than teach blocks.
- [ ] Presenter deck carries per-movement timing, verbatim "Say", facilitation "Do", and a
      backup problem bank.
- [ ] Concept widgets are ported from the pre-read (same data, sized up).

**Homework**
- [ ] Advances the *same* problem by exactly one stage.
- [ ] Has a paste-in template and a self-check bar; no scores.
- [ ] Names what it feeds in the next week.

**Whole week**
- [ ] Tailored to the cohort's functions (Finance/HR/Sales/IT examples), per `MISSION.md`.
- [ ] New terms added to `reference/glossary.html`; every claim cited to `RESOURCES.md`.
- [ ] British spelling; `DESIGN.md` tokens/registers; self-contained; local-only; prints clean.

---

## 5. Per-week production checklist

The repeatable path from slide to shipped, for one week:

1. **Read the spec + the reference.** The week's PPT slide; `overview.md`; the week's
   `README.md` + `run-of-show.md` skeleton; the prior week's homework (what the leaders walk
   in *with*); Week 1's shipped files as the pattern.
2. **Define the COVERAGE and agree it (§2 Step 1).** The canonical concept list for the week.
   This is grilled and finalized *before any HTML is written* — it is the one thing both the
   pre-read and the session are derived from.
3. **Build the pre-read** from the coverage to the bar (§3a, §4). Author widgets, run every path.
4. **Build the session decks** from the *same* coverage — audience first, then add the
   presenter script (§3b, §4).
5. **Write the homework** drawing on the whole week's coverage (§3c, §4).
6. **Glossary + resources** — add any new term/source the week introduced.
7. **Self-audit** as teacher *and* student against §4. Fix drift in cross-references, finale,
   glossary.
8. **Commit** on the week's branch.

---

## 6. Running it week by week (how to move forward)

We build **one week per chat session.** The kickoff is deliberately minimal — the new chat
reads *this section* and drives the rest itself, asking the trainer which week.

**Paste-ready kickoff message (no editing needed — paste verbatim):**

```
Read .claude/skills/teach/PLAYBOOK.md, then follow its §6 "Running it week by week"
procedure to plan and build the next week of the AI Capability Program. Start by asking
me which week we're doing. Name this session "Week <N> planning" once I tell you.
```

**Procedure the new chat follows (this is the §6 it's pointed at — Claude, do these in order):**

1. **Ask the trainer which week N.** Then resolve the week from this map and read its files:

   | N | Theme / folder | PPT slide |
   |---|---|---|
   | 2 | `week-2-agentic-deep-dive` | slide 7 |
   | 3 | `week-3-handson-building` | slide 8 |
   | 4 | `week-4-build-and-lead` | slide 9 |

2. **Read, in order, then confirm understanding briefly (don't skim):**
   - `.claude/skills/teach/PLAYBOOK.md` (this doctrine + the bar) — already reading it.
   - `.claude/skills/teach/SKILL.md`, `LESSON-FORMAT.md`, `DECK-FORMAT.md` (mechanics).
   - `ai-capability-program/overview.md` + `reference/DESIGN.md` (contract + visual canon).
   - The **Week N PPT slide** in `source/AI_Capability_Program_v3.pptx` (the spec = *what* to
     deliver). *(Use python-pptx to read it; it's a binary file.)*
   - `ai-capability-program/weeks/week-N-<theme>/` (the current skeleton).
   - `ai-capability-program/weeks/week-1-foundations/` (the **reference shipment** = *how* we
     deliver — match its pattern; shipment wins over any older doc).
   - The **prior week's finished homework** (what the leaders walk in *with*).

3. **Do NOT build yet. First agree the COVERAGE (§2 Step 1).** Propose the week's canonical
   concept list and let the trainer grill it. Iterate until agreed — this is the gate.

4. **Build from the agreed coverage:** pre-read → session decks (audience, then presenter
   script) → homework. To the bar (§3–§5).

5. **Self-audit (§4)** as teacher *and* student → fix drift → **commit on the week's branch**.

6. **When the week looks good → new chat for the next week.** Repeat.

---

## 7. Reconciliation — where the old docs were corrected

Recorded so the corrections aren't re-litigated. **Shipment wins** — and "shipment" means
*the files that actually exist in `weeks/week-1-foundations/`*, verified against disk, not
what any ADR/README/format file claims was built.

1. **Session artifact = audience deck + presenter deck**, not "3 act-decks + a separate
   `hands-on-movements.md` helper" and not a `keynote.html`. Week 1 shipped two decks of the
   same 47 slides — `deck-week1-foundations-audience.html` and `…-presenter.html` (the
   presenter copy adds the per-slide *Remember → Move → Say → Do → Bridge* script) — with
   hands-on prompts **inline** behind copy buttons. **Superseded and known-stale:**
   `DECK-FORMAT.md` (3-deck/helper model), **`ADR 0002`** (its "reference implementation"
   lists `deck-1/2/3` + `hands-on-movements.md` as "all authored" — those files do **not**
   exist), the Week-1 `README.md` (same phantom file list), and `KEYNOTE-FORMAT.md` (the
   keynote was absorbed into the deck's opening cold-open slides, never shipped standalone).

2. **Build tool = Claude chat + Claude Projects** (no-code), on the program workspace
   account. Triply confirmed by shipped artifacts: the v2 preread ("live Claude Project
   demo"), the facilitator run-sheet ("run the capstone-finder prompt in Claude"), and the
   audience deck (tool = "Claude Desktop"). **Stale "Gems" framing still lives in**
   `overview.md` (tooling ladder), `NOTES.md` ("Resolved: Gems for the no-code core"), and
   **`reference/glossary.html`** (the `Gem` term says "the no-code build surface every leader
   uses in this program"). The glossary is the desk reference leaders keep — its `Gem` entry
   is actively wrong and should be corrected to Claude Projects **when the glossary is next
   touched for Week 2** (don't edit Week-1 content pre-emptively; flag it).

3. **Canonical preread = `week-1-preread-v2.html`** (4 sections: Prompting → RAG → Agents →
   Stack, ~1 hr, ends on synthesis), **not** the older 6-section `week-1-prework.html`.
   The folder name (`00-preread`) matches v2; v2 is the trimmed, re-sequenced, leaner cut
   that fits the "text-light, ends-on-synthesis" intent. **But** `SKILL.md`, `LESSON-FORMAT.md`
   and `DESIGN.md` all still name the **old v1** as "the reference implementation." When
   building a week's preread, **emulate v2's structure** (4 lean sections, one concept each,
   ~15 min/section, synthesis last), borrowing v1's richer widgets where the concept needs
   them. *(v2 carries two harmless leftover bugs — a hardcoded "0/6" label and dead
   `placeStack` JS — don't copy those.)*

4. **Cohort functions are known even though `MISSION.md` per-leader blocks are blank.** The
   run-sheet names the room: **MD · Finance Head · HR Head · HR Deputy · one more functional
   lead.** Tailor Week 2 Finance/HR-heavy; only named-leader pain points are missing.

5. **Week 2 is where the build begins.** The run-sheet's realistic Day-1 promise is "found
   the problem + architected & specced the agent — *the build happens across Weeks 2–3.*"
   So Week 2 = turn the Week 1 spec into a **working Claude Project** (the same mechanism as
   the Capstone Finder, on the leader's own problem). Don't promise a coded/tool-looping
   agent the no-code tool can't deliver.

> Not a conflict (kept distinct on purpose): **pre-read progress is local-only and never
> submitted; homework *is* a deliverable** posted to Teams and brought to the next session.
> Different layers, both correct. (Confirmed by `ADR 0001`.)
