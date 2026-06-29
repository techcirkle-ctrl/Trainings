# PRE-READ PLAYBOOK
### The primary source of truth for building every week's pre-read

> **The job in one sentence:** hand me a week's **requirement slide**, and by following this
> playbook I produce a finished, interactive, leader-friendly **pre-read HTML** that is at least
> **90% ship-ready on the first pass** — looking and teaching like the Week 2 pre-read, or better.

This is the **primary playbook for pre-reads.** It supersedes `LESSON-FORMAT.md` for anything
about pre-reads. Where they disagree, **this wins** (older docs get reconciled later). The two
finished references it is calibrated against are:

- **Gold standard:** `weeks/week-2-agentic-deep-dive/00-preread/week-2-prework.html`
- **Lean baseline:** `weeks/week-1-foundations/00-preread/week-1-preread-v2.html`

When in doubt, **open Week 2 and copy how it does the thing.**

---

## 0. How to use this playbook

You will be given **one requirement slide** (a PowerPoint slide from
`ai-capability-program/source/AI_Capability_Program_v3.pptx` — Week 3 = slide 8, Week 4 =
slide 9). Then, in order:

1. Read **§1 Persona** and **§2 Doctrine** — this is *who you are* and *what you believe* while building.
2. Use **§4 Translation** to turn the slide into a section list, and **agree it with the trainer before building.**
3. Build each section to the **§5 blueprint**, using the **§7 widget catalogue** and **§9 canon**.
4. **Verify in the browser** (§14) and clear the **§15 checklist**.
5. Show the trainer each piece as you go; iterate.

Everything you need is in this one file. You should not need to reverse-engineer Week 2 to
match it — but it's there as the worked reference, and §16 maps it slide-to-section so you can
see the method applied end to end.

---

## 1. The persona — who you are when you build this

You are a **superb teacher** — the kind people remember. Not a documentation writer, not a
slide-filler. Hold this voice the entire time:

- **You make them *do*, not watch.** Every idea is something the leader *drives* with their own
  hands before you explain a word of it. If a section is mostly you talking, you've failed.
- **You respect their time and intelligence.** They are senior, busy, and not technical. No
  jargon, no filler, no flattery. Plain-English analogies (a context window is a *desk*; a tool
  call is the model *asking* you to run something). One idea per section.
- **You keep it alive.** Short cycles — a little reading, then a hands-on beat, then a one-line
  takeaway, repeated. A wall of prose is the enemy. So is a widget bolted onto the end of an
  essay.
- **You hand them a decision every time.** They don't leave a section with trivia; they leave
  with *a call they now know how to make* (the "Leader's read").
- **You make it feel like a good app, not a worksheet.** Brilliant.org, not a PDF. Playful where
  it can be, never boring. The page should make them *want* to click the next thing.
- **You close loops.** Callbacks to last week and to earlier sections, placed right where they
  land. The leader who found last week "Latin" should feel recognised and carried.

If a section would bore *you* to read, it will bore them. Rebuild it.

---

## 2. Doctrine — the beliefs that don't bend

1. **Teach a little, do a lot.** Interaction is the product; reading is a cost. Aim for roughly
   half of each section's time spent *doing*, not reading.
2. **Out-judge the machine.** The leader's scarce skill is *judgement*, not operation. Every
   section ends by tying the mechanism to a decision they own (cost, risk, where a human stays
   in the loop).
3. **The cheapest layer that works wins.** Over-building is the most common, most expensive
   mistake. Teach restraint as the core skill.
4. **One escalating problem, one spine example.** The cohort carries **one problem across all
   four weeks** — never reseed a new use case. Inside a single pre-read, thread **one concrete
   recurring example** through the sections (Week 2 = the *complaint-queue agent*) so
   recognition carries the room.
5. **Use before explain.** Let them drive the widget before you open the internals.
6. **No false simplifications.** Never teach a tidy hierarchy that breaks under an expert's eye
   (the AI stack is *composable capabilities on one engine*, not a containment ladder). Clarity
   must never cost correctness.
7. **Leader altitude.** Plain analogies, tied to their function (Finance/HR/Sales/IT), never
   "to understand X."
8. **Test understanding everywhere.** Every section closes with an instant-feedback check that
   teaches on **right *and* wrong**.
9. **Tool reality: Claude chat + Projects (no-code).** Leaders build in Claude Projects.
   Claude Code is the *trainer's* instrument, shown live, watch-only. Don't promise a
   code-wired / tool-looping agent the no-code surface can't deliver.
