# Lesson Format

A lesson is the primary unit this skill produces: **one self-contained interactive HTML preread** that teaches ONE thing tied to a leader's mission. The reference implementation is `ai-capability-program/weeks/week-1-foundations/00-preread/5-pe-reading-the-ai-evolution-stack.html` — copy its visual system for every new lesson so the program looks consistent.

## Location & naming

```
ai-capability-program/weeks/week-N-<theme>/00-preread/<n>-<slug>.html
```
`<n>` is 1–5 (the preread's position in the week). Slug is dash-case. Example: `2-anthropic-tool-use.html`.

## Hard rules

1. **Self-contained.** Inline `<style>` and vanilla `<script>` only. No external assets, no CDN, no fonts to fetch, no network calls. It must work fully offline and open with a single command:
   ```
   open "<path-to-lesson>.html"
   ```
2. **Teaches one thing.** One skill or concept. If you're tempted to teach two, that's two lessons.
3. **Mission-framed.** Opens with a "why this matters to you" block in the leader's own function's language — never abstract ("to understand X").
4. **Cited.** Every factual claim links to a `RESOURCES.md` entry by ID (R1, R5, …). No bare or invented URLs in the lesson body.
5. **Tight feedback loop.** An instant-feedback interaction — scenario multiple-choice with automatic right/wrong + explanation and a running score. This is the learning, not decoration.
6. **Closes the Hr-1 loop.** Ends with a "bring this to Hour 1" output: the leader produces something (a one-line answer, a workflow mapped to a concept) with a copy-to-clipboard button so they can paste it into the Teams channel. Hr 1 of the session consumes it.
7. **Beautiful & print-friendly.** Clean typography, ~760px reading column, restrained palette suited to senior leaders. Include `@media print` rules; leaders revisit and print these.

## Structure (in order)

1. **Masthead** — program · week/theme · "Preread N · wrapper|authored" · duration · one-line topic.
2. **Mission framing** — "why this matters to you" + what they'll be able to do by the end.
3. **The one idea** — the content. For *authored* lessons, full explanation with leader-level examples and a visual where it helps (e.g. the layer ladder). For *wrapper* lessons, a short frame then a clear hand-off to the external course.
4. **Optional decision lens / cheat element** — a small table or rule of thumb that compresses the judgement.
5. **Feedback loop** — the quiz (`Check yourself`).
6. **"Bring this to Hour 1"** — the output box + copy button.
7. **"Ask your trainer"** reminder — clinic + Teams doubt channel (answered within 1 business day).
8. **Sources** — numbered, linking to RESOURCES entries; note they're tracked in `RESOURCES.md`.
9. **Footer** — points to `reference/glossary.html` for the compressed essentials.

## The two types

- **Wrapper** (prereads 1–4): thin. Frame why it matters → external course (cite the registry) → comprehension loop on the *key takeaways* → output. Don't re-teach the external course; orient and check.
- **Authored** (item 5, the PE readings): full content you write, because it's in-house material. The richest lessons.

## Quality bar

- Vanilla JS only — no frameworks, no build. It must run by double-click in any browser, today and in a year.
- Feedback must be immediate and automatic — never "answers at the bottom."
- If the lesson introduces a new term, add it to the glossary in the same session (see `GLOSSARY-FORMAT.md`).
- Tailor examples to the specific leader when building for one; use the cohort's common ground when building for all.
