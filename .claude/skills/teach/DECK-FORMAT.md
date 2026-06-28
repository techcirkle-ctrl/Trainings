# DECK-FORMAT — the per-week session decks + hands-on helper

The authoring spec for a week's session: **N projectable HTML decks** (one per act) in
`weeks/week-N-<theme>/01-workshop/`, plus **one circulated `hands-on-movements.md`** the
team copies prompts from. Read this before authoring them.

> Supersedes `KEYNOTE-FORMAT.md` and `run-of-show.md`. The session is no longer a markdown
> script — it is a set of **presenter-projected decks** built on **movements**.
>
> **RECONCILED (see `PLAYBOOK.md` §7 — shipment wins):** Week 1 actually shipped **two decks
> of the same slides — `…-audience.html` + `…-presenter.html`** (the presenter copy adds the
> per-slide script) — with **hands-on prompts inline behind copy buttons**, *not* the
> "3 act-decks + a separate `hands-on-movements.md` helper" model described below. Follow the
> shipped audience/presenter pattern unless a week deliberately revives the helper split.

## The model in one paragraph

A week's 5–6 hr session is delivered as **2–4 decks** (`deck-N-<slug>.html`) — one per
**act** (Deck 1 Fundamentals, Deck 2 Prompting, Deck 3 RAG & Agents) — that the trainer
projects and switches between, **plus one `hands-on-movements.md`** that every leader opens
on their own laptop to copy the starter prompts. The atomic unit across both is the
**movement** (~12–13 across the week). **Concept movements** live in the decks (a driveable
widget the trainer runs live). **Hands-on movements** live in the helper MD (copyable
prompts the leaders run). Each deck carries a short **bridge slide** at each hands-on
movement — goal + judgment + a pointer to the helper — so the deck walks the full arc while
the working detail sits in the MD. Everything **re-teaches from zero**; nothing assumes the
prework was done.

## Why split decks + a helper

- **Projection vs copy-paste don't mix.** A leader can't copy a long prompt off a projected
  slide. Decks are for the room's shared attention; the MD is for each laptop.
- **The MD is circulated.** One file the trainer sends round — leaders work from it during
  the hands-on movements and keep it after.
- **Separate decks per act** let the trainer open/close a clean unit per flow and keep each
  file small enough to load and edit fast.

## The movement — the unit

Every movement shares one shape: a **goal**, something the leader **does**, and the
**judgment they own**.

- **Concept movement (in a deck):** a dark **movement divider** (number · goal · "you'll
  decide"), then 1–2 panels teaching one idea through a **driveable widget** ported up from
  the prework (predictor, attention, stack composer, prompt builder, RAG on/off, agent
  loop, sorter). Close on a **Leader's read**.
- **Hands-on movement (in the helper MD + a bridge slide in the deck):** the MD section has
  the goal, the **copyable starter prompts** (the *floor* — run them, then push past), and
  the judgment. The deck's **bridge slide** states the goal + "you'll decide" + `→ Hands-On
  Helper · Movement N` so the room knows to switch to their laptops.

## Hard rules

1. **N decks + one helper.** `deck-N-<slug>.html` per act; one `hands-on-movements.md` for
   the whole week. Decks open with `open <file>`; the MD is circulated.
2. **Self-contained decks.** Inline `<style>` + vanilla `<script>`, no network/CDN/build.
   Each widget in its own IIFE with defensive guards. (Each deck re-inlines the shared
   engine CSS + only the widget CSS it uses — that duplication is the cost of self-containment.)
3. **Full-bleed slide.** One viewport = one panel; `overflow:auto` so a dense panel scrolls.
   Defer to `reference/DESIGN.md` for tokens/fonts/registers.
4. **Re-teach from zero.** Never "as you saw in the prework."
5. **The trainer talks; the panel supports.** On-glass text is a cue + visual, never a script.
6. **Movements grouped into the deck's act.** Tag slides `data-deck` + `data-mv`; the chrome
   shows "Deck 1 · M2 · …". Each deck opens with a title, a **mini-agenda** of its movements
   (hands-on tagged), and (Deck 1) the **cold open** — the keynote's job, absorbed.
7. **Hands-on lives in the MD, bridged from the deck.** Don't duplicate prompts onto slides;
   point to the helper. (Exception: a teaching widget like the data sorter may run live in
   the deck *and* the leaders build their own version in the MD.)
8. **Port the prework's hero interactions** verbatim where they exist (same data, sized up).

## Slide engine (copy from a reference deck)

- **Nav:** `→`/`Space`/`↓`/click-right = next; `←`/`↑` = prev; **`Home` = mini-agenda**;
  `End` = last.
- **Chrome:** movement label ("Deck 1 · M2 · …") + slide counter, low-corner, muted.
- **Registers:** muted "what is" (cold open) vs teal teaching; movement/act dividers dark.
- **Print:** `@media print` stacks panels and reveals notes.

## Speaker notes

- `N` (or `S`) toggles a notes panel; **hidden by default**. Pure CSS/JS.
- **Bullet cues, not a script** — 3–5 delivery beats per panel. This is where the old
  `run-of-show.md` talk-track lives.
- **Carry the operational gold** in the notes of the panel it applies to: per-movement
  timing, demo fallback, the **backup problem bank**, the "kill a weak idea with the bar"
  move. The pivot drops the roundtable *posture*, never these.

## The hands-on helper (`hands-on-movements.md`)

- **Audience: the leaders**, on their laptops. Opens with the posture + the tool (Claude
  Desktop, workspace account) + a one-row-per-movement table.
- One section per hands-on movement: **goal · "you'll decide" · the copyable starter
  prompts** (in fenced code blocks) · the judgment. British spelling, leader altitude.
- It is the participant-facing twin of the decks — keep the movement numbers identical.

## Reference implementation

`weeks/week-1-foundations/01-workshop/` is the de-facto template: `deck-1-fundamentals.html`
(M1–M5), `deck-2-prompting.html` (M6–M9), `deck-3-rag-agents.html` (M10–M13), and
`hands-on-movements.md` (M4, M5, M7, M8, M11, M13). Copy their engine, mini-agenda, chrome,
register coding, bridge-slide pattern, and ported widgets.

## Self-audit before shipping

- **Goal → do → judgment** in every movement; nothing passive.
- **Words on glass** pass "could the trainer say this, not show it?"
- **Widgets drive** — every ported interaction runs, every path exercised, state from the DOM.
- **Bridges match the MD** — every hands-on movement has a deck bridge slide *and* a helper
  section with the same number, and the prompts copy cleanly.
- **Re-teaches cold**; **mini-agendas** list exactly the movements that exist.
- **Notes carry delivery** + the operational gold is present.
- **Register + British spelling** — coded as the prework; behaviour, summarise, organised.