10. **British spelling, executive register; self-contained; local-only; prints clean.** Always.

---

## 3. The input — anatomy of a requirement slide

Every week's slide has the **same five blocks.** This is your raw material:

| Block | What it gives you | How you use it |
|---|---|---|
| **Objective** | The one capability the week builds | The pre-read's north star; shapes the finale. |
| **Pre-work list** | External courses/readings + times | Becomes **"Go deeper"** links + the **1–2 required reads** (the rest is optional). Register each in `RESOURCES.md`. |
| **Session — 5 hours** | Hr 1–5, each a concept or activity | **This is the spine.** Each *teaching* hour → one pre-read section. |
| **Homework** | The artifact the week produces | Informs the pre-read's **closing "what you'll build/bring"** beat — but the pre-read itself stays generic (no leader's own data). |
| **Output** | The deliverable | Reinforces the closing framing and the finale. |

> The pre-read **pre-builds the intuition** for what the session then *applies*. Anything needing
> the leader's own data lives in the session/homework — the pre-read is generic and driveable.

---

## 4. The translation — slide → section list (do this first, agree it before building)

**Step 1 — Read the 5 session hours.** Hr 1 is usually "pre-work + last week's homework debrief"
(an in-room activity, not a concept). **Hours 2–5 are the concept hours** — each becomes a
pre-read section that pre-teaches its intuition.

