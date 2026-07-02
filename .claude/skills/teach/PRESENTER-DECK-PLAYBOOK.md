# PRESENTER-DECK PLAYBOOK
### The primary source of truth for turning a week's finished audience deck into the trainer's presenter deck

> **The job in one sentence:** hand me a week's **finished audience deck** (and its
> **facilitator run-sheet / source notes** where they exist), and by following this playbook I
> produce the **presenter deck** — the *same* deck, byte-for-byte on the glass, with a
> per-slide **presenter script** (Remember → Move → Say → Do → Bridge) docked behind the `S`
> key — at least **95% identical to the audience deck in slides and content**, looking and
> teaching exactly like the Week 1 presenter deck, or better.

This playbook is **only about one transformation**:

```
   (finished audience deck HTML)  +  (facilitator run-sheet / notes)   ─────►   presenter deck HTML
        the frozen surface              the trainer's voice & timing            the same deck + a script layer
```

It is **not** a deck-authoring guide (that is `AUDIENCE-DECK-PLAYBOOK.md`'s job) and it does
**not** re-derive a single slide, widget, word, or Takeaway. It **adds a script layer and
nothing else.** Everything the audience already sees stays *exactly* as it is — that is the
whole point, and it is what guarantees the 95%.

**Calibration target (the benchmark):** the shipped
`weeks/week-1-foundations/01-workshop/deck-week1-foundations-presenter.html`, measured against
its own audience twin `deck-week1-foundations-audience.html`. Everything here is
reverse-engineered from how those two files differ. **The measured truth of that pair — the
contract this playbook must reproduce:**

- **47 slides in both. Identical.** Same order, same registers, same widgets, same on-glass copy.
- **47 Takeaway `.note` blocks in both. Identical.** The presenter deck does **not** touch the
  Takeaways.
- **47 `.script` blocks in the presenter, 0 in the audience.** **Exactly one script per slide —
  1:1, no slide skipped, no slide doubled.**
- **Do is near-universal — 45 of the 47 scripts carry a Do.** Only the two barest movement
  dividers omit it. Even the title, the act-openers, and the dark dividers get a **one-line
  stage Do** (a watching question to pose the room, a tone/timing directive, or a
  "collect the artefact" note). Treat a Do-less script as the rare exception, not the default.
- The *only* other differences are five pieces of **plumbing** (§8): the print rule that shows
  the script on paper, the `<aside class="scriptpanel">`, the JS wiring, the helpbar `S` entry,
  and the header comment.

The bar: re-run this playbook on any week's audience deck and reproduce a presenter deck that
is **≥95% identical to that audience deck** (it can only differ by the added script layer +
plumbing) **and** whose scripts read like Week 1's.

**Ignore the stale format docs.** `DECK-FORMAT.md`, `KEYNOTE-FORMAT.md`, `LESSON-FORMAT.md`,
`PLAYBOOK.md`'s older per-artifact notes, and the other `*-FORMAT.md` files describe superseded
models (the "3 act-decks + a hands-on-movements.md helper", the standalone `keynote.html`).
Week 1 shipped **two decks of the same 47 slides** — audience + presenter — and that is the
only model. Do not cite, follow, or reconcile against the stale docs. When in doubt, **open the
Week 1 presenter deck and copy how it does the thing.**

---

## 0. How to use this playbook

You are given **one primary input** — the week's **finished audience deck HTML** — and, where
they exist, a **secondary input**: the week's **facilitator run-sheet / trainer notes** (Week 1
= `Week1_Facilitator_RunSheet.pdf` + `my_notes.md`). Then, in order:

1. Read **§1 Persona** and **§2 Doctrine** — *who you are* and *the beliefs that don't bend*.
2. Run **§5 the conversion map** to lock the two rules that protect the 95% (freeze the
   surface; one script per slide) and to plan where each script's *content* comes from.
