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
3. **The teaching** — concept explained through the interaction, in read→interact→recap cycles. Lead with the doing; keep any callback adjacent to what it refers to.
4. **Compression** — a small "Keep this" table / rule-of-thumb that fixes the takeaway, placed *after* the interaction (recap, never the explanation itself). Often paired with a one-line "Leader's read."
5. **Self-check** — instant-feedback recall. Prefer a *visual* recall that reuses the section's interaction (place-on-the-visual); a short quiz (automatic right/wrong + explanation) is fine as the closing check. Local only.
6. **Go deeper** (optional) — one course link.
7. **Section footer** — "Mark complete" + a "Next: …" button.

## File-level furniture

- **Masthead** — program · week/theme · "Prework" · pace + total time + the "saved locally, nothing sent" line.
- **Sticky navbar** — progress bar (`X / N complete`) + the pill row (pills show a ✓ when done).
- **Finale** — a short completion note shown when all sections are marked complete.
- **"Ask your trainer"** — once, near the end: clinic + Teams doubt channel (answered within 1 business day).
- **Footer** — points to `reference/glossary.html`; notes RESOURCES + local-storage.

## Interaction patterns — the catalog (from the reference file)

Reuse and remix these; invent new ones when a concept needs it. **Prefer the visual, mechanistic patterns** — they show a mechanism the learner drives.

**Prefer these:**
- **Driveable machine (before/after toggle)** — one control flips the system between two modes and re-runs; the learner sees the contrast instantly. *RAG ON/OFF: pick a question, flip RAG, watch documents light by relevance, flow into a context box, produce a cited answer — or honestly "not in our docs."* The single highest-impact pattern for "what does X actually change?"
- **Node-and-link graph, step-through** — nodes + edges drawn as SVG; "Step"/"Run all" lights the active node, its edge(s), and any tool it calls. *The agent loop (Goal → Think → Act → Observe → Decide → Done, lighting the tool each pass and looping back visibly); the LLM forward pass (input → layers → output, click a neuron to inspect its weights).* Use for anything with a flow or a cycle.
- **Build-up composer** — toggle capabilities/parts on and watch the result + a cost/quality meter recompute. *Compose LLM + retrieval + tools → the system names itself (Plain LLM → RAG → Agent → …); the prompt builder.* Teaches "it's made of independent pieces."
- **Animated meter** — a value moves so an abstract process is *felt*. *"Watch it learn": error falls, confidence climbs, then freezes → training and frozen knowledge.*
- **Place-on-the-visual recall** — the self-check reuses the teaching visual: drop a task onto the stack you just built (over-reach lights amber, too-low red); switch on the capabilities a task needs and check. Spatial and tactile.
- **Token predictor** — click to build a sentence one weighted guess at a time → "predicts, probabilistic, never looks up." Still excellent.
- **Attention highlighter** — click a word, see what it attends to → attention/coreference.
- **Sorter** — classify items with instant verdicts → data-sensitivity judgement.

**Retire these — they read as passive or as a quiz in disguise:**
- **Click-to-expand accordion** (the old "ladder") — passive reading hidden behind a toggle. Replace with a build-up composer or a graph.
- **Linear text step-through** where a *visual* would carry it — if the steps describe a flow (retrieval, a loop), draw the flow and light it; don't reveal paragraphs one by one.
- **Text-prompt + answer-button grid** dressed up as "recall" — it's a quiz wearing the section's clothes. Reuse the section's visual instead.
- **A wall of tables/bullets as the primary teaching of a mechanism** — tables are *recap*, placed *after* the interaction as a "Keep this" card, never the explanation itself.

## Pedagogical principles (hard-won — apply to every section)

These were paid for in revision. Honour them up front so future weeks don't repeat the rework.

- **Read → interact → recap, in short cycles.** ~2–3 minutes of reading, then a hands-on beat, then a one-line takeaway — repeated. Never a wall of prose with one widget bolted to the end. People retain what they manipulate; low attention spans punish lecture.
- **Keep callbacks adjacent to their setup.** If a section says "the dial you just felt," the dial must be the *immediately preceding* element — not separated by two other topics. A payoff that references an earlier experience has to sit right after it, or the reference doesn't land. Re-order ruthlessly to keep a setup and its callback together.
- **Visualize the mechanism; don't tabulate it.** Anything about *how something works* earns a driveable visual (a graph, a machine, an animation). If you're explaining a mechanism with a table, a bullet list, or a click-to-expand accordion, you've already lost the room — convert it.
- **Interactions must teach, not test in disguise.** A recall exercise should use the *same* visual vocabulary as the lesson and be spatial/tactile. If it feels like a quiz wearing the section's clothes (a sentence plus four answer buttons), redesign it around the section's visual.
- **No false simplifications.** Never teach a clean hierarchy or containment that breaks under an expert's scrutiny. (Canonical example: LLM / RAG / Agent / Multi-agent are **composable capabilities on one engine**, *not* a containment ladder where each layer includes the one below. An agent need not use RAG; they compose freely.) Clarity must not cost correctness — if a domain expert would wince, it's wrong, however tidy.
- **Make the control embody the idea.** Apply `DESIGN.md`'s two-register rule to the widget's *own* controls: the status-quo / "what is" state inert and muted, the "lifted / what could be" state teal (RAG **OFF** grey vs **ON** teal; Chatbot vs Agent). The control itself should teach. Use the design's named components — rounded pills, the segmented switch — never basic bordered rectangles.
- **End mechanisms with a "Leader's read."** One line tying the mechanism to a decision the leader owns (turn temperature down for repeatability; fewest-capabilities-wins; where the human sits in the loop). This is what makes it *their* knowledge, not trivia.
- **Build it, then drive it.** After authoring a widget, run it in the preview and exercise *every* path before calling it done. Derive widget state from the DOM (read the active class), not a parallel JS variable, so a toggle and its logic can never desync.

## Self-audit before shipping a week (read it as teacher *and* as student)

Walk the whole prework, paired sections in order (1→2, 3→4, 5→6), and check:
- **Sequence** — each section builds on the last; the next/previous handoff flows; no concept used before it's introduced.
- **Cognitive load** — no section carries more concepts than its time tag implies; every hard idea has an interaction supporting it, not just prose.
- **Accuracy** — every claim scientifically defensible; no simplification that breaks under scrutiny.
- **Consistency** — cross-references, the finale, and the glossary match the *current* content. (Real miss caught late: the finale still said "four-layer stack" after Section 3 was reframed to composition.)
- **Grammar/spelling & register** — clean, and consistent British spelling for the Sandvik cohort (behaviour, summarise, organised).

## Quality bar

- Vanilla JS only — runs by double-click in any browser, today and in a year. Wrap each widget in its own IIFE with defensive guards.
- Feedback immediate and automatic — never "answers at the bottom."
- New term introduced → add it to `reference/glossary.html` the same session (`GLOSSARY-FORMAT.md`).
- Tailor examples to the cohort's common ground; tailor to a specific leader when building for one (mission blocks).
