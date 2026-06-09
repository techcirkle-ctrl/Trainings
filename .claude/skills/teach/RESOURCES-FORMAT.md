# Resources Format

`ai-capability-program/RESOURCES.md` is the **single source of truth** for every external link used in a lesson. Lessons cite an entry by its **ID**; they never hardcode a duplicate URL. Principle: never trust parametric knowledge — ground every claim in a high-trust source.

## Structure

A table, one row per source:

```md
| ID | Source | Type | Used in | URL |
|----|--------|------|---------|-----|
| R1 | Google Cloud — Introduction to Generative AI | Course (~1 hr) | W1 preread 1 | https://… |
| R5 | Anthropic — Building Effective Agents | Engineering article | W2 preread 1 | https://… |
```

Optionally followed by a `## Gaps` section listing knowledge the program needs but has no good source for yet — this drives future search.

## Rules

- **High-trust only.** Primary sources, recognised vendors (Google, Anthropic, DeepLearning.AI), peer-reviewed or first-party docs. No marketing-as-education.
- **Stable IDs.** Once an ID is assigned (R1, R2 …), don't renumber it — lessons link to it. Add new sources with the next free number.
- **Annotate "Used in".** Track which lesson(s) depend on each row, so a dead link's blast radius is visible.
- **Verify before launch.** Confirm every URL resolves before the Week-0 preread email goes out. Flag any approximate/landing-page link to be pinned to the exact resource.
- **Prune, don't bury.** A source that proved shallow or wrong is removed, not left in. Five sharp sources beat thirty mediocre ones.
- **Knowledge vs Wisdom.** Course/article/doc rows are Knowledge. Communities/forums (the wisdom layer) can live in a separate `## Wisdom (Communities)` list with the same annotate-every-entry rule.