**Step 2 — Add a "Start here" Section 1** that *closes the previous week's loop*: remind them of
the homework/artifact they should have finished, and have them do one tiny hands-on thing that
the week stands on (Week 2: open a Project, connect one no-code tool). This reactivates fluency
and earns the rest of the page. (Skippable; it's a pre-read, not an exam.)

**Step 3 — Write the canonical section list** — the ordered set of one-line, leader-language
concepts. **This is the contract. Agree it with the trainer before writing any HTML.**

**Step 4 — Sequence and time it.** Order so each section builds on the last; ~10–15 min per
section; total ≈ 1–1.25 hr on the page (plus required reads stated separately).

**The mapping rule of thumb:**

```
Section 1            = "Start here" (close last week's loop + one tiny hands-on)
Sections 2..N        = the session's concept hours (Hr 2..Hr 5), one each
Final framing        = points at this week's homework/output (generic, build-first)
```

A week with 4 concept hours → **6 sections** (Start-here + 4 + the build-shell close lives inside
the last section). A leaner week can be **4–5 sections** like Week 1 v2. Match the *content*, not
a fixed count.

---

## 5. The section blueprint (every section, in this order)

1. **Tag strip** — `Section n of N` + rough time (`~15 min`).
2. **Title** (`<h2>`) + **"Why this matters to you"** (`.why` accent-soft box) — in *their*
   function's language, never "to understand X."
3. **Callback** (`.callback` amber) where useful — "↩ From Week 1: …", placed *adjacent* to what
   it refers to.
4. **The teaching = a driveable widget** (`.lab`) — read → interact → recap, in short cycles.
   The interaction **is** the teaching, not decoration. (See §7.)
5. **"Keep this"** — a small recap `table.lens` or rule-of-thumb, placed *after* the interaction
   (recap, never the explanation).
6. **"Leader's read"** (`.why` box) — one line tying the mechanism to a decision they own.
7. **Instant-feedback quiz** (`.card.quiz`) — 4 questions (5 on the meatier sections); teaches on
   right *and* wrong. (See §11.)
8. **"Go deeper"** (`.deeper`) — optional, one or two `RESOURCES.md`-cited links.
9. **Section footer** (`.secfoot`) — "Mark this section complete" + "Next: … →".

Keep the rhythm: **why → do → keep → decide → check → next.**

---

## 6. File-level furniture (the shell around the sections)

- **Masthead** — program · week/theme · "Prework" · pace line:
  `Work at your own pace · ~1.25 hr on this page + required reads (~X hr) · N short, interactive sections. Your progress is saved on this device only — nothing is sent anywhere.`
- **Sticky navbar** — progress bar (`X / N complete`) + the **pill row** (each pill shows ✓ when done).
- **Required-reads callout** (if the week has required reads) — amber, near the top / inside
  Start-here. **Clickable links.** 1–2 required; everything else optional "go deeper."
- **Finale** — hidden until all sections complete; a short, build-forward completion note.
- **"Ask your trainer"** — once, near the end: mid-week clinic + Teams doubt channel (answered
  within 1 business day).
- **Footer** — points to `reference/glossary.html`; notes RESOURCES + local-only storage.

**State:** one `localStorage` key per week (`acp-wN-preread`), `{done:[...]}`. Nothing is sent.
Each widget is its own IIFE with defensive guards (`if(!el) return;`).

---

## 7. The widget catalogue — the heart of the pre-read

**The rule above all rules: visualise the mechanism; don't tabulate it.** Anything about *how
something works* earns a **driveable visual**. If you're explaining a mechanism with a table, a
bullet list, or a passive reveal, you've lost the room — convert it.

### Reuse these (proven across W1 + W2)

| Pattern | What it is | Use for |
|---|---|---|
| **Driveable machine (before/after toggle)** | One control flips the system between two modes and re-runs; contrast is instant. | "What does X actually change?" — RAG on/off; Chatbot vs Agent. The single highest-impact pattern. |
| **Node-and-link graph, step-through** | SVG nodes + edges; Step / Run all lights the active node, its edges, and any tool it calls; a loop counter. | Anything with a flow or cycle — the agent loop (Goal→Think→Act→Observe→Decide→Done). |
| **Step-through stepper** | A linear sequence of states with Step/Reset; each state shows who-acts + a code/console line + a plain narration. | A single mechanism in stages — a tool call (model *requests* → your system *runs* → observation returns). |
| **Build-up composer** | Toggle parts on; the result + a meter recompute; refuse-to-proceed logic encodes a rule. | "It's made of independent pieces" — compose a spec (Instructions/Knowledge/Tools/Stopping/Human-checkpoint), with required vs recommended grouping. |
| **State/“desk” widget** | Add items; watch capacity overflow and drop the oldest; pin to persist; start-new to show what survives; remove to curate. | Memory & context windows — short-term desk vs long-term knowledge, and that *you* curate it. |
| **Filterable labelled accordion** | Rows each carry their **one answer as a label** (visible at a glance, ordered to show a spectrum); click a row to open its "why"; group **filter toggles** at top. | A one-to-one decision set where the *spectrum* matters — task → its one pattern (workflow vs agent). |
| **Sorter** | Classify items, instant per-item verdict. | Judgement calls — data-sensitivity. |

### Avoid these (they read as passive or as a quiz in disguise)

- **Passive click-to-expand reveals** that just hide prose behind a toggle. *(Note: the Week-2
  filterable accordion is allowed precisely because it is **not** passive — every row shows its
  answer as a label, the order teaches the spectrum, and the filters make it a tool. The line is:
  **no passive reveals; interactive/filterable/at-a-glance is fine.**)*
- **Linear text step-through where a visual would carry it** — if the steps describe a flow,
  draw the flow and light it.
- **A text prompt + four answer buttons dressed up as "recall"** — that's a quiz wearing the
  section's clothes. Reuse the section's visual instead.
- **A wall of tables/bullets as the primary teaching** — tables are *recap* ("Keep this"),
  placed *after* the interaction, never the explanation.

### Make the control embody the idea
Apply the two-register rule to the widget's **own** controls: the status-quo / "what is" state is
inert and muted; the "lifted / what could be" state is teal. The control itself teaches (RAG
**off** grey vs **on** teal; Chatbot vs Agent). Use the named components (pills, segmented
switch) — never plain bordered rectangles.

### Build it, then drive it
After authoring a widget, run it and exercise **every path**. Derive widget state from the DOM
(read the active class), not a parallel JS variable, so the control and its logic can't desync.

---

## 8. The spine example

Pick **one concrete example** from the cohort's world and thread it through every section that
needs an example (Week 2 = the **complaint-queue agent** they watched in Week 1). Recognition
does the heavy lifting: the same example, seen from a new angle each section, beats a fresh
example per section. Keep it familiar but don't copy the prior week's exact framing verbatim.

---

## 9. The design canon (copy verbatim — do not reinvent)

Inline these tokens in every file:

```css
:root{
  --ink:#16202b; --muted:#5c6b7a; --line:#e4e8ec;
  --paper:#ffffff; --wash:#f6f8fa; --accent:#0b6e6e; --accent-soft:#e2f0ef;
  --warn:#b06a00; --good:#1c7a4a; --bad:#b23b3b;
  --maxw:820px;
}
```

- **Type:** body/reading = **serif** (`ui-serif, Georgia, "Iowan Old Style", Palatino, serif`);
  UI/labels/widgets = **sans** (`ui-sans-serif, system-ui, sans-serif`); code = mono. Kicker =
  600, `letter-spacing:.14em`, uppercase, teal, ~12px — every section opens with one.
- **Layout:** reading column, `--maxw:820px`, dense serif text, tab nav.
- **Two registers (the Sparkline rule):** *What Is* = muted/`--wash`, flat, no teal (status quo
  feels inert). *What Could Be* = teal `--accent`, `--paper`, more light (the future warms the
  room). Code both poles this way **everywhere**.
- **Named components:** `.card` `.pills/.pill` `.why` `.lab` `.kicker` `.tag` `.callback`
  `.deeper` `.secfoot` `.quiz` `table.lens`. Reuse; don't invent parallels.
- **Hard rules:** self-contained (inline CSS + vanilla JS, no CDN/network/build); `@media print`
  reveals all panels and expands interactive content; local-only state.
- **No dark surfaces** — keep everything light.

---

## 10. Voice & copy

- **British spelling, executive register** (behaviour, summarise, organised, prioritise).
- **"Why this matters to you"** speaks the leader's function, the stakes, and the decision —
  never "to understand the concept."
- **"Leader's read"** is one sentence: mechanism → a call they own. This is what turns trivia
  into *their* knowledge.
- **Callbacks** ("↩ From Week 1: …") sit adjacent to what they reference.
- **Build-first register** (a Week-2 lesson worth keeping): make them *itch to build*. Governance
  is something a builder *designs in*, not a posture above the keyboard. Lead with building;
  subordinate governance to it.

---

## 11. The instant-feedback check

- **4 questions per section** by default; **5** on the meatier sections.
- **Teaches on right *and* wrong:** every option, when chosen, reveals an explanation — the
  correct answer is affirmed; a wrong answer is corrected *and* the right one highlighted.
- Reinforce the section's own content and the **new** things the page introduced (a new widget
  behaviour, a build step). Feedback is immediate and automatic — never "answers at the bottom."
