# Lesson Format

The unit this skill produces is **one week's prework as a single, self-contained, interactive HTML file** — a tabbed set of short sections that *teach the concepts themselves*. The reference implementation is `ai-capability-program/weeks/week-1-foundations/00-preread/week-1-prework.html` — copy its visual system and interaction patterns for every new week so the program looks and feels consistent.

> **This replaced an earlier "one file per topic, frame-then-send-to-a-course" model.** Prework now teaches in-file and interactively; external courses are optional depth, not the main event. See ADR if present.

## The model in one paragraph

A leader opens **one file** for the week. A sticky **pill/tab bar** lists the sections; clicking a pill shows that section. Each section **teaches one concept by letting the leader *do* something** — manipulate a widget, step through a process, build intuition (think Brilliant.org, not a slide). At the end of a section the leader clicks **"Mark complete"**; a progress bar fills. **Everything is local** — progress saves to `localStorage` on their device and **nothing flows back** to the trainer. The prework builds understanding; the *session* is where they ask questions and produce things.

## Hard rules

1. **One file per week.** A tabbed/pill structure with N sections (one per concept). Don't ship 5–10 separate files. Name it `week-N-prework.html` in the week's `00-preread/`.
2. **Self-contained.** Inline `<style>` + vanilla `<script>` only. No CDN, no fonts to fetch, no network. Must work fully offline and open with `open "<path>"`.
3. **Teach, don't dispatch.** Each section explains the concept *in-file* with at least one **genuine interaction** that builds intuition (a manipulable widget, a step-through, a sorter, a builder). The interaction *is* the teaching — not decoration, not a quiz bolted onto prose. Reaching for "now go watch this course" as the main content is the failure mode this format exists to kill.
4. **Sections mirror the run-of-show.** Whatever the session teaches must be pre-taught here. Before shipping, check the week's `run-of-show.md` and confirm every major topic has a section. (Week 1 example: prediction · inside-an-LLM · the stack · prompting · RAG · agents+responsible-use.)
5. **Cognitively sequenced.** Order sections so each builds on the last. Use next/back steppers *within* a section where a process unfolds in stages.
6. **Local, not submitted.** Progress + any reflection box persist to `localStorage` only. Say so on the page ("saved on this device; nothing is sent"). **No "copy to Teams / Hour 1 consumes this" mechanics** — the flipped-classroom hand-off is the trainer's job in the room, not a data pipeline.
7. **Optional "Go deeper."** Each section may end with one small optional link to the matching external course, cited by `RESOURCES.md` ID (R1, R5, …). Optional depth, never the substance.
8. **Cited.** Every factual claim ties to a `RESOURCES.md` entry. No bare or invented URLs in the body.
9. **Beautiful & print-friendly.** Clean typography, ~820px column, restrained palette for senior leaders. `@media print` must reveal all panels and expand interactive content.

## Per-section structure (in order)

1. **Tag strip** — "Section n of N" + rough time.
2. **Title** + a short **"why this matters to you"** in the leader's own function's language (never "to understand X").
3. **The teaching** — concept explained through the interaction. Lead with the doing.
4. **Compression** — a small table / rule-of-thumb that fixes the takeaway.
5. **Self-check** — 2 short instant-feedback questions (automatic right/wrong + explanation). Local only.
6. **Go deeper** (optional) — one course link.
7. **Section footer** — "Mark complete" + a "Next: …" button.

## File-level furniture

- **Masthead** — program · week/theme · "Prework" · pace + total time + the "saved locally, nothing sent" line.
- **Sticky navbar** — progress bar (`X / N complete`) + the pill row (pills show a ✓ when done).
- **Finale** — a short completion note shown when all sections are marked complete.
- **"Ask your trainer"** — once, near the end: clinic + Teams doubt channel (answered within 1 business day).
- **Footer** — points to `reference/glossary.html`; notes RESOURCES + local-storage.

## Interaction patterns that work (from the reference file)

Reuse and remix these; invent new ones when a concept needs it:
- **Token predictor** — click to build a sentence one weighted guess at a time → teaches "predicts, probabilistic, doesn't look up."
- **Attention highlighter** — click a word, see what it attends to → teaches attention/coreference.
- **Context-window box** — add chunks, watch the earliest fall out → teaches working memory.
- **Expandable ladder** — click a rung to open it → the AI Evolution Stack.
- **Prompt builder** — toggle parts on/off, watch a preview + reliability meter assemble → prompt anatomy.
- **Step-through (next/back)** — reveal a process one stage at a time → RAG retrieve→ground→cite, or an agent loop.
- **Sorter** — classify items with instant verdicts → data-sensitivity judgement.

## Quality bar

- Vanilla JS only — runs by double-click in any browser, today and in a year. Wrap each widget in its own IIFE with defensive guards.
- Feedback immediate and automatic — never "answers at the bottom."
- New term introduced → add it to `reference/glossary.html` the same session (`GLOSSARY-FORMAT.md`).
- Tailor examples to the cohort's common ground; tailor to a specific leader when building for one (mission blocks).
