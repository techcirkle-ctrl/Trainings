# Glossary Format

`ai-capability-program/reference/glossary.html` is the **authoritative vocabulary** of the program — the compressed, revisited layer leaders keep on the desk. Once a term is defined here, every lesson uses it the same way. It is HTML (not markdown) so it shares the lessons' look and prints cleanly.

## Conventions

- **Self-contained HTML**, same restrained visual system as the lessons. Opens with `open "glossary.html"`. Prints to one or two pages (`@media print` with `break-inside: avoid` on term cards).
- **Term cards**, each: the term (+ expansion / "also known as"), a **1–2 sentence** plain-language definition, and — where relevant — a one-line tie to the structure of the program (e.g. "Layer 3 of the AI Evolution Stack").
- **Leader-level language.** Define for a senior non-engineer. No jargon inside a definition unless that jargon is itself a glossary term.
- **Grows weekly.** Start with Week 1's terms; each week's lessons add the terms they introduce. The header should say it grows each week.

## Rules

- **Add on introduction.** When a lesson introduces a term, add it to the glossary in the same session. Lessons defer to these definitions — they don't redefine.
- **Opinionated and tight.** One clear definition per term. If a term is used two ways in the program, pick one and note the other explicitly; don't leave it ambiguous.
- **Use glossary terms inside definitions.** Cross-reference rather than re-explaining — it reinforces the shared language.
- **Revise as understanding deepens.** If a definition turns out to be loose or wrong, fix it; the glossary is authoritative, so a stale entry pollutes every lesson.