- Local only.

---

## 12. Resources & citations

- Every external link is registered in `ai-capability-program/RESOURCES.md` with an ID (R1, R5…)
  and cited by ID. **No bare or invented URLs in the body.**
- From the slide's pre-work list: pick **1–2 required reads** (state them up front, clickable);
  everything else becomes **optional "Go deeper."**
- If a named in-house reading **doesn't exist yet**, substitute a **reputable, free, public
  source** (e.g. IBM Think, Anthropic, Google) that teaches the same thing — and flag the gap.
  Never cite a dead link.
- Verify approximate links before launch.

---

## 13. The build routine (slide → shipped)

1. **Read** the week's slide (the 5 blocks), the prior week's homework (what they walk in with),
   and **open Week 2** as the live reference.
2. **Translate** (§4): write the section list; **agree it with the trainer** before any HTML.
3. **Scaffold** one self-contained HTML: tokens (§9), masthead + sticky pills + progress, N empty
   `<section class="panel">` shells, the finale, footer, the JS shell (pill nav, progress,
   localStorage, `makeQuiz`).
4. **Build each section to the §5 blueprint**, newest concept widget per §7. Thread the spine
   example (§8). Show the trainer each piece as you go.
5. **Quizzes** (§11), **required reads + Go-deeper** (§12), register new links in `RESOURCES.md`.
6. **Glossary** — add any genuinely new term to `reference/glossary.html`.
7. **Verify in the browser** (§14): 0 console errors, every widget drives on every path, print
   reveals everything.
8. **Self-audit** as teacher *and* student (§17); clear the **§15 checklist**; fix cross-reference
   / finale / section-number drift.
9. **Don't commit** unless the trainer says so.

---

## 14. Verify in the browser (required after meaningful changes)

The pre-read is observable in a browser, so prove it works — don't ask the trainer to check
manually.

