# AUDIENCE-DECK PLAYBOOK
### The primary source of truth for turning a week's (requirement slide + finished pre-read) into the live session's audience deck

> **The job in one sentence:** hand me a week's **requirement slide** and its **finished
> pre-read**, and by following this playbook I produce the **projectable, hands-on audience
> deck** the trainer runs in the room — at least **90% ship-ready on the first pass**, looking
> and teaching like the Week 2 deck, or better.

This playbook is **only about one transformation**:

```
   (requirement slide)  +  (finished pre-read HTML)   ─────►   audience deck HTML
        the contract          the intuition, pre-built           the live session
```

It is **not** a general deck-authoring guide, and it does **not** re-derive the pre-read (that
is `PRE-READ-PLAYBOOK.md`'s job). It takes inspiration from that playbook's *shape*, but its
whole focus is the **correct conversion** of the two inputs into the deck.

**Calibration target (the benchmark):** the shipped **Week 2** deck (our gold standard) —
`weeks/week-2-agentic-deep-dive/01-workshop/deck-week2-agentic-audience.html`. Match it first.
**Week 1** (`deck-week1-foundations-audience.html`) is a **secondary reference** — draw a few
cues from it, but Week 2 is the bar. The bar: re-run this playbook on Week 2's two inputs and
reproduce **~90–95%** of that deck.

> **Note:** the worked example in §17 still walks through **Week 1** (Slide 6 + `week-1-preread-v2.html`)
> as the illustrative method. Treat it as a valid *method* walkthrough, but calibrate the final
> look/feel/richness against the **Week 2** deck above.

**Ignore the stale format docs.** `DECK-FORMAT.md`, `KEYNOTE-FORMAT.md`, `LESSON-FORMAT.md`,
`PLAYBOOK.md` and the other `*-FORMAT.md` files in this folder describe superseded models
(e.g. "N decks + a helper.md"). The shipped decks did **not** follow them. Do not cite, follow,
or reconcile against them. When in doubt, **open the Week 2 deck and copy how it does the
thing.** Ignore the stale pointers inside the deck's own HTML comments too (it references
`DECK-FORMAT.md` and `reference/DESIGN.md`) — derive the canon straight from the file.

---

## 0. How to use this playbook

You are given **two inputs**: the week's **requirement slide** (from
`ai-capability-program/source/AI_Capability_Program_v3.pptx` — Week 1 = slide 6, Week 2 = slide
7, Week 3 = slide 8, Week 4 = slide 9) and the week's **finished pre-read HTML**. Then, in order:

1. Read **§1 Persona** and **§2 Doctrine** — *who you are* and *what you believe* while building.
2. Use **§5 the conversion map** to turn the two inputs into an **act/movement plan**, and
   **agree it with the trainer before building.**
3. Build each movement to the **§6 blueprint**, port widgets per **§8**, and build the finale
   to **§7**. Use the **§9 canon** and **§10 furniture** verbatim.
4. Write the **§11 Takeaway notes**, **verify in the browser** (§15), clear the **§16 checklist**.
5. Show the trainer each act as you go; iterate.

Everything is in this one file. §17 maps Week 1 slide-to-deck so you can see the method applied
end to end.

---

## 1. The persona — who you are when you build this

You are a **master workshop designer** building the room's shared surface for a **six-hour,
hands-on session** — not a slide-filler, not a documentation writer. Hold this voice:

- **You build a working session, not a lecture.** The deck exists so leaders *do the work on
  their own problem*, live. If a stretch is the trainer talking at glass, you've failed.
- **The trainer talks; the glass supports.** Every slide is a **cue + a visual**, never a
  script. The test for any sentence on a slide: *could the trainer say this rather than show
  it?* If yes and it's long, cut it to a cue and move the words to the Takeaway note.
- **You teach a little and make them do a lot.** Hands-on blocks are *deliberately longer* than
  teach blocks. That ratio is the point for this room.
- **You re-teach from zero.** Never assume the pre-read was done. The pre-read pre-built the
  intuition; the deck earns it again, cold, then *applies* it. Never write "as you saw in the
  prework."
- **You turn concepts onto their own work.** The pre-read was generic and solo. The deck's
  finale makes each leader take **one real problem they own** from a hunch to a spec — the spine
  they carry for four weeks.
- **You hand them the judgement every time.** Every movement ends with *a call they now own*
  ("You'll decide…") — cost, risk, the layer choice, where a human stays in the loop.
- **You make it feel like a keynote, not a deck template.** Big type, clean registers, one idea
  per slide, momentum. The room should lean in.

If a slide would bore *you* from the back of the room, it will bore them. Rebuild it.

---

## 2. Doctrine — the beliefs that don't bend (deck edition)

1. **Teach a little, do a lot.** The hands-on minutes exceed the teach minutes; the timed
   day-plan proves it on the second slide.
2. **The trainer is the teacher; the panel is the aid.** Words on glass pass "say it, don't show
   it." The talk-track lives in the **Takeaway notes**, never on the slide.
3. **Re-teach from zero.** The deck stands alone. No "as in the prework." The pre-read is a
   *pre-loader*, not a prerequisite the deck leans on.
4. **Out-judge the machine.** The leader's scarce skill is *judgement*, not operation. State the
   posture early ("How today works") and return to it — the machine over-builds and sounds
   authoritative; pushing it down a layer is the call they're paid to make.
