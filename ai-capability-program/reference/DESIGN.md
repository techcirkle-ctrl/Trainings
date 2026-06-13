# Design Language — AI Capability Program

The program-wide visual canon. Every HTML artifact (prework lessons, keynote decks,
the glossary) defers to this so the program reads as **one thing**, not a pile of files.
Descriptive, not aspirational: these tokens already live in
`weeks/week-1-foundations/00-preread/week-1-prework.html` — that file is the reference
implementation. Match it; don't reinvent it.

> Authoring engine: the `teach` skill reads this before building any visual artifact.

---

## Tokens (single source of truth)

Inline these CSS custom properties verbatim in every file. Do not introduce new colours
without adding them here first.

```css
:root{
  --ink:#16202b;        /* primary text */
  --muted:#5c6b7a;      /* secondary text, status-quo register */
  --line:#e4e8ec;       /* hairline borders */
  --paper:#ffffff;      /* card surface */
  --wash:#f6f8fa;       /* page background */
  --accent:#0b6e6e;     /* teal — the program's signature; the "lifted" register */
  --accent-soft:#e2f0ef;
  --warn:#b06a00;       /* ceilings, cautions */
  --good:#1c7a4a;       /* success, "done" */
  --bad:#b23b3b;        /* wrong, failure mode */
}
```

## Type

- **Body / reading:** serif — `ui-serif, Georgia, "Iowan Old Style", Palatino, serif`.
- **UI, kickers, labels, widgets:** sans — `ui-sans-serif, system-ui, sans-serif`.
- **Code:** mono — `ui-monospace, Menlo, Consolas, monospace`.
- **Kicker** convention: 600 weight, `letter-spacing:.14em`, uppercase, `--accent`, ~12px.
  Every section/slide opens with one.

## Component vocabulary

Reuse these named patterns; don't invent parallel ones.

| Component | Class | When to use |
|---|---|---|
| Card | `.card` | A bounded unit of content — rounded 14px, hairline border, faint shadow. |
| Pill nav | `.pills`/`.pill` | Tabbed navigation (prework). Active = teal fill. |
| Why-box | `.why` | "Why this matters to you" — accent-soft panel opening a section. |
| Lab shell | `.lab` | An interactive widget's container (prework). |
| Kicker | `.kicker` | The uppercase teal eyebrow above a title. |
| Tag | `.tag` | Small uppercase metadata chip (section N of M, duration). |

## The two registers (Sparkline rule)

The program tells a **What Is → What Could Be** story (Nancy Duarte's Sparkline). The two
poles are colour-coded the *same way everywhere* so the contrast is felt, not just read:

- **What Is** — the painful present. Cool/muted: `--wash` ground, `--muted` ink, no teal.
  Restrained, a little flat. The status quo should feel inert.
- **What Could Be** — the possible future. Lifted: `--accent` teal, `--paper` surfaces,
  more light and saturation. The future should feel like the room warms up.

Any future persuasion artifact (keynote, pitch) **must** code its two poles this way.

## Two layouts, one palette

The palette is shared; the layout is not. Pick by artifact:

- **Reading column** (prework, glossary) — narrow `--maxw:820px`, dense serif text,
  scroll + tab nav. Built for self-paced study on a laptop.
- **Full-bleed slide** (keynote) — one viewport = one slide, large type, minimal words,
  arrow-key/space nav. Built for projection and live delivery. Same tokens, same fonts,
  inverted information density.

## Hard rules (inherited from the skill)

1. **Self-contained** — inline CSS + vanilla JS. No network, no build step, no CDN.
   Opens with a single `open <path>`.
2. **Print-friendly** — a `@media print` block that flattens interactive state to a
   readable static document.
3. **Local only** — any persisted state goes to `localStorage` on the device; nothing is
   sent anywhere.
