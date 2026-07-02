# PRESENTER-DECK KICKOFF — reusable prompt (any week)

> **How to use:** start a NEW chat, attach this file, and send it. The assistant's FIRST action
> is to ask which week. Answer with a number or name; it resolves the week and builds the
> presenter deck from that week's finished AUDIENCE deck.

---

## STEP 0 — ASK FIRST, BUILD LATER

Before doing anything else, ask me exactly one question and then STOP and wait:

> **"Which week are we building the presenter deck for? (number or name)"**

When I answer, resolve the week `N` from this map, confirm it back to me in one line, then name
this session **"Week N presenter deck"** and proceed:

| N | Theme / folder |
|---|---|
| 1 | `week-1-foundations` |
| 2 | `week-2-agentic-deep-dive` |
| 3 | `week-3-handson-building` |
| 4 | `week-4-build-and-lead` |

Everywhere below, substitute the real number/theme for `N` and `<theme>`.

---

## THE TASK

Build the Week `N` **presenter deck** for the AI Capability Program (Sandvik GCC) by adding a
per-slide presenter script to that week's **finished audience deck**. Work in this repo and this
working tree (do NOT create a fresh worktree/branch — you need the on-disk playbook + deck files).
Do NOT commit anything unless I explicitly say so.

## THE PRIMARY GUIDE (governs HOW you build)
`.claude/skills/teach/PRESENTER-DECK-PLAYBOOK.md` — the source of truth for presenter decks.
Follow it exactly: persona (§1), doctrine (§2), the two inputs (§3–§4), the conversion map (§5),
the script-block blueprint (§6), writing each field (§7), the verbatim plumbing (§8), the five
archetypes (§9), voice (§10), browser-verify (§11), the 95% fidelity checklist (§12), the worked
example (§13), and the reuse rules (§15: reuse the plumbing, write every script fresh).

## THE INPUTS
- **Input A (primary — the frozen surface):** the finished Week `N` audience deck,
  `ai-capability-program/weeks/week-N-<theme>/01-workshop/deck-week-N-<theme>-audience.html`.
  This is copied UNCHANGED; the script is added on top.
- **Input B (the voice source, if it exists):** the week's facilitator run-sheet / trainer notes
  in `.../01-workshop/` (Week 1: `Week1_Facilitator_RunSheet.pdf` + `my_notes.md`). Mine for
  verbatim Say lines, timings, demo data, coverage rule, contingencies. If none exists, write the
  scripts from Input A alone (voice the Takeaways + on-glass cues; set timings from the day-plan).

## IGNORE stale/irrelevant files
Any `*-REGEN.html` artifact, the `region.html` test sample, and the `*-FORMAT.md` docs
(superseded — the playbook is the only authority).

## THE OUTPUT
One self-contained HTML file, a copy of the audience deck plus the script layer, saved in the
same `01-workshop/` folder. **Name it by taking the week's real `…-audience.html` filename and
replacing the single word `audience` with `presenter` — nothing else** (e.g.
`deck-week2-agentic-audience.html` → `deck-week2-agentic-presenter.html`). Do NOT invent a name
from a generic pattern; the presenter file is the exact twin of the audience file. If a presenter
file of that name already exists, overwrite it.
Inline CSS + vanilla JS, no network/build. `@media print` shows the script inline and drops
chrome/notes/panels.

## THE METHOD (per playbook §5)
1. Copy the audience deck to the output filename, UNCHANGED. Every later edit is additive.
2. Freeze the surface: touch no slide markup, widget, `.read`, `.goalrow`, prompt, or `.note`.
3. Add the §8 plumbing once (verify the dormant CSS shell is present; add only what's missing:
   the `<aside class="scriptpanel">`, the JS wiring, the helpbar `S`, the print `.script` rule,
   the header comment).
4. Walk every `<section>` in order. Insert exactly ONE `<div class="script">` immediately after
   that slide's `.note`, before `</section>`. Slide count = script count, no slide skipped.
5. Each script = Remember → Move → Say → Do → Bridge (§6). Shape it by archetype (§9). Voice per
   §7/§10. Pull run-sheet verbatim where it maps.

## THE GATE — do NOT write all 47 scripts until I approve the first act
First, add the plumbing and write the scripts for the FIRST ACT only (the front matter + Act 1),
and show me. I'll check the voice and the freeze. ONLY THEN write the rest, act by act, showing me
as you go.

## BUILD + VERIFY (per playbook §11)
- Host static server + preview_eval harness: walk `→` through ALL slides; on each, press `S` and
  read back `#scriptBody` — confirm EVERY slide has a non-empty script (no "No script…"), with
  Remember/Move/Say/Bridge present and Do where the archetype needs it.
- Confirm `S` toggles the dock, `N`/`Esc` close it, deck + chrome track `--scriptw`, close button
  works, 0 console errors, and widgets still drive (they're untouched).
- Confirm `@media print` stacks every slide with the script inline as a white card.
- Clear the §12 fidelity checklist. Then stop and let me review.

## STYLE OF OUR CONVERSATION
Keep answers short and in clearly-labelled sections, simple language. Recommend decisively; don't
ask permission for every small choice. Do not commit.

---

**Begin now with STEP 0: ask which week, then wait for my answer.**
