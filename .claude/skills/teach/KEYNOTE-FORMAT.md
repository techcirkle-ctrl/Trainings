# KEYNOTE-FORMAT — the per-week Sparkline cold open

The authoring spec for `weeks/week-N-<theme>/01-workshop/keynote.html` — the **secondary**
per-week artifact (the prework stays the primary unit). Read this before authoring a keynote.

## What it is

A **~10-minute, 10–12-slide TED-style cold open** the trainer delivers *before* Hr 1, to
sell that week's promise. It is a **persuasion artifact, not a knowledge artifact** — it
reframes the pain and the possibility the prework already taught; it does not teach new
material. It uses **Nancy Duarte's Sparkline**: oscillate between *What Is* (the painful
present) and *What Could Be* (the possible future), ending on the week's call to work.

- **Self-contained HTML slide deck.** Inline CSS + vanilla JS, no network, no build. Opens
  with `open keynote.html`. Arrow-key / space navigation, slide counter, print-friendly.
- **Standalone.** Do **not** edit `run-of-show.md` to reference it; the artifacts stay
  decoupled. The trainer slots it in manually.
- **Visual system:** defer entirely to `reference/DESIGN.md`. Same tokens/fonts as the
  prework; full-bleed slide layout (not the reading column).

## Where the two poles come from

- Pull **What Is** and **What Could Be** from the week's `run-of-show.md` objective + the
  arc/promise in `overview.md`. **Never `MISSION.md`** — keep it **cohort-general**, so the
  deck is reusable across cohorts and puts no one on the spot. Concrete imagery ("the report
  that eats your Friday"), not "businesses struggle with AI" — but never named to a person.

## The 7-beat default skeleton

A **default**, not a cage — restructure per week if the content demands it (the oscillation
count especially flexes to the week's concept count). Each beat is 1–2 slides.

1. **STAR opener** *(What Is)* — one vivid status-quo image. Duarte's "Something They'll
   Always Remember." The painful present this week's topic attacks.
2. **The gap named** — status quo vs. the tantalizing possible. Plants the week's tension.
3. **Oscillation 1** *(What Is → What Could Be)* — week concept #1 as a gap closing.
4. **Oscillation 2** — concept #2, contrast sharpened.
5. **Oscillation 3** — concept #3. (Pull the week's 3–4 big concepts from the run-of-show
   hour goals; add/drop oscillations to match.)
6. **The turn / new bliss** *(What Could Be, made real)* — what they hold by Friday; the
   week's promise from `overview.md` rendered as the resolved future.
7. **Call to the week's work** — hands off to the day, ends the cold open.

## The two-pole visual coding

Render the oscillation *literally* (see `reference/DESIGN.md` → "The two registers"):

- **What Is** slides — cool/muted, `--wash` ground, `--muted` ink, no teal. Feels inert.
- **What Could Be** slides — lifted, `--accent` teal, brighter surfaces. The room warms.
- A small persistent **sparkline glyph** in a corner tracks position along the arc.

## Speaker notes

- **Mechanism:** press `S` (or `N`) to toggle a notes panel; **hidden by default** so the
  deck is projector-clean. Pure CSS/JS, no popup window. The trainer always sees the slide
  counter + the current **beat label** ("Oscillation 2 — What Could Be").
- **Content:** **bullet cues, not a verbatim script** — 3–5 delivery beats per slide: the
  point to land, the contrast to draw, one transition line. **Exception:** the STAR opener
  and the final call get **fuller suggested phrasing** (those two moments are scripted-tight
  in real TED talks).

## Citations

- **Exempt from on-slide citations** (unlike the prework). It makes no new factual claims.
- **Default to zero stats on slides.** If a hard number *does* appear, source it to a
  `RESOURCES.md` entry **in that slide's speaker notes** — never on the slide face.

## Reference implementation

`weeks/week-1-foundations/01-workshop/keynote.html` is the de-facto template (there is no
`templates/` folder — Week 1 is the template, same as the prework). Copy its slide engine,
nav, notes panel, and pole-coding so every week's keynote is consistent.