3. Add the **§8 plumbing** verbatim (most of the CSS shell is already dormant in the audience
   deck — verify, add only what's missing).
4. Write one **§6 script block** per slide, field by field to **§7**, in the **§10 voice**,
   differentiated by slide archetype per **§9**.
5. **Verify in the browser** (§11), then clear the **§12 fidelity checklist** — including the
   machine diff that proves ≥95%.

Everything is in this one file. §13 shows the method applied to two Week 1 slides end to end.

---

## 1. The persona — who you are when you build this

You are a **master session director** writing the **trainer's private earpiece** for a
six-hour, hands-on room — not a slide author (the slides are done and frozen), not a scriptwriter
inventing new teaching. Hold this voice:

- **You touch the script, never the slide.** The audience deck is a finished, signed-off
  artifact. Your entire job is the layer *behind* the `S` key. If you find yourself editing a
  headline, a widget, a `.read` band, or a Takeaway, **stop** — you have left your lane and
  broken the 95%.
- **You are the calm expert in the trainer's ear.** The Week 1 room is five senior leaders; the
  posture is *calm expert who respects their seniority*, not high-energy L&D. The script must
  sound like that — measured, precise, never chirpy. (Straight from the run-sheet.)
- **You write what the trainer *says* and *does*, not what the slide shows.** The slide is the
  cue; the script is the performance. Every script re-teaches the slide's idea out loud, in the
  trainer's first-person voice — it never says "read the slide."
- **You give timing and stage directions, not just words.** A presenter script that omits *how
  long* and *what to click* is half a script. Every block carries a **Move** (timing + intent)
  and, where the slide is a widget or hands-on, a **Do** (the exact controls to drive, who to
  call on, the backup bank).
- **You keep the trainer one step ahead.** Every script ends with a **Bridge** — the sentence
  that launches the next slide — so the trainer never stalls at a transition.
- **You mine the run-sheet for gold and put it where it belongs.** Verbatim demo lines, the
  confidence-read wording, the "why are we here for four weeks?" beat, contingency answers,
  the coverage rule — these live in the script, never on the glass.

If a script would leave the trainer guessing what to say, how long to spend, or what to click,
it is not finished. Rewrite it.

---

## 2. Doctrine — the beliefs that don't bend (presenter edition)

1. **The surface is frozen.** The presenter deck's 47 slides are the audience deck's 47 slides,
   unchanged — every heading, widget, `.read` band, `.goalrow`, prompt block, and **Takeaway
   note**. The script is *additive*. This is the rule that earns the 95%.
2. **One script per slide, every slide.** No slide ships without a `.script`; no slide gets two.
   47 slides → 47 scripts. A title slide gets one; a divider gets one; a dense widget slide gets
   one.
3. **The script is where the presenter's words go — the glass stays a cue.** Anything that reads
   like a paragraph, a talk-track, a contingency, or a stage direction belongs in the script,
   never on the slide. (This is the mirror of the audience deck's "prose lives in the Takeaway".)
4. **Re-teach out loud from zero.** The **Say** voices the idea as the trainer would speak it —
   it does not read the slide aloud and does not say "as the slide shows."
5. **Timing is part of the script.** Every **Move** carries a duration or an energy note
   ("~30 sec", "~8 min", "slow down here", "shortest act — keep it tight"). The day is a 5-hour
   clock; the scripts must add up to it.
6. **Drive directions are exact.** For every widget slide the **Do** names the controls to
   toggle *in order* and what to point at; for every hands-on slide it names the timing, the
   circulate-and-harvest move, and the **backup bank** so no leader stalls.
7. **The voice is the room's voice.** British spelling, executive register, calm-expert posture.
   The Week 1 room is named in the run-sheet (MD · Finance Head · HR Head · HR Deputy · one more
   lead) — pitch the Say to *that* altitude.
8. **The run-sheet is the source of truth for the open and the demo.** Where the run-sheet gives
   verbatim lines (the March bridge, the 1–5 confidence read, the vendor-quote demo, the
   coverage rule), the script uses them — that is the trainer's tested wording.
9. **Contingencies live in the Do.** "If asked whose job the data cleanup is…", the backup
   problem bank, "if the two prompts land too close, make the vague one lazier" — the hard-won
   facilitation gold goes in the **Do** bullets of the slide it applies to.
10. **The Takeaway and the script are different organs.** The Takeaway (kept, unchanged) is the
    one-line *landing* for the reader of the audience copy; the script is the trainer's *full
    delivery*. Never delete or rewrite the Takeaway to make room for the script — they coexist,
    script immediately after note.
11. **Self-contained; local-only; prints clean; British spelling.** Always. The script prints as
    an inline white card (the trainer's paper script); the Takeaway and chrome drop on print.

---

## 3. Input A — anatomy of the finished audience deck

The audience deck is your **frozen canvas and your richest content source at once**. Every part
of a slide tells you what its script must carry. Mine each slide, change none of it:

| Audience-slide element | What it gives the script |
|---|---|
| **Slide register** (`.act` / `.dark` / `.isnow` / paper) | The **archetype** (§9) — which sets the shape of Move and whether a Do is needed. |
| **Kicker + `h1.big`/`h2.head`** | The slide's subject — the spine of the **Say** and the **Remember** hook. |
| **`.goalrow` (Goal / You'll decide)** | On a dark divider: the **Say** frames the goal and the call; **Remember** compresses it. |
| **The ported widget** (`.pb`/`.temp`/`.ragm`/`.agent2`/`.build`…) | The **Do** — the exact control paths to drive live, in order, with what to point at. |
| **`.read` band** (Leader's read) | The **Remember** hook and the closing beat of the **Say** — the call they own. |
| **Hands-on block** (`.hobadge`/`.hodo`/`.hostep`/`.promptblock`) | The **Do** — timing, the copy-the-block instruction, circulate/harvest, the backup bank. |
| **Finale stepper** (`.stepper`/`.steppanel`) | The **Do** — the enrich → run → capture rhythm and which sub-step to walk on the TV. |
| **Takeaway `.note`** | The seed of the **Say** — expand the note's one line into the spoken talk-track (do **not** move or delete the note). |
| **The next slide's kicker/title** | The **Bridge** — the line that launches it. |

> The audience deck sets the **content contract** (what is taught, in what order, with what
> widget). The script never renegotiates it — it *performs* it.

---

## 4. Input B — the facilitator run-sheet & trainer notes (the voice source)

Where a week has a **facilitator run-sheet** (Week 1: `Week1_Facilitator_RunSheet.pdf`) and/or
**trainer notes** (`my_notes.md`), they are the **voice and timing source** — the trainer's own
tested wording. Mine them for the script; never for the slide.

| Run-sheet / notes element | Becomes, in the script |
|---|---|
| The **posture** ("calm expert… energy from the content, not working the room") | The register of every **Say**; the tone note in early **Move**s. |
| **Verbatim "Say" lines** (the March bridge, the confidence read, the demo beats) | The **Say**, used close to verbatim on the slides they map to (open, cold-open, demo). |
| **Timings** (10:00 0–3 min, 11–15 min…) | The **Move** durations; the day-plan the scripts must sum to. |
| **Demo data / prompts** (the vendor-quote reconciliation) | The **Do** of the demo slide — what to paste, the wifi-failure backup, the "make the vague one lazier" contingency. |
| **The coverage rule** ("a second person floats… within ~60 seconds") | A **Do** bullet on the hands-on slides. |
| Contingency Q&A ("if asked whose job the data cleanup is…") | **Do** bullets — "If asked X:" on the slide it would come up. |
| The **realistic Day-1 promise** (spec, not a built agent) | Keeps the **Say** honest at the open and the close. |

> If a week has **no** run-sheet, the script is written purely from Input A — voice the
> Takeaway and the on-glass cue as spoken lines, and set timings from the audience deck's
> day-plan slide. The run-sheet makes the script *sharper*; it is not required to make it.

**Excluded / stale inputs (do not read as sources):** any `*-REGEN.html` artifact, the
`region.html` test sample, and the stale `*-FORMAT.md` docs. If you are unsure whether a file is
a source, ask the trainer before reading it into the script.

---

## 5. The conversion map — audience deck → presenter deck (do this first)

This is the contract. It is far simpler than the audience playbook's, because **structure and
content are already decided — you are not converting them, you are preserving them.** Two rules
protect the 95%; the rest is writing scripts well.

**Step 0 — copy the audience deck to the presenter filename, unchanged.** **Derive the presenter
filename from the actual audience filename — take the week's real `…-audience.html` file and
replace the single word `audience` with `presenter`, changing nothing else** (e.g.
`deck-week2-agentic-audience.html` → `deck-week2-agentic-presenter.html`). Do **not** invent a
name from the `deck-week-N-<theme>-presenter.html` pattern — that pattern is only a shape;
whatever the audience deck is actually called on disk is the truth, and the presenter file must be
its exact twin with `audience`→`presenter`. Save it in the same `01-workshop/` folder. Every edit
from here is *additive*. If your diff against the audience deck ever shows a *deletion* or a
*change* to slide content, you have made a mistake — revert it. (Header comment is the one allowed
content edit — §8.)

**Step 1 — freeze the surface (the first rule).** Do not touch: any `<section>`'s slide markup,
any widget, any `.read`/`.goalrow`/`.hodo`/`.promptblock`, or any **Takeaway `.note`**. The
machine diff at the end (§11–12) must show **zero** changes to these. This single rule is what
guarantees ≥95%.

**Step 2 — one script per slide (the second rule).** Walk the deck section by section. For each
`<section>`, insert exactly one `.script` block **immediately after that slide's `.note`**, just
before `</section>`. 47 slides → 47 scripts. Never skip, never double.

**Step 3 — plan each script's content source.** For each slide, note in a one-line plan where
its Say/Do come from:
- **Say** ← the Takeaway note (expanded to spoken form) + the run-sheet's verbatim line if one
  maps to this slide + the on-glass cue voiced.
- **Do** ← the widget's control paths (read them off the audience widget) / the hands-on
  facilitation + backup bank / the finale stepper rhythm / the run-sheet's demo & contingencies.
- **Remember** ← the slide's `.read` band or core thesis, in one line.
- **Move** ← the slide's archetype (§9) + its timing from the day-plan / run-sheet.
- **Bridge** ← the next slide's kicker/title.

**Step 4 — add the plumbing (§8) once.** The aside, the JS wiring, the helpbar `S`, the print
rule. Verify the dormant CSS shell is present; add any missing piece.

**Step 5 — verify + diff.** Browser-drive the `S` panel across all 47 slides; run the machine
diff; confirm the only changes are the 47 scripts + the five plumbing pieces.

**The mapping rule of thumb:**

```
For each of the deck's N slides (unchanged):
    keep everything on the glass, keep the .note
    insert, right after .note:
      <div class="script">
        Remember  ← the slide's one-line thesis (.read / core claim)
        Move      ← archetype + timing/energy
        Say       ← the Takeaway voiced + run-sheet verbatim + cue spoken   (1–3 paras)
        Do        ← widget drive-path / hands-on facilitation + backup / finale rhythm  (bullets; optional on pure framing slides)
        Bridge →  ← the line into the next slide
      </div>
Add once: scriptpanel aside · JS wiring · helpbar S · print .script rule · header comment
```

A 47-slide audience deck → a 47-slide presenter deck with 47 scripts. **Match the count exactly**
— if your presenter deck has fewer scripts than slides, you have under-built; if it has more
slides or different slides than the audience deck, you have broken the freeze.

---

## 6. The script-block blueprint (every slide, in this order)

A **script block** is the atomic unit — one per slide. It is a single `<div class="script">`
placed **immediately after the slide's `.note`**, containing five fields in this fixed order.
Copy the exact markup shape from Week 1:

```html
<div class="script">
  <div class="lead1"><span class="k">Remember</span>[one-line thesis — the single thing to hold]</div>
  <div class="t">Move</div><p>[timing + facilitation intent — what this slide does, how long, what energy]</p>
  <div class="t">Say</div><p>"[verbatim first-person talk-track, executive register, British spelling]"</p>
  <p>"[further Say paragraphs as the slide needs — 1 to 3 total]"</p>
  <div class="t">Do</div><ul><li>[exact stage direction]</li><li>[timing / who to call on / backup / contingency]</li></ul>
  <div class="t">Bridge &rarr;</div><p>[the line that launches the next slide]</p>
</div>
```

Field rules:

1. **Remember** — *always present.* One line, in the `.lead1` band with `<span class="k">Remember</span>`.
   The slide's payload compressed to a sentence the trainer can glance at. Declarative, not a cue
   to the audience. (Ex: "The cheapest layer that works, wins.")
2. **Move** — *always present.* One short paragraph: what to *do* with the slide + timing/energy.
   (Ex: "The most important framing of the day — the posture and the tool. Slow down here.")
3. **Say** — *always present.* One to three quoted paragraphs, first-person, the words the
   trainer speaks. British spelling; `<em>…</em>` on the words to stress. Re-teaches; never reads
   the slide.
4. **Do** — *present on nearly every slide (Week 1: 45 of 47).* Widget / hands-on / demo /
   finale slides get the full drive-path or facilitation Do. **Framing slides — title,
   act-openers, dark dividers, cold-opens, stuck, close — still get a one-line stage Do:** a
   *watching question* to pose the room ("as I build this, ask which of these your work needs"),
   a *tone/timing directive* ("shortest act — keep it tight"), a *"collect the artefact"* note
   where the slide produces one, or an *"If asked X:"* contingency. **Omit Do only on a
   genuinely bare divider with nothing to stage — at most one or two in a whole deck.** When in
   doubt, write the one-line Do. Bulleted stage directions: controls to toggle *in order*, what
   to point at, timings, who to call on, backup bank, "If asked X:" contingencies.
5. **Bridge →** — *always present.* One line (usually quoted) into the next slide. The last
   slide's Bridge is a sign-off ("(End of Week 1.)").

Keep the rhythm identical across all 47: **hold this → do this for this long → say this →
click/circulate this → launch the next.**

---

## 7. Writing each field well

### 7a. Remember — the one thing to hold
- One sentence. The slide's thesis, not a summary of the slide. If the slide has a `.read` band,
  the Remember is usually a tighter paraphrase of it.
- Written *to the trainer* as a **declarative thesis** — third-person about the room ("they leave
  owning a real problem") or a bare principle ("the cheapest layer that works, wins"). Use second
  person only for a principle the *leader* owns ("you don't tune the model — two choices are
  yours"); never address the room with an instruction ("your team should…", "list your data").
- Examples from Week 1: "A production prompt has six parts; Task is the only must-have." ·
  "Vague invents and over-promises; structure refuses to guess — that gap is your risk." ·
  "The agent only touches you where its authority runs out — that's the governance call."

### 7b. Move — timing + intent
- Lead with the *action verb* for the slide ("Set the contract…", "You drive the builder…",
  "They work; you circulate…", "Mark the pivot…").
- Always include a duration or energy note: "~30 sec, energy up" · "~8 min" · "slow down here" ·
  "shortest act — keep it tight" · "under 90 seconds, then straight to the widget".
- Name *who acts*: trainer-drives ("You drive…"), room-does ("They work…"), or trainer-frames
  ("Give them the map…").

### 7c. Say — the verbatim talk-track
- **First person, in quotes, spoken register.** This is what comes out of the trainer's mouth.
- **Re-teach, don't read.** Voice the idea; never "as you can see on the slide."
- **1–3 paragraphs.** A framing slide is one paragraph; a heavy concept (the engine, the RAG
  demo, a finale step's rhythm) may run three.
- **Use the run-sheet verbatim where it maps** — the March bridge, the confidence read, the
  "that's a good answer — so why are we here for four weeks?" beat are already tested; use them.
- **Stress with `<em>`** the two or three words that carry the point ("specificity is
  *control*", "*out-judge* it", "it *refuses*").
- **British spelling, executive altitude** — behaviour, summarise, organised, prioritise; pitch
  it to a senior leader, never to a beginner.

### 7d. Do — the stage directions
- **Widget slides:** name the controls to toggle **in order**, and what to point at.
  (Ex: "Toggle in order: Task → Role → Context → Constraints → Format → Examples. Pause on the
  Constraints and Examples jumps and point at them.")
- **Hands-on slides:** the timing ("~8 min"), the circulate-and-harvest move ("Circulate while
  they work. Then pull 2–3 leaders to read out…"), the **coverage rule**, and the **backup bank**
  ("Blank page? Procurement→RAG · AP invoice triage→Agent…").
- **Demo slides:** what to paste, the order, the wifi-failure backup, the "make the vague one
  lazier" contingency.
- **Finale-step slides:** the enrich → run → capture rhythm ("Add text content → title it →
  paste → save; then one-line trigger"), and which leader's output to run on the TV.
- **Contingencies:** fold hard-won Q&A in as "If asked X: …" bullets on the slide it would arise.
- **Framing slides (title, act-openers, dark dividers, cold-opens, stuck, close):** still give a
  **one-line Do** — the *watching question* the room should hold while you teach, a *tone/timing
  directive* ("shortest act — keep it tight", "slow down and kill the ladder image"), a
  *"collect the artefact"* note where the slide produces one, or an *"If asked X:"* contingency.
- Omit **Do** only on a genuinely bare divider with nothing to stage — no more than one or two in
  a whole deck. When in doubt, write the one-line Do.

### 7e. Bridge → — the launch into the next slide
- One line, usually quoted, that the trainer says as they advance.
- It should name or tee up the *next* slide's subject ("Now the one map that carries the whole
  program — the stack." → next slide is the stack).
- The final slide's Bridge is the day's sign-off, not a transition.

---

## 8. The plumbing (add verbatim — most of the CSS is already dormant)

The presenter deck differs from the audience deck by the **47 scripts (§6)** plus **five pieces
of plumbing**. Crucially, **the CSS shell is usually already present in the audience deck as
dormant hooks** (Week 1's audience deck already carries `--scriptw`, the `.scriptpanel` CSS, the
`.lead1` CSS, `body.script-open` rules, and the `.note,.script{display:none}` hide). **Verify
each is present; add only what is missing.** Then add the five active pieces.

**8.1 — The `--scriptw` token** (in `:root`; usually already there):
```css
--scriptw:min(460px,42vw);
```

**8.2 — Hide `.script` on screen** (line ~27; usually already there — note it hides *both*):
```css
.slide.active{display:flex}.note,.script{display:none}
```

**8.3 — The docked side-panel CSS** (usually already dormant in the audience deck — verify the
whole block is present, add if not):
```css
/* presenter script — docked side-by-side (S), not an overlay */
.deck,.chrome{transition:right .25s ease}
body.script-open .deck{right:var(--scriptw)}
body.script-open .chrome{right:var(--scriptw)}
.scriptpanel{position:fixed;right:0;top:0;bottom:0;width:var(--scriptw);z-index:38;background:#10211f;color:#dcebe9;transform:translateX(100%);transition:transform .25s ease;box-shadow:-8px 0 30px rgba(0,0,0,.35);display:flex;flex-direction:column;border-left:3px solid var(--accent)}
body.script-open .scriptpanel{transform:none}
.scriptpanel header{padding:14px 20px;border-bottom:1px solid #1d3a39;display:flex;justify-content:space-between;align-items:center}
.scriptpanel header .b{font:700 12px ui-sans-serif,system-ui,sans-serif;letter-spacing:.1em;text-transform:uppercase;color:#7fd1cb}
.scriptpanel header .x{cursor:pointer;color:#7fd1cb;font-size:18px;background:none;border:0;line-height:1}
.scriptpanel .body{padding:16px 20px;overflow:auto;font:14.5px/1.55 ui-sans-serif,system-ui,sans-serif}
.scriptpanel .body p{margin:.4em 0}.scriptpanel .body ul{margin:.2em 0 .8em;padding-left:1.1em}.scriptpanel .body li{margin:.3em 0}
.scriptpanel .body em{color:#7fd1cb;font-style:normal;font-weight:700}
.scriptpanel .body .t{font:700 11px ui-sans-serif,system-ui,sans-serif;letter-spacing:.08em;text-transform:uppercase;color:#8aa6a2;margin:.8em 0 .15em}
.lead1{background:var(--accent-soft);border-left:3px solid var(--accent);border-radius:0 8px 8px 0;padding:9px 13px;margin:0 0 .8em;font:700 13.5px/1.45 ui-sans-serif,system-ui,sans-serif;color:#0d3b39}
.lead1 b{color:var(--accent)}
.scriptpanel .body .lead1{background:rgba(127,209,203,.14);color:#eafaf8;font-size:15px}
.scriptpanel .body .lead1 .k{display:block;font:800 10px ui-sans-serif,system-ui,sans-serif;letter-spacing:.1em;text-transform:uppercase;color:#7fd1cb;margin-bottom:3px}
.lead1 .k{display:block;font:800 10px ui-sans-serif,system-ui,sans-serif;letter-spacing:.1em;text-transform:uppercase;color:var(--accent);margin-bottom:3px}
```

**8.4 — The print rule that shows the script on paper** (this *is* presenter-only — add it inside
the existing `@media print` block, and add `.scriptpanel`/`.note`/`.stepcue` to the print
hide-list so the panels and Takeaways drop but the inline script shows):
```css
/* inside @media print — drop everything that isn't slide content or the presenter script */
.chrome,.helpbar,.progress,.notes,.scriptpanel,.promptblock .copy,.note,.stepcue{display:none!important}
/* presenter script — white card so it reads on any slide background */
.script{display:block!important;background:#fff!important;color:#26323d!important;margin-top:7px!important;padding:7px 11px!important;border:1px solid var(--line)!important;border-left:3px solid var(--warn)!important;border-radius:6px!important;font-size:9.5px!important;line-height:1.34!important}
.script::before{content:"SCRIPT — presenter only";display:block;font:700 8.5px ui-sans-serif,system-ui,sans-serif;letter-spacing:.1em;color:var(--warn);margin-bottom:4px}
.script .lead1{font-size:11px!important;padding:6px 10px!important;margin:0 0 .5em!important}
.script .t{font-weight:700;text-transform:uppercase;color:var(--warn);font-size:8.5px;margin:.4em 0 .08em}
.script p{margin:.16em 0}.script ul{margin:.1em 0 .35em;padding-left:1em}.script li{margin:.1em 0}.script em{color:var(--ink);font-style:normal;font-weight:700}
```

**8.5 — The `<aside>` panel** (presenter-only; place it right after the notes `<aside>`, near the
end of `<body>`):
```html
<aside class="scriptpanel" id="script"><header><span class="b" id="scriptBeat">Script</span><button class="x" id="scriptClose">✕</button></header><div class="body" id="scriptBody"></div></aside>
```

**8.6 — The helpbar `S` entry** (presenter-only; add `S script` to the existing helpbar):
```html
<div class="helpbar">→ next · ← back · <b>Home</b> agenda · <b>N</b> notes · <b>S</b> script · <b>F</b> full-screen</div>
```

**8.7 — The JS wiring** (presenter-only; four edits to the existing engine `<script>`):
```js
// (a) declare the panel refs alongside body — replace `var body=document.body;`
var scriptBody=document.getElementById("scriptBody"),scriptBeat=document.getElementById("scriptBeat"),body=document.body;

// (b) in syncNotes(), after the notes lines, mirror the slide's .script into the panel:
var sc=s.querySelector(".script");scriptBody.innerHTML=sc?sc.innerHTML:"<p class='muted'>No script for this slide yet.</p>";scriptBeat.textContent=lbl(s);

// (c) in the keydown handler — N and Esc also clear script-open; add the S toggle:
else if(e.key==="n"||e.key==="N"){notes.classList.toggle("open");body.classList.remove("script-open");}
else if(e.key==="s"||e.key==="S"){body.classList.toggle("script-open");notes.classList.remove("open");}
else if(e.key==="Escape"){notes.classList.remove("open");body.classList.remove("script-open");}

// (d) wire the panel's close button:
document.getElementById("scriptClose").onclick=function(){body.classList.remove("script-open");};
```

**8.8 — The header comment** (the one allowed non-script content change — update the top-of-file
HTML comment to describe the presenter deck, mirroring Week 1's wording).

That is the *complete* set of differences. If your diff shows anything outside §6 scripts +
§8.1–8.8, you have drifted.

---

## 9. The five slide archetypes and how their scripts differ

Every slide is one of five archetypes (read it off the register + content). The script's
**Move/Do** shape follows the archetype; **Remember/Say/Bridge** are always present.

| Archetype | How to recognise it | Move | Say | Do |
|---|---|---|---|---|
| **Front-matter / framing** (`.slide.active` title, `.isnow` day-plan, mini-agenda, how-today-works, cold-open, stuck, close) | Muted/wash register, no widget | Short, ~30–45 sec, tone note | 1–2 paras; the run-sheet's open lines live here | **One-line Do** — the watching question, a tone/timing directive, hold for laptops, or point at the day-plan/agenda |
| **Dark movement divider** (`.slide.dark`, `.goalrow`) | Deep-teal, Goal + You'll decide | "Frame the goal / mark the pivot", short | 1–2 paras framing the goal + the call they own | **One-line Do** — the watching question for the widget/hands-on that follows, or a tone/timing directive; omit only on a truly bare divider |
| **Concept widget panel** (paper, a `.lab` widget) | Teaching surface with a driveable widget | "You drive…", the widget's tempo | 1–3 paras re-teaching through the widget | **Required** — controls to toggle *in order*, what to point at |
| **Hands-on** (`.hobadge`, `.hodo`, `.promptblock`) | Hands-on badge + copyable prompts | "They work; you circulate…", ~6–12 min | 1–2 paras — the task, the one question to answer | **Required** — timing, circulate/harvest, coverage rule, **backup bank** |
| **Finale step** (`.stepper`/`.steppanel`) | Capstone Decider step, in-slide stepper | "Establish/repeat the enrich→run rhythm", timing | 2–3 paras — the rhythm + what they get | **Required** — enrich→run→capture; which leader's output to run on the TV |

Match the archetype and the script writes itself into the right shape.

---

## 10. Voice & copy

- **British spelling, executive register, calm-expert posture.** The room is senior; the voice
  respects that. Energy comes from the content landing, not from performing.
- **Say is spoken, not written.** Contractions, direct address, the rhythm of speech. Read it
  aloud — if it sounds like a document, rewrite it.
- **Re-teach, never read the slide.** No "as the slide shows", no "this bullet says".
- **Stress sparingly with `<em>`** — two or three words per Say paragraph, the ones that carry
  the point.
- **Move and Do are terse and imperative** — stage directions, not prose. Timings are explicit.
- **Callbacks land where they belong** — the March→builder bridge at the open, the confidence
  re-read at the close, the DRIVES "evaluator → builder" line on the qualify step.
- **Contingencies and backup banks live in Do**, on the slide they'd arise — never on the glass.
- **Honesty about the Day-1 promise** — the run-sheet's realistic line (a *spec*, not a built
  agent) keeps the Say truthful at open and close.

---

## 11. Verify in the browser (required after building)

The presenter deck is observable, so prove it. Use the same sandbox recipe as the audience deck
(`preview-verification-setup` memory note):

1. Start the host static server (`/opt/homebrew/bin/node .claude/static-server.js`, sandbox
   disabled, background) and `preview_start`; navigate to the **presenter** file.
2. Drive a `preview_eval` harness that walks `→` through **all 47 slides** and, on each, presses
   `S` and reads back `#scriptBody` — confirm **every slide has a non-empty script** (no "No
   script for this slide yet."), and that Remember/Move/Say/Bridge are present (Do where the
   archetype requires it).
3. Confirm the panel behaviour: `S` opens/closes the dock, `N` and `Esc` close it, the deck
   slides left by `--scriptw` when open, the chrome tracks, `scriptClose` works.
4. Confirm the **freeze**: the on-glass content, widgets, and Takeaways are visually identical to
   the audience deck (spot-check the widget slides drive on every path — they must, since you
   didn't touch them).
5. Confirm **`@media print`**: every slide stacks on its own page with the script shown inline as
   a white card and the Takeaway/chrome/panels dropped. `preview_screenshot` a couple of slides
   and the print view.
6. **0 console errors.**

---

## 12. The 95% fidelity checklist (the bar)

The presenter deck is not ready until **all** of these are true:

**The freeze (this is what earns the 95%)**
- [ ] The presenter deck has the **same number of slides** as the audience deck, in the **same
      order**, same registers.
- [ ] A **machine diff** of presenter vs audience shows **only**: (a) the 47 added `.script`
      blocks, (b) the §8 plumbing (print rule, aside, helpbar `S`, JS wiring, `--scriptw`/panel
      CSS if it wasn't already dormant), and (c) the header comment. **No slide content,
      widget, `.read`, `.goalrow`, prompt, or Takeaway is changed or deleted.**
- [ ] Every **Takeaway `.note`** is present and byte-identical to the audience deck's.

**The script layer**
- [ ] **One `.script` per slide — count equals the slide count** (47 = 47 for Week 1). None
      skipped, none doubled.
- [ ] Each script sits **immediately after that slide's `.note`**, inside the `<section>`.
- [ ] Every script has **Remember, Move, Say, Bridge**; **Do** on nearly every slide (Week 1:
      45/47) — the full Do on widget/hands-on/demo/finale, a **one-line stage Do** on framing
      slides; omit only the rare bare divider.
- [ ] **Remember** is a declarative thesis to the trainer (third-person "they" or a bare
      principle) — not an instruction addressed to the room.
- [ ] **Say** is first-person spoken register, re-teaches (never reads the slide), British
      spelling, `<em>`-stressed sparingly.
- [ ] **Move** carries a timing/energy note; the durations roughly sum to the day-plan.
- [ ] **Do** names widget controls *in order* / hands-on timing + coverage + backup bank /
      finale enrich→run→capture; contingencies folded in as "If asked X:".
- [ ] Run-sheet verbatim (March bridge, confidence read, vendor demo, coverage rule) is used on
      the slides it maps to.

**Build & canon**
- [ ] The §8 plumbing is present and correct; the CSS shell verified (dormant hooks reused, not
      duplicated).
- [ ] `S` toggles the dock; `N`/`Esc` close it; deck + chrome track `--scriptw`; `scriptClose`
      works; **0 console errors**.
- [ ] Widgets still drive on every path (untouched); nav/steppers/copy/notes/full-screen all work.
- [ ] `@media print` stacks every slide with the script inline as a white card and drops
      chrome/notes/panels.

If every box is ticked, the machine diff confirms ≥95% identity and the scripts read like
Week 1 — you are at the bar.

---

## 13. Worked example — Week 1 audience deck → presenter deck (two slides)

**Slide 1 — the title (`.slide.active`).** The audience slide has the program/week kicker, the
two-line promise, a `.lead`, and a Takeaway ("A working session, not a lecture…"). Frozen. The
presenter script added *after* that Takeaway:
- **Remember:** "Working session, not a lecture — they leave owning a real problem."
- **Move:** "Set the contract in one breath — a working session, not a lecture. ~30 sec, energy up."
- **Say:** "Welcome. This is a working session, not a lecture — your hands are on the tool within
  the first half hour…" (voices the Takeaway, run-sheet register).
- **Do:** "Don't read the agenda yet. Keep the keys handy: *Home* agenda · *N* notes · *F*
  full-screen." (framing slide → light Do.)
- **Bridge →:** "Here's how the day flows." (→ the day-plan slide.)

**A widget slide — M1 the prompt builder (paper + `.pb`).** The audience slide has the six-part
builder widget and its `.read` band. Frozen. The presenter script added after its Takeaway:
- **Remember:** "Add each part and reliability climbs — specificity is control."
- **Move:** "You drive the builder; narrate the reliability meter climbing as you switch each part on."
- **Say:** "Watch the meter. I start with task only — 'summarise this.' It'll do something, but
  it's guessing at everything I didn't say. Now a Role. Context… See the jump on Constraints and
  Examples? …that's specificity buying you *control*."
- **Do:** "Toggle in order: Task → Role → Context → Constraints → Format → Examples. Pause on the
  Constraints and Examples jumps and point at them. Leave them the memory aid: *Task is the
  spine, the rest are ribs* — T-R-C-C-O-E." (widget slide → drive-path Do.)
- **Bridge →:** "Now you drive — but like a scientist, not a tourist." (→ the controlled-experiment slide.)

Notice: nothing on either slide changed. Only a script block appeared after each Takeaway. That
is the entire transformation, 47 times over.

---

## 14. Self-audit — read it as the trainer holding the deck live

Walk the whole presenter deck, slide by slide, and check:

- **Freeze intact** — every slide, widget, `.read`, and Takeaway is exactly the audience deck's.
  If any changed, revert it.
- **Every slide has a usable script** — Remember to glance at, Move with a timing, Say to speak,
  Do to click (where needed), Bridge to launch. No empty panels.
- **Could I run the room from this alone?** If a slide's script leaves you guessing what to say,
  how long, or what to click, it is not finished.
- **Voice** — calm expert, British spelling, spoken register, senior altitude. No L&D chirp.
- **Timings sum to the day** — the Moves add up to the day-plan's 5 hours.
- **Contingencies covered** — backup bank on hands-on, "If asked" on the tricky slides, the
  wifi-failure backup on the demo.
- **Diff is clean** — the machine diff shows only scripts + §8 plumbing.

---

## 15. Reuse — borrow the plumbing, write the scripts fresh

| Reuse verbatim (plumbing) | Write fresh every week (the script content) |
|---|---|
| The §8 CSS shell, aside, JS wiring, helpbar `S`, print rule | Every Remember / Move / Say / Do / Bridge |
| The five-field block shape (§6) | The run-sheet verbatim lines (they are *this* week's) |
| The archetype→shape mapping (§9) | The widget drive-paths (read off *this* week's widgets) |
| The verify + diff routine (§11) | The backup banks, timings, and contingencies |

**The line you don't cross:** copy the *plumbing and the block shape*, then fill the scripts with
**this week's** talk-track, drawn from **this week's** audience deck and run-sheet. If you ever
paste a Week-1 **Say** line onto a later week's slide, you have copied the body — start it over.
And **never** copy a change to a slide — the surface is always the current week's frozen audience
deck.

---

## 16. How this playbook gets better every week (the reflection loop)

This playbook is a **living benchmark**; the Week 1 presenter deck (measured against its audience
twin) is the **floor, not the ceiling.**

**After each presenter deck ships, run the loop:**
1. **Reflect** — where did the trainer want a different word, a missing timing, a contingency the
   script didn't hold? What made the machine diff dirtier than "scripts + plumbing"?
2. **Convert each correction into a one-line rule** so the same miss can't recur.
3. **Promote anything better-than-benchmark** into the standard and update the section.
4. **Log it** — add a dated line below.
5. **Re-benchmark** — the newest presenter/audience pair becomes the "match or beat" reference.

**Standing rules for the loop:**
- **Every correction becomes a rule.** Feedback that lives only in chat is feedback lost.
- **The bar only goes up.** A new presenter deck may not regress below the last.
- **Keep it lean.** When you add a rule, check whether it *replaces* a vaguer one.

**Lessons log (newest first):**
- **2026-07-02 · validation pass against the Week-1 benchmark.** A blind build from this playbook
  reproduced the surface at 100% (machine diff = scripts + plumbing only) but under-covered **Do**:
  the build put Do on 26/47 slides, the shipped deck carries it on **45/47**. Correction (now
  general rules above): Do is *near-universal* — even framing slides (title, act-openers, dark
  dividers, cold-opens, close) get a **one-line stage Do** (a watching question, a tone/timing
  directive, a "collect the artefact" note, or an "If asked X:"); omit only the rare bare divider.
  Second correction: **Remember** is a declarative thesis to the trainer (third-person "they" or a
  bare principle), never an instruction addressed to the room.
- **Week 1 (the founding benchmark):** the transformation is *audience deck → presenter deck*,
  additive only. 47 slides, 47 Takeaways, unchanged; 47 scripts added, one per slide, each
  Remember → Move → Say → Do → Bridge, placed right after the Takeaway. The CSS shell was already
  dormant in the audience deck; the active plumbing is the aside + JS wiring + helpbar `S` + the
  print `.script` rule. The scripts' voice and verbatim lines come from the facilitator
  run-sheet; timings sum to the 5-hour day. ≥95% identity is guaranteed by freezing the surface
  and proven by a machine diff that shows only scripts + plumbing.

---

*This playbook is the contract for presenter decks — and a living one. Each week makes it
sharper; the goal is that the next first draft is always a little closer to the Week-1 bar than
the last.*