5. **The cheapest layer that works wins.** Teach restraint as the core skill; make it the rule
   that governs the finale ("the lowest capability that solves this, and why not the one above?").
6. **One escalating problem, carried — and it's *theirs*.** The whole day converges on the
   leader's **own** real problem, surfaced live in the finale, and carried across all four weeks.
   Inside the teaching, thread **one concrete recurring example** (Week 1 = the complaint /
   vendor / RFP world) so recognition carries the room.
7. **Every movement is Goal → do → judgment.** Nothing passive. A dark divider states the Goal +
   "You'll decide"; the panel makes them do it; the `.read` band names the call they own.
8. **Port the pre-read's hero widgets verbatim, sized up.** Same mechanism, same data, bigger.
   Never reinvent an interaction the pre-read already proved.
9. **No quizzes in the deck.** A live room doesn't self-mark. The pre-read's instant-feedback
   checks convert into **"You'll decide"** + the **hands-on judgment**. (The only self-checking
   interaction that survives is a *teaching* widget like the data sorter — it teaches, it isn't
   an exam.)
10. **Tool reality: Claude Desktop + Projects (no-code), workspace account.** Leaders build in
    Claude Desktop on the **program workspace account** (not personal). Claude Code / the
    terminal is the *trainer's* instrument, watch-only. The finale runs inside a **Claude
    Project** built up in layers.
11. **British spelling, executive register, build-first; self-contained; local-only; prints
    clean.** Always.

---

## 3. Input A — anatomy of the requirement slide

Same five blocks as the pre-read used. Here is what each one drives **in the deck**:

| Block | What it gives you | How the deck uses it |
|---|---|---|
| **Objective** | The one capability the week builds | The day's spine and the finale's north star. |
| **Pre-work list** | External courses/readings | **Not re-listed** — the deck re-teaches cold. Surfaces only as an optional line in a Takeaway or the "Stuck or curious?" support slide. |
| **Session — 5 hours** | Hr 1–5 | **The act/movement spine.** Hr 1 (debrief) → cold open + "how today works". Concept hours → teaching movements grouped into acts. The build hour → the finale. |
| **Homework** | The artifact the week produces | **The finale produces the homework, started live.** (Week 1: "Map the Stack" homework = the stack map + agent spec the leader writes in the Capstone Decider.) |
| **Output** | The deliverable | Reinforces the finale's exported artifact and the "prove the shift" close. |

> The slide sets the **contract** (what must be delivered) and the **time budget** (a 5-hr
> session → a ~6-hr projected day with breaks). The deck honours both.

---

## 4. Input B — anatomy of the finished pre-read

The pre-read is your **richest** source: it already contains the concepts, the analogies, the
spine example, and — crucially — the **driveable widgets**, already built and calibrated. Mine it:

| Pre-read element | Becomes, in the deck |
|---|---|
| Each **section** (a concept) | One **teaching movement** (re-sequenced into an act, re-taught cold). |
| The section's **"Why this matters to you"** | The movement divider's **Goal** + **"You'll decide"**. |
| The section's **driveable widget** (`.lab`) | **Ported verbatim, sized up** into the movement's teaching panel (§8). |
| The section's **"Keep this" / rule-of-thumb** | The on-slide `.read` band and/or the Takeaway note. |
| The section's **"Leader's read"** | The `.read` band (mechanism → a call they own) and the Takeaway. |
| The section's **quiz** | **Dropped** → converted to "You'll decide" + hands-on judgment (§2.9). |
| The **spine example** | Carried through the teaching movements (same world, fresh framing). |
| The pre-read's **generic drive-it-yourself** framing | Upgraded to **their own real problem** in the finale. |

> The pre-read pre-built intuition **generically and solo**. The deck's job is to **re-teach that
> intuition cold in a room, then bend it onto each leader's own problem** and turn it into an
> owned artifact. That bend — from generic to personal, from watch to build — is the conversion.

---

## 5. The conversion map — slide + pre-read → deck (do this first; agree it before building)

This is the contract. Produce it before writing any HTML.

**Step 0 — the slide-coverage audit (the 100% guarantee).** The deck is the **complete** artifact;
the pre-read is a lean primer. Before anything else, audit the **whole slide** — not just the
concept hours — and map **every** element to the movement/slide that will carry it:

- **Every session hour, Hr 1–5** — including the debrief/peer-review hour and the build/demo hours.
- **Every pre-work TASK the session consumes.** These are not just readings — some are *deliverables
  the session depends on* (Week 3: "identify 3 real use cases, one-para brief each" → **Hr 4 picks
  1 of those 3**). The deck must **prompt leaders to bring these** and the sprint must **build from
  them**. A pre-work task the session uses is a slide requirement, not optional.
- **The build-sprint mechanics, exactly as the slide states them** — pick-1-of-N use cases, 1:1
  coaching, peer review in pairs, a *second* agent, timed demos (e.g. 3 min each). Mirror them.
- **The homework and the output** — the finale points at them.

Any slide element with **no home is a gap you must design in.** A gap in the lean pre-read is
**never** an excuse for a gap in the deck — where the pre-read is silent, build the movement fresh
from the slide. Produce this audit as a short table (slide element → movement) and agree it with
the trainer alongside the act/movement plan.

