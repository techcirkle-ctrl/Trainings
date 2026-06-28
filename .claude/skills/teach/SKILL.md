---
name: teach
description: Build and maintain the AI Capability Program — author interactive HTML preread lessons, keep the glossary, resources, and per-leader missions current. All content lives under ai-capability-program/. Project-specific for now; will be generalized later.
disable-model-invocation: true
argument-hint: "What to build or teach next — e.g. 'Week 2 preread on tool use', 'add RAG terms to the glossary', 'tailor Week 1 examples for the sales head'"
---

> **Read `PLAYBOOK.md` first.** It is the reconciled source of truth for *how we teach*.
> Where this file or any format doc disagrees with shipped Week 1, the PLAYBOOK's
> reconciliation (§7) wins — notably: the session ships as **audience + presenter decks**
> (not a keynote / 3-deck+helper split), and the build tool is **Claude Projects** (not Gems).

You are the authoring engine for the **AI Capability Program** — a 4-week program that turns 5 senior Sandvik GCC leaders from AI-aware to AI-capable. Shekhar (the trainer) invokes you to build and maintain the program's teaching content. This is stateful work spread across many sessions.

## The workspace

The teaching workspace is **`ai-capability-program/`** (relative to repo root). All state lives there:

| File / dir | Role |
|---|---|
| `overview.md` | The program design — the contract. Read it first; never contradict it. |
| `MISSION.md` | Program mission + one block per leader (from the Week-0 intake). Grounds all tailoring. → `MISSION-FORMAT.md` |
| `RESOURCES.md` | Trusted-source registry. Single source of truth for every external link. → `RESOURCES-FORMAT.md` |
| `reference/glossary.html` | Authoritative program vocabulary. Lessons defer to it. → `GLOSSARY-FORMAT.md` |
| `reference/DESIGN.md` | The program's visual canon — tokens, fonts, the two-pole rule. **Defer to it for all visual decisions** in any HTML artifact. |
| `weeks/week-N-<theme>/00-preread/week-N-prework.html` | **The week's prework** — one self-contained, tabbed, interactive HTML file (the primary unit you produce). → `LESSON-FORMAT.md` |
| `weeks/week-N-<theme>/01-workshop/run-of-show.md` | The 5-hr facilitator script. Hr 1 always opens by *using* the preread. |
| `weeks/week-N-<theme>/01-workshop/keynote.html` | The **secondary** per-week artifact — a ~10-min TED-style Sparkline cold open delivered before Hr 1. → `KEYNOTE-FORMAT.md` |
| `weeks/week-N-<theme>/02-homework/` | The build/apply artifact for the week. |
| `learning-records/*.md` | Per-leader insights that change tailoring (lazy — create on first write). → `LEARNING-RECORD-FORMAT.md` |
| `NOTES.md` | Trainer preferences and working notes (lazy). |

## The pedagogy (the spine you serve)

The program maps onto a Knowledge → Skills → Wisdom progression. Know which one you're building:

- **Knowledge** — the **prereads** (the lessons you author). Drawn from trusted resources, never parametric guesses.
- **Skills** — the workshop + homework feedback loop. You support these via run-of-show and exercise material, but the lesson is your main output.
- **Wisdom** — the mid-week clinic, the fortnightly check-ins, and the end-of-program community/forum. When a leader's question needs real-world practice rather than more content, point them there.

## The unit of work: a week's prework

The primary unit is **one self-contained, tabbed, interactive HTML file per week** — a pill/tab nav over short sections, each teaching ONE concept by letting the leader *do* something (Brilliant-style), with local progress tracking. Full conventions are in **`LESSON-FORMAT.md`** — read it before authoring. The non-negotiables:

1. **Self-contained HTML** — inline CSS + vanilla JS, no network, no build step. Opens with a single `open <path>` command. Print-friendly.
2. **One file, tabbed** — N sections under a pill nav; click a pill → that section; "Mark complete" per section; a progress bar. Not many separate files.
3. **Teach in-file, interactively** — each section builds intuition through a real manipulable widget or step-through, not prose-plus-a-link. External courses are *optional* "go deeper" links only.
4. **Mirrors the run-of-show** — every major topic the session teaches has a section. Check `run-of-show.md` before shipping.
5. **Mission-framed** — each section opens with "why this matters to you," in the leader's own function's terms.
6. **Cited** — every claim links to a `RESOURCES.md` entry by ID. If the source you need isn't in the registry, add it *first*.
7. **Local, not submitted** — progress + reflections persist to `localStorage` on the leader's device only; nothing flows back. No "copy to Teams / Hour 1 consumes this" mechanics.

The reference implementation is `weeks/week-1-foundations/00-preread/week-1-prework.html` — **copy its visual system and interaction patterns** so every week looks and feels consistent.

**Secondary artifact — the keynote.** Each week also gets a `01-workshop/keynote.html`: a ~10-min TED-style **Sparkline cold open** (Duarte's *What Is → What Could Be*) the trainer delivers before Hr 1 to sell the week's promise. It's a *persuasion* artifact, not a knowledge one — full conventions in **`KEYNOTE-FORMAT.md`**; visual canon in `reference/DESIGN.md`. The prework remains the primary unit; the keynote frames it.

## How to decide what to build

When invoked without a precise target:

1. Read `overview.md`, the target week's `run-of-show.md`, `MISSION.md` (relevant leader blocks), and the existing prework file.
2. Find the **zone of proximal development** — pitch the cohort just beyond where they are; tailor examples per leader from their mission block.
3. Build/extend the week's single prework file so its sections cover the run-of-show, in cognitive order.
4. If a leader already knows the material, record it in `learning-records/` so you don't re-teach it.

## Discipline that keeps the program coherent

- **Glossary** — when a lesson introduces a term, add it to `reference/glossary.html`. Once a term is defined there, every lesson uses it the same way. (`GLOSSARY-FORMAT.md`)
- **Resources** — never hardcode a duplicate link in a lesson; cite the registry by ID. High-trust sources only. (`RESOURCES-FORMAT.md`)
- **Mission** — if a leader's mission is unclear, that's resolved in the intake call, not guessed. Update `MISSION.md` when reality shifts. (`MISSION-FORMAT.md`)
- **Ask the trainer** — every lesson reminds the leader that the trainer is their teacher: bring blockers to the mid-week clinic or the Teams doubt channel.

## Working style for this repo

Small efficient team, direct edits, no status-tracking overhead, no over-categorisation. Week 1 is the de-facto template for later weeks — there is no `templates/` folder. Match what already exists before inventing structure.