**The sandbox recipe** (the preview-managed server can't bind a port under the sandbox):

1. Start the host static server via Bash with `dangerouslyDisableSandbox: true` and
   `run_in_background: true`: `/opt/homebrew/bin/node .claude/static-server.js` (serves repo root;
   honours `PORT`, default 8765). If a stale server already holds the port, point
   `.claude/launch.json` at a free port (e.g. 8766).
2. `preview_start`, then navigate via `preview_eval` →
   `window.location.href='http://localhost:<port>/ai-capability-program/weeks/week-N-…/00-preread/week-N-prework.html'`.
3. Drive **every** widget with a `preview_eval` harness that `.click()`s the controls and returns
   a state report (faster than many click round-trips).
4. Confirm **0 console errors**, every widget reaches its end state, the quiz feedback fires, and
   `@media print` reveals panels. `preview_screenshot` always captures from the top — hide
   preceding elements briefly if you need a lower shot, then reload.

(See the memory note `preview-verification-setup` for the full recipe and gotchas.)

---

## 15. The 90% quality checklist (the bar)

A pre-read is not ready until **all** of these are true:

**Teaching**
- [ ] Sections mirror the session's concept hours; every session concept is pre-taught.
- [ ] Each section is `why → drive a widget → keep-this → leader's read → quiz → next`.
- [ ] ~½ of each section is interaction, not reading. No wall of prose with a widget bolted on.
- [ ] Every section's interaction **teaches a mechanism** (driveable), not a quiz in disguise.
- [ ] Every mechanism ends with a one-line **Leader's read** tied to a decision.
- [ ] One **spine example** threaded through. Callbacks sit adjacent to their setup.
- [ ] Each section's quiz: 4 (or 5) questions, teaches on right *and* wrong.

**Correctness & register**
- [ ] No false simplification that breaks under an expert's eye.
- [ ] British spelling; executive register; build-first framing (govern = something a builder designs in).
- [ ] Tool reality respected (Claude Projects = leaders; Claude Code = trainer, watch-only).
- [ ] Every external claim cited to `RESOURCES.md`; required reads clickable; no dead/invented links.

**Build & canon**
- [ ] Self-contained (inline CSS + vanilla JS, no network); opens with `open`.
- [ ] Design tokens + named components used; light throughout; two-register colours applied.
- [ ] Progress persists locally (`acp-wN-preread`); nothing sent.
- [ ] **0 console errors**; every widget drives on every path; `@media print` reveals all panels.
- [ ] Section numbers, cross-references, finale, and pill titles all consistent.

If every box is ticked, you're at the 90% bar — what remains is taste-level iteration with the
trainer.

---

## 16. Worked example — the Week 2 slide, mapped to the shipped pre-read

This is the method applied end to end. **Slide 7** gave:

- *Objective:* understand agent lifecycle, architectures, tools, memory; **build first agent.**
- *Session:* Hr 1 debrief · Hr 2 lifecycle + architectures · Hr 3 tools + MCP · Hr 4 memory &
  state · Hr 5 build your first agent.

Translated to the shipped 6-section pre-read:

| Pre-read section | Came from | Widget |
|---|---|---|
| 1 · **Start here** | Closes Week 1's homework loop | Action card: finish your stack-map, open a Project, connect one no-code tool |
| 2 · **The agent loop** | Hr 2 (what an agent *is*) | Chatbot↔Agent toggle + SVG loop graph step-through (complaint queue) |
| 3 · **Workflow vs agent** | Hr 2 (architectures) | Filterable labelled accordion — task → its one pattern, workflow/agent filters |
| 4 · **Tools** | Hr 3 (tools + MCP) | Tool-call stepper (model requests → your system runs → observation) + static MCP panel |
| 5 · **Memory & state** | Hr 4 | The "desk" context-window widget (overflow / pin / forget / new chat) |
| 6 · **Design your agent** | Hr 5 (build) | Lifecycle stepper + spec composer (required vs recommended) + build-the-shell close |

Required reads (from the pre-work list): Anthropic *Building Effective Agents* (R5) +
*Agent Architectures* (R13 → three IBM explainers, since the in-house doc was a stub). Everything
else → optional "Go deeper." Spine example = the complaint-queue agent throughout.

---

## 17. What Week 2 refined over Week 1 (now standard)

These are paid-for lessons — bake them in from the start:

- **A "Start here" Section 1** that closes the prior week's loop and gets one tiny no-code build
  done before the page even teaches.
- **Build-first register** — make them itch to build; subordinate governance to building.
- **One spine example** threaded through (vs switching examples per section).
- **Filterable labelled accordion** for one-to-one decision sets (the spectrum visible at a
  glance; not a passive reveal).
- **Curate-able state** in the memory widget (you can *forget*, not only add).
- **Required reads made clickable**, with a reputable public substitute when an in-house reading
  doesn't exist.
- **4–5 quiz questions** per section (up from 3).
- **Grouped composer** (required vs strongly-recommended) so the layout itself teaches.

---

## 18. Self-audit — read it as teacher *and* as student

Walk the whole pre-read, paired sections in order, and check:

- **Sequence** — each section builds on the last; no concept used before it's introduced;
  the next/previous handoff flows.
- **Cognitive load** — no section carries more than its time tag implies; every hard idea has an
  interaction, not just prose.
- **Accuracy** — every claim defensible; no tidy simplification that breaks under scrutiny.
- **Consistency** — cross-references, section numbers, finale, pill titles, and the glossary all
  match the *current* content.
- **Register** — clean British spelling; leader altitude; build-first.
- **Would it bore you?** If yes, it will bore them. Rebuild it.

---

## 19. Starter kit & reuse — borrow the bones, never the body

The fastest route to a Week-2-quality first draft is to **reuse the plumbing and regenerate the
teaching.** Borrow the skeleton; write a brand-new body every week. Two weeks should never *read*
the same — they should only be built the same way.

**Reuse vs regenerate:**

| Reuse the skeleton (format / boilerplate) | Regenerate fresh every week (content) |
|---|---|
| The HTML scaffold — masthead, sticky pills, progress bar, finale, footer | The week's concepts, section titles, and all prose |
| The design tokens + named components (`.why .lab .callback .deeper .secfoot .quiz table.lens`) | Every "Why this matters", "Keep this", "Leader's read" |
| The JS shell — pill nav, progress + `localStorage`, the `makeQuiz` helper | Every quiz question, option, and explanation |
| The widget **mechanisms** (graph, stepper, state-desk, composer, filterable accordion) | Each widget's data, labels, narration — and the spine example |
| The section anatomy (§5) and file furniture (§6) | The cohort-tailored examples (Finance/HR; their real capstones) |

**The line you don't cross:** copy a widget's *mechanism*, then **empty its data and rebuild it
from this week's concept.** If you ever paste a sentence of Week-2 teaching text, you've copied the
body, not the bones — start that piece over.

**Pick a widget by the shape of the concept** (don't default to one):

| The concept is… | Reach for… |
|---|---|
| a flow or a cycle | node-graph step-through |
| one mechanism unfolding in stages | a stepper |
| "what does X actually change?" | a before/after toggle machine |
| made of parts / a readiness check | a build-up composer |
| accumulation, eviction, persistence | a state-"desk" |
| a one-to-one choice across a spectrum | a filterable, labelled accordion |
| a judgement call | a sorter |

If nothing fits, **invent one** — but it must be *driveable*, never a passive reveal.

**Two warnings paid for in blood:**
- **Homework anchor.** Before writing "Start here", open the **prior week's actual homework file**
  and match its end-state word-for-word. Never assume what they were asked to do. (We shipped the
  wrong anchor once; don't repeat it.)
- **Individuality.** The structure repeats; the soul doesn't. Each week earns its own examples,
  its own spine, its own voice — inside the same bones.

---

## 20. How this playbook gets better every week (the reflection loop)

A good teacher reviews the lesson after every class. This playbook is a **living benchmark**, and
the latest shipped week is the **floor, not the ceiling.**

**After each week ships, run the loop:**
1. **Reflect** — what did the trainer/PM correct, and why? What bored anyone? What needed iteration?
2. **Convert each correction into a one-line rule** — so the same miss can never happen twice.
3. **Promote anything better-than-the-benchmark** into the standard (a sharper structure, a new
   widget) and update the relevant section.
4. **Log it** — add a dated line to the Lessons log below, so the growth is visible.
5. **Re-benchmark** — the newest shipped week becomes the new "match or beat" reference.

**Standing rules for the loop:**
- **Every correction becomes a rule.** Feedback that lives only in a chat is feedback lost.
- **The bar only goes up.** A new week may not regress below the last.
- **Keep it lean.** When you add a rule, check whether it *replaces* a vaguer one. The playbook
  should get sharper, not just longer.

**Lessons log (newest first):**
- **Week 2 → 3 carry-forward:** build-first register; one threaded spine example; filterable
  *labelled* accordion (not passive reveals); curate-able memory (you can *forget*, not only add);
  required reads made clickable with a reputable public substitute when an in-house reading is
  missing; 4–5 quiz questions per section; grouped composer (required vs recommended); and
  **verify the homework anchor against the real file.**

---

*This playbook is the contract for pre-reads — and a living one. Each week makes it sharper; the
goal is that the next first draft is always a little closer to flawless than the last.*