**Step 1 — read the slide's 5 session hours and the pre-read's sections side by side.** They
*mostly* correspond, but **do not assume 1:1.** The pre-read is often **trimmed** — it drops
concepts to stay lean (Week 1's pre-read kept only Prompting/RAG/Agents/Stack and **dropped the
engine internals**). Any concept hour on the **slide** that the pre-read left out **still becomes
a movement** — you teach it from the slide, and you may have to **build its widget fresh** rather
than port one (see §8). **Rule: the slide's session hours are the spine; the pre-read supplies
widgets and framing for the concepts it *did* keep. A whole act can be slide-sourced with no
pre-read section behind it** (Week 1's entire "The engine" act came from the slide's Hr 1, not the
pre-read). Confirm the full concept list from the **slide**, then note which concepts the pre-read
already armed with a widget and which you must build.

**Step 2 — group the concept hours into 2–3 acts.** An act is a themed run of movements with a
dark **act divider**. Week 1 grouped 4 pre-read sections + the engine internals into **3 acts**
(Prompting · The engine · RAG, Agents & Capstone). Pick act themes that tell a story arc, not
just buckets.

**Step 3 — expand each concept into movements.** A concept hour usually becomes **1 concept
movement** (the pre-read widget) plus, where the slide's session calls for practice, **1–2
hands-on movements**. Number them **M1…MN across the whole week** (Week 1 = M1–M13).

> **Reference prior content by NAME — never by number (movement *or* slide), never by a vague word.**
> Movement numbers (M1…MN) exist only for *you*, for the **mini-agenda badges** (where the number
> sits *beside its title*, so it's self-defining), and in the hidden `data-mv` attribute. An
> individual movement slide **never shows its own number**, and slide *positions* shift the moment
> any slide is added or removed. So **every pointer to a position is either invisible or fragile** —
> never write "in **M2**" or "on **slide 11**" in a `.hodo`, `.read`, prompt, **widget text**, or the
> presenter script.
> Instead, **point at the thing's identity — its name.** A movement's name is its own heading and
> its agenda title, so it's already on the glass: *"the loop you named in **Read your own loop**"*,
> *"the **complaint-queue agent**"*. For open/close callbacks a **time anchor** also works
> (*"the number you wrote **at 10:45**"*). A name and a time travel with the content; a number does
> not. And prefer the **name** over a vague *"earlier"* whenever the thing has one — name it.

**Step 4 — design the finale from the build hour + the homework.** The slide's Hr 5 ("build…")
and the Homework/Output become a **multi-step applied finale** (§7) — the Capstone Decider
(Week 1) or The Build (Week 2). This is where the day converges on the leader's own problem.

**Step 5 — wrap with the fixed furniture** (§10): title → timed day-plan → mini-agenda → how
today works → cold open → [acts + movements] → finale → stuck/curious → close.

**Step 6 — time it against the slide's 5 hours.** Lay out a real day-plan (breaks + lunch);
hands-on longer than teach. Week 1 = 10:30–16:30 with three breaks and a full lunch.

**The mapping rule of thumb:**

```
Front matter        = title · timed day-plan · mini-agenda · how-today-works · cold open (×2)
Acts 1..K           = the slide's concept hours, grouped; each = a dark act divider + its movements
  each movement     = dark divider (Goal + You'll decide) → teaching panel (ported widget) → .read
  hands-on movement = hobadge + copyable prompt(s) + checks + the judgment
Finale              = the build hour + homework → a multi-step applied capstone/build on THEIR problem
Back matter         = "Stuck or curious?" support · "Close" that proves the shift
```

A rich week (4 concept hours + a build hour) → **~13 movements + a 6-step finale ≈ 45–50
slides** (Week 1). Match the *content*, not a fixed count — but if your plan lands far short of
that for a comparably rich slide, you have under-built (this is exactly how Week 2 went thin:
M1–M4 + a 4-step build ≈ 30 slides).

---

## 6. The movement blueprint (every movement, in this order)

A **movement** is the atomic teaching unit. Two kinds; both share the shape **Goal → do →
judgment**.

### 6a. Concept movement (teach one idea through a ported widget)

1. **Dark movement divider** (`.slide.dark`): kicker (`Act X · Theme`) + `h1.big` title +
   a **`.goalrow`** with two boxes — **Goal** and **You'll decide** (or **You'll carry
   forward** in the finale). This is the pre-read's "Why this matters", re-cast as a decision.
2. **Teaching panel(s)** (`.slide` on paper): a `h2.head` cue + the **driveable widget** ported
   from the pre-read (`.lab …`), sized up. 1–2 panels max. The interaction **is** the teaching.
3. **`.read` band** — the **Leader's read**: one line tying the mechanism to a call they own
   (`<span class="read"><b>What you decide:</b> …</span>`). Ported from the pre-read's leader's read.
4. **Takeaway note** (`.note`, hidden) — the trainer's talk-track for this movement (§11).

### 6b. Hands-on movement (they do it on their own task)

1. **Dark movement divider** — same as above (Goal + You'll decide).
2. **Hands-on panel** (`.slide`): a **`.hobadge`** ("Hands-on · NN"), a `h2.head` cue, one or
   more **`.hodo`** instruction lines, **`.hostep`** step labels, and **`.promptblock`** copyable
   starter prompts (a `<pre>` + a **Copy** button). Give a *borrow-one* fallback so a blank page
   never stalls anyone ("Blank page? Borrow one: Finance… HR… Any function…").
3. **`.read` band** — the judgment: *which* result to keep, *what* makes it good enough, *what*
   decision it feeds.
4. **Takeaway note.**

**The starter prompts are the floor, not the ceiling** — leaders run them, then push past. Keep
them copy-clean (no stray indentation; they land in Claude Desktop verbatim).

Keep the rhythm across the deck: **frame (Goal) → do → name the call → next.**

---

## 7. The finale blueprint — the applied spine (the crown jewel)

The finale is where the day pays off and the **most common place a week goes thin.** It converts
every concept onto the leader's **own** problem and ends with an **owned, exportable artifact =
the week's homework, started live.** Build it to this pattern (calibrated to Week 1's Capstone
Decider; Week 2's "The Build" is the same shape, thinner).

**1. It runs inside a Claude Project, built up in layers.**
- **Step 1 sets the base:** the leader creates a **Project**, pastes a **router instruction**
  (how the Project runs each step) + a **base knowledge file** (the week's fundamentals + the
  criteria for a good artifact). This is RAG/grounding, working live.
- **Every later step *enriches* the Project** with **one role file** (a self-contained
  instruction the Project follows for that step), then **runs** it with a **one-line trigger**,
  then **captures** the output. Prompts stay tiny because the intelligence lives in the role
  files. This **enrich → run → capture** rhythm repeats every step and is stated on each step's
  in-slide **stepper**.

**2. Each step is a two-slide movement:** a dark divider (Goal + "You'll carry forward"), then a
hands-on panel with an **in-slide stepper** (`.stepper` / `.steppanel`) that advances with → so
the trainer walks the sub-steps without leaving the slide. Long role files sit inside a
**collapsible** `<details class="promptfold">` behind a Copy button, so the slide stays clean.

**3. It reuses a framework the cohort already knows, turned from evaluator → builder.** Week 1
reused **DRIVES** (which they'd used in March to *judge* others' AI proposals) — now applied to
their *own* initiative, filled into an interactive **AI Goals Canvas** (`.canvas` / `.dcard`
with `<textarea>` fields that persist and **export** via a "Copy my full canvas" button).

**4. It ends on a decision + an exported artifact.** Week 1: a **GO / NOT-YET / NO-GO** call plus
the completed canvas + stack map + agent spec — *that* is the capstone the leader sponsors,
builds, hardens and deploys across weeks 2–4. Name explicitly, on the last `.read` band, that
this artifact **is the homework**.

**The canonical finale step sequence** (calibrated to Week 1's 6-step Capstone Decider — reuse
the *shape*, refit the content to the week):

```
Step 1 · SET UP     — build the Project base (router + base-knowledge file). One-time scaffold.
Step 2 · SURFACE    — the tool INTERVIEWS the leader to surface their own real problem.
Step 3 · QUALIFY    — pressure-test it against a known framework's first half (W1: DRIVES D·R·S).
Step 4 · ARCHITECT  — decompose across the stack, then out-judge / push every layer down.
Step 5 · SPEC       — distil the buildable core into a one-paragraph spec, then pressure-test it.
Step 6 · VALIDATE   — the framework's second half (W1: DRIVES I·V·E) → a GO / NOT-YET / NO-GO call.
```

Not every week needs all six, but a rich build hour should have **at least: set up → surface →
qualify/architect → spec → decide.** If your finale is 3–4 one-slide steps, you have under-built.

**"The AI interviews you" is the signature surface move.** Rather than asking the leader to *pick*
a problem cold, the Project (enriched with an Interviewer role) runs a short, one-question-at-a-time
interview that *talks them into* their sharpest problem, then outputs it in a fixed template
(PROBLEM / IMPACT / AI LAYER …). Reach for this whenever the finale must start from the leader's
own work — it out-performs a blank prompt every time.

**Finale sizing check:** if the slide's build hour and homework are substantial, the finale
should be the **longest single stretch of the day** (Week 1's Capstone Decider = 6 steps /
~14 slides / two of the day's timed blocks). A 3–4 step, one-slide-each build for a rich week is
the tell-tale of an under-built deck.

---

## 8. Port the pre-read's widgets — don't reinvent

**The rule above all rules for the deck: the teaching interactions already exist in the
pre-read. Port them verbatim, size them up for projection, and drive them live.** Same
mechanism, same data, bigger type, full-bleed.

### The proven ports (Week 1 pre-read → Week 1 deck)

| Widget (pre-read → deck class) | Mechanism | Ports into |
|---|---|---|
| **Prompt builder** (`.pb`) | Toggle parts on; preview + reliability meter recompute | "Anatomy of a prompt" movement |
| **Vague-vs-structured** (`.cmp`) | Pick a task; flip vague↔structured; output + hint change | "What structure prevents" movement |
| **Token/temperature** (`.temp`) | A dial re-writes the sentence at the chosen setting | "How it predicts / play with prediction" |
| **Context-window "desk"** (`.ctxw`) | Add messages; watch the earliest fall out | "Two decisions only you make" (working memory) |
| **Stack composer** (`.build`) | Switch capabilities onto the engine; name + cost recompute | "The stack: compose, don't climb" |
| **RAG machine** (`.ragm`) | Pick a question; flip RAG off/on; retrieve + ground + cite | "RAG — ground it" |
| **Data sorter** (`.sorter`) | Classify each item OK/Never; instant per-item verdict | "The data rule" (the one self-checking widget that survives) |
| **Agent-loop graph** (`.agent2`) | Chatbot↔Agent toggle; step the loop; light nodes/edges/tools | "Agent vs chatbot — the loop" |

### Apply the two-register rule to the widget's own controls
Status-quo / "what is" state is inert and muted; the "lifted" state is teal (RAG **off** grey vs
**on** teal; Chatbot vs Agent). The control itself teaches. Use the named components (`.seg`
segmented switch, `.pill`s), never plain bordered rectangles.

### If the week's pre-read introduced a *new* widget
Port that one too (Week 2's pre-read added the **filterable labelled accordion** for
workflow-vs-agent — port it, sized up). If a concept genuinely has no pre-read widget, **invent a
driveable one** for the deck — but it must be driveable, never a passive reveal, and it must pass
"the interaction *is* the teaching."

### Build it, then drive it
After porting, run the deck and exercise **every path** of every widget. Derive state from the
DOM (read the active class), not a parallel variable, so control and logic can't desync.

---

## 9. The design canon (copy verbatim — do not reinvent)

Inline these tokens; they extend the pre-read's palette with the deck-only variables:

```css
:root{
  --ink:#16202b; --muted:#5c6b7a; --line:#e4e8ec;
  --paper:#fff; --wash:#f6f8fa; --accent:#0b6e6e; --accent-soft:#e2f0ef;
  --warn:#b06a00; --good:#1c7a4a; --bad:#b23b3b;
  --navy:#1f2a5a;               /* DRIVES canvas "what/why" cards */
  --scriptw:min(460px,42vw);    /* docked presenter-script width (audience copy hides it) */
}
```

- **Full-bleed slides.** `body` sits on a dark stage (`#0c1419`); each `.slide` is one viewport,
  `position:absolute; inset:0; overflow:auto` (a dense panel scrolls). Only `.active` shows.
- **The four registers (this is the deck's version of the Sparkline rule):**
  - `.slide` (default) = **paper**, teal accents — the teaching surface.
  - `.slide.isnow` = **wash / muted**, no teal — *status quo & framing* (cold open, day-plan,
    agenda, how-today-works, stuck, close).
  - `.slide.dark` = **deep teal `#0d2b2b`**, white heads, `#7fd1cb` kickers — **movement dividers**.
  - `.slide.act` = **near-black `#0c1419`** — **act dividers** (and the finale opener).
- **Type scales with the viewport** via `clamp()` so it projects: `h1.big` (800, up to ~3.7rem),
  `h2.head` (800), `.xl` (the one-line punch), `.lead` (serif), `.sub` (muted sans), `.kicker`
  (700, `letter-spacing:.16em`, uppercase — every slide opens with one).
- **Named components — reuse, don't invent parallels:**
  `.stage` · `h1.big`/`h2.head`/`.xl` · `.kicker` · `.lead`/`.sub` · `.read` (leader's-read
  band) · `.goalrow`+`.gb` (Goal / You'll decide) · `.cards`+`.ucard` · `.dayplan`+`.drow` ·
  `.agcols`+`.mvlist` (mini-agenda) · `.hobadge`/`.hostep`/`.hodo`/`.promptblock`/`.copy`/`.checks`
  (hands-on) · `.stepper`/`.steppanel`/`.stepcue` (in-slide steps) · `.promptfold` (collapsible
  role files) · `.lab …` (ported widgets) · `.canvas`/`.dcard`/`.dfield` (DRIVES) ·
  `.note` (Takeaway) · `.chrome`/`.progress`/`.helpbar`/`.notes` (engine).
- **Hard rules:** self-contained (inline `<style>` + vanilla `<script>`, no CDN/network/build);
  each widget its own IIFE with defensive guards (`if(!el) return;`); `@media print` stacks every
  slide on its own page, shows all `.steppanel`s statically, and drops chrome/notes/copy buttons.

---

## 10. Deck furniture (the fixed shell around the acts)

Author these once, in this order. They are the deck's spine and rarely change week to week:

1. **Title** (`.slide.active`) — program · week · a two-line `h1.big` promise + a `.lead`. One
   Takeaway: "a working session, not a lecture."
2. **Timed day-plan** (`.slide.isnow`) — the real clock (Week 1: 10:30–16:30), every block with a
   time chip; **breaks and lunch** as muted `.brk` rows; hands-on blocks tagged and **visibly
   longer**. This slide *proves* "teach a little, do a lot."
3. **Mini-agenda** (`.slide.isnow`) — `.agcols` grid: one column per act with its movements
   (hands-on tagged), plus the finale's steps as a numbered `.seqrow`. Lists **exactly** the
   movements that exist.
4. **How today works** (`.slide.isnow`) — two `.ucard`s: **the posture** (out-judge the machine)
   and **the tool** (Claude Desktop, workspace account, copy prompts off hands-on slides). A
   `.read` band states what they walk out with.
5. **Cold open** (2× `.slide.isnow`) — the keynote's job, absorbed: slide 1 names the tension
   ("AI is a black box you're told to trust"); slide 2 makes the promise ("by the end you won't
   trust it — you'll *understand* it, and you'll *own* a real problem"). Muted register — this is
   status quo before the lift. **Plant the "confidence read" here:** have each leader privately
   **rate their confidence (e.g. 1–10)** on the week's capability — the number you make them
   **re-read at the close** to prove the shift. Where it fits, open with a short **live "black-box"
   demo** (the trainer runs one striking thing on the TV) so the tension is *felt*, not just stated.
6. **[Acts + movements]** — per §6, grouped per §5.
7. **Finale** — per §7.
8. **"Stuck or curious?"** (`.slide.isnow`) — support: flag the trainer in-session; after → the
   **mid-week clinic** + **Teams doubt channel** (answered within 1 business day); terms → the
   glossary.
9. **Close** (`.slide.isnow`) — **prove the shift**: **have them re-read the confidence number**
   from the open and commit their capstone in one sentence; a direct callback to the cold open
   (Week 1: "you opened the box — and *owned* a real problem"); and a one-line hand-off to the
   homework + next week.

**The engine (copy from the Week 1 deck's `<script>`):**
- **Nav:** `→`/`Space`/`↓`/`PageDown` = next; `←`/`↑`/`PageUp` = prev;
  **`Home` = mini-agenda (slide 2-ish)**; `End` = last; `N` = notes; `F` = full-screen; `Esc`
  closes notes.
- **Click-to-advance (safe zones + selection guard):** clicking the **left 25%** of the width goes
  back, the **right 25%** goes forward, and the **middle 50% does nothing** — so the presenter can
  point at or highlight content in the middle without the slide jumping. Never advance when (a) the
  click lands on a widget, button, link, input, stepper, `details`, promptblock or note; (b) there
  is an active **text selection** (`window.getSelection().toString()` is non-empty); or (c) the
  gesture was a **drag** (mouse moved >8px between down and up). The left/right zones show a
  `pointer` cursor on hover; the middle keeps the default (so text reads as selectable). This is
  shared engine plumbing — identical in the audience and presenter decks.
- **In-slide steppers:** on a slide with `.steppanel`s, `→` advances the **sub-step** first and
  only moves to the next slide once the last sub-step is shown (and `←` reverses). Clicking a
  `.snode` jumps to that sub-step.
- **Chrome:** `<b>{act}</b> · {movement}` label + `cur / tot` counter, low corner, muted; a top
  **progress** bar.
- **Copy buttons:** every `.promptblock .copy` copies its `<pre>` (clipboard API + a
  `document.execCommand` fallback), flashing "Copied ✓".

---

## 11. Speaker notes (the Takeaway) — where the words go

The audience copy **strips the presenter Say/Do/Bridge script but keeps the Takeaway notes.**
Every slide carries a `<div class="note"><div class="t">Takeaway</div><p>…</p></div>`, hidden by
default, toggled with **`N`**.

- **The Takeaway is where prose lives.** Anything you were tempted to put on the glass as a
  paragraph belongs here instead. On-glass = cue; note = the sentence.
- **One tight paragraph per slide** — the trainer's delivery beat and the thing to land. Carry
  the **operational gold** (the "kill a weak idea with the bar" move, the fallback, the callback
  to March/last week) in the note of the slide it applies to.
- Write them as the trainer would *say* them, in executive register.

---

## 12. Voice & copy

- **British spelling, executive register** (behaviour, summarise, organised, prioritise).
- **Words-on-glass test** on every sentence: *could the trainer say this rather than show it?*
  If yes and it's more than a cue, cut it and move it to the Takeaway. Slides carry **cues,
  punches, and visuals** — not paragraphs. (Exception: a `.read` band is a deliberate one-line
  punch; the finale's role files are copy-targets, not reading.)
- **Goal / You'll decide** speak the leader's function and the call they own — never "to
  understand X."
- **`.read` band** = one line: mechanism → a decision they own. This is the pre-read's leader's
  read, re-housed.
- **Build-first register.** Make them itch to build; governance is something a builder *designs
  in* (the human-in-the-loop, the data rule), never a posture above the keyboard.
- **Callbacks land where they belong** — the close calls back to the cold open; a framework
  callback ("in March you used DRIVES to judge others…") sits on the slide that reuses it.
- **Give the hard things a memorable handle** — a short mnemonic makes a list stick (Week 1's
  prompt anatomy: **T·R·C·C·O·E**, "The Right Context Cuts Obvious Errors"). Use where a movement
  asks the room to remember a set.

---

## 13. Resources & citations

- The deck **re-teaches from zero**, so it does **not** reproduce the slide's pre-work reading
  list. Any external link that does appear (rare) is registered in
  `ai-capability-program/RESOURCES.md` with an ID and cited by ID — **no bare or invented URLs.**
- Optional "go deeper" belongs in a **Takeaway note** or the "Stuck or curious?" slide, never as
  on-glass body text.
- Verify any link before launch; never ship a dead link.

---

## 14. The build routine (slide + pre-read → shipped)

1. **Read** the week's **slide** (5 blocks) and its **finished pre-read** end to end; **open the
   Week 1 deck** as the live reference.
2. **Convert** (§5): write the **act/movement plan + finale plan + day-plan**; **agree it with
   the trainer** before any HTML.
3. **Scaffold** one self-contained HTML: tokens + registers (§9), the engine `<script>` (nav,
   steppers, copy, chrome, notes), and the fixed furniture shells (§10) — title, day-plan,
   agenda, how-today-works, cold open, stuck, close.
4. **Build the acts** (§6): dark divider (Goal + You'll decide) → ported widget panel (§8) →
   `.read` band → Takeaway, movement by movement. Thread the spine example.
5. **Build the finale** (§7): the Project base, then each step's enrich → run → capture with its
   stepper and role file; the canvas; the decision + export.
6. **Write the Takeaways** (§11) on every slide.
7. **Port + verify widgets** — every ported interaction drives on every path; state from the DOM.
8. **Verify in the browser** (§15): 0 console errors, nav + steppers + copy all work, print
   stacks every slide.
9. **Self-audit** as trainer *and* as a leader in the back row (§18); clear the **§16 checklist**;
   fix movement-number / agenda / chrome drift.
10. **Don't commit** unless the trainer says so.

---

## 15. Verify in the browser (required after meaningful changes)

The deck is observable in a browser, so prove it — don't ask the trainer to check manually.

**The sandbox recipe** (same as the pre-read; the preview-managed server can't bind a port under
the sandbox):

1. Start the host static server via Bash with `dangerouslyDisableSandbox: true` and
   `run_in_background: true`: `/opt/homebrew/bin/node .claude/static-server.js` (serves repo
   root; honours `PORT`, default 8765). If the port is held, point `.claude/launch.json` at a
   free port.
2. `preview_start`, then navigate via `preview_eval` →
   `window.location.href='http://localhost:<port>/ai-capability-program/weeks/week-N-…/01-workshop/deck-week-N-…-audience.html'`.
3. Drive it with a `preview_eval` harness: walk `→` through **every** slide, advance each
   **stepper** to its last sub-step, `.click()` each widget's controls through **every path**,
   and click each **Copy** button; return a state report.
4. Confirm **0 console errors**, the chrome label + counter track, `Home`/`End`/`N`/`F` work,
   and `@media print` stacks every slide with steppers expanded. `preview_screenshot` captures
   from the top of the active slide.

(See the memory note `preview-verification-setup` for the full recipe and gotchas.)

---

## 16. The 90% quality checklist (the bar)

A deck is not ready until **all** of these are true:

**Conversion fidelity**
- [ ] **100% slide coverage (the hard gate).** Every session hour (Hr 1–5), **every pre-work task the session consumes** (e.g. the 3 use cases), the build-sprint mechanics (pick-1-of-N · coaching · peer review · second agent · timed demos), the homework, and the output each map to a movement/slide — verified against the Step 0 slide-coverage audit. **No slide element orphaned.**
- [ ] Every concept in the slide's session (and its pre-read section) appears as a teaching movement.
- [ ] **Slide-sourced concepts the pre-read *dropped* are still built** (their widgets built fresh if needed) — no act missing because the pre-read was silent on it.
- [ ] The finale follows the canonical sequence (set up → surface/interview → qualify/architect → spec → decide) and ends on a real GO/NOT-YET/NO-GO or equivalent decision.
- [ ] The **confidence read** is planted at the cold open and **re-read at the close**.
- [ ] Every pre-read hero **widget is ported** (verbatim mechanism + data), sized up, and drives live.
- [ ] The pre-read's quizzes are **gone**, converted to "You'll decide" + hands-on judgment.
- [ ] The slide's **homework/output is produced by the finale, live** — and the slide says so.
- [ ] Movement count and finale depth match the richness of the slide (no thin M1–M4 for a rich week).

**Teaching**
- [ ] Every movement is **Goal → do → judgment**; nothing passive.
- [ ] Hands-on minutes exceed teach minutes; the day-plan proves it.
- [ ] The finale converges on the **leader's own problem** and ends with an **owned, exportable artifact**.
- [ ] One spine example threaded; callbacks (cold-open↔close, framework reuse) land where they belong.

**Register & correctness**
- [ ] **Words-on-glass** passes "say it, don't show it"; prose lives in Takeaways.
- [ ] Re-teaches from zero — no "as in the prework."
- [ ] No false simplification that breaks under an expert's eye (stack = composition, not a ladder).
- [ ] British spelling; executive register; build-first; tool reality (Claude Desktop/Projects; Claude Code watch-only).

**Build & canon**
- [ ] Self-contained (inline CSS + vanilla JS, no network); opens with `open`.
- [ ] Four registers applied (`.act` / `.dark` / `.isnow` / paper); tokens + named components used.
- [ ] **0 console errors**; nav, steppers, copy buttons, notes, full-screen all work; every widget drives on every path.
- [ ] `@media print` stacks every slide, expands steppers, drops chrome/notes/copy.
- [ ] Movement numbers, mini-agenda, chrome labels, and finale step counts all consistent.

If every box is ticked, you're at the 90% bar — what remains is taste-level iteration with the
trainer.

---

## 17. Worked example — Week 1 Slide 6 + pre-read → the shipped deck

The method applied end to end. **Slide 6** gave: *Objective* — understand the full stack
(LLM→RAG→Agents→Multi-agent) + prompting + RAG; *Session* — Hr1 debrief+LLMs, Hr2 the stack,
Hr3 prompting, Hr4 RAG, Hr5 concept of agents + write an agent spec; *Homework* — "Map the
Stack" (decompose a real problem across the stack + 3 prompts + spec the agent parts). The
**pre-read** gave four driveable sections: Prompting · RAG · Agents · The Stack.

Converted to the shipped **~47-slide deck**:

| Deck stretch | Came from | Widget ported |
|---|---|---|
| Title · day-plan · mini-agenda · how-today-works · cold open ×2 | Hr1 debrief + slide objective | — (furniture) |
| **Act 1 · Prompting** — M1 anatomy · M2 controlled experiment (H-O) · M3 build & bank 3 (H-O) · M4 what structure prevents | Pre-read "Prompting" §; slide Hr3 | prompt builder (`.pb`) · vague-vs-structured (`.cmp`) |
| **Act 2 · The engine** — M5 how it predicts (+ temperature) · M6 two decisions (context window + model) · M7 the stack | Slide Hr1 (LLMs deeper) + Hr2 (the stack); pre-read "The Stack" § | temperature (`.temp`) · context-window (`.ctxw`) · stack composer (`.build`) |
| **Act 3 · RAG, Agents & Capstone** — M8 RAG · M9 the data rule (H-O ×2) · M10 agent vs chatbot | Slide Hr4 (RAG) + Hr5 (agents); pre-read "RAG" + "Agents" §§ | RAG machine (`.ragm`) · data sorter (`.sorter`) · agent-loop (`.agent2`) |
| **Capstone Decider** — 6 steps: set up Project · AI interviews you · qualify (DRIVES 1) · architect & out-judge · write spec · validate & decide (DRIVES 2) | Slide Hr5 (write an agent spec) + Homework ("Map the Stack") | Project + role-file rhythm · DRIVES `.canvas` |
| Stuck or curious? · Close | support + "prove the shift" | — |

Spine example = the RFP / complaint / vendor world throughout. The homework ("Map the Stack" +
agent spec) is **written live** in the Capstone Decider. DRIVES is reused from the cohort's March
workshop, turned from evaluator → builder.

---

## 18. Self-audit — read it as trainer *and* as a leader in the back row

Walk the whole deck, slide by slide, and check:

- **Arc** — front matter → acts build in order → finale converges → close proves the shift. No
  concept used before its movement introduces it.
- **Say-don't-show** — every slide is a cue + a visual; no slide reads like a document; the prose
  is in the Takeaways.
- **Do-a-lot** — hands-on outweighs teach; the finale is the day's centre of gravity, not an
  afterthought.
- **Ports drive** — every widget runs, every path exercised, state from the DOM.
- **Consistency** — movement numbers, mini-agenda, chrome labels, stepper counts, finale steps
  all match the *current* content.
- **Register** — British spelling; leader altitude; build-first; tool reality respected.
- **Would it bore the back row?** If yes, rebuild it.

---

## 19. Starter kit & reuse — borrow the bones, never the body

The fastest route to a Week-1-quality deck is to **reuse the plumbing and regenerate the
teaching.** Two weeks should never *read* the same — only be *built* the same way.

| Reuse the skeleton (format / boilerplate) | Regenerate fresh every week (content) |
|---|---|
| The HTML scaffold — stage, four registers, chrome, progress, help-bar, notes | The week's acts, movement titles, and every cue |
| The engine `<script>` — nav, in-slide steppers, copy buttons, notes toggle | Every Goal / You'll-decide / `.read` band |
| The design tokens + named components (§9) | Every Takeaway note (the talk-track) |
| The furniture shells (§10) — title, day-plan, agenda, how-today-works, cold open, stuck, close | The day's real clock, the act themes, the cold-open tension + promise |
| The **widget mechanisms** — ported straight from *this week's* pre-read | Each widget's data (comes from the pre-read), the spine example |
| The finale pattern (§7) — Project + enrich→run→capture + a known framework + canvas + decision | The finale's steps, role files, the framework reused, the exported artifact |

**The line you don't cross:** copy a widget's *mechanism* and a furniture *shell*, then fill them
with **this week's** concepts and **this week's pre-read data**. If you ever paste a sentence of
Week-1 *teaching* or a Week-1 Takeaway, you've copied the body — start that piece over.

**Two warnings paid for in blood:**
- **Homework anchor.** Before designing the finale, open the week's **actual homework/output on
  the slide** and make the finale produce *that* artifact — not a plausible-sounding one.
- **Individuality.** The structure repeats; the soul doesn't. Each week earns its own acts, its
  own cold open, its own finale artifact — inside the same bones.

---

## 20. How this playbook gets better every week (the reflection loop)

This playbook is a **living benchmark**, and the latest shipped deck is the **floor, not the
ceiling.** Week 1 is the current floor.

**After each deck ships, run the loop:**
1. **Reflect** — what did the trainer/PM correct, and why? What felt like a lecture? What ran thin?
2. **Convert each correction into a one-line rule** — so the same miss can't happen twice.
3. **Promote anything better-than-benchmark** into the standard and update the relevant section.
4. **Log it** — add a dated line below.
5. **Re-benchmark** — the newest shipped deck becomes the "match or beat" reference.

**Standing rules for the loop:**
- **Every correction becomes a rule.** Feedback that lives only in chat is feedback lost.
- **The bar only goes up.** A new deck may not regress below the last.
- **Keep it lean.** When you add a rule, check whether it *replaces* a vaguer one.

**Lessons log (newest first):**
- **Week 1 (the founding benchmark):** the conversion is *slide + pre-read → deck*, not a fresh
  build. Port the pre-read's widgets verbatim; drop its quizzes; re-teach cold; make the finale
  produce the homework live on the leader's own problem via a layered Claude Project (enrich →
  run → capture) reusing a framework they already know (DRIVES). A rich slide → ~13 movements +
  a multi-step finale; anything much thinner is under-built.
- **Week 1 back-test patches (self-test of this playbook):** four gaps the first draft missed —
  (1) **slide-sourced concepts** the pre-read trimmed (a whole act can have no pre-read behind it —
  don't under-build it); (2) the **confidence-read** device (rate at open, re-read at close);
  (3) the **canonical finale step sequence**; (4) **"the AI interviews you"** as the signature
  surface move. Plus mnemonics for memorable lists. All now folded into §§5, 7, 10, 12, 16.

---

*This playbook is the contract for audience decks — and a living one. Each week makes it sharper;
the goal is that the next first draft is always a little closer to the Week-1 bar than the last.*
