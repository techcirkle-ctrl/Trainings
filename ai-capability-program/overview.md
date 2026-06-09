# AI Capability Program — Overview

A 4-week structured program to turn senior leaders from AI-aware to AI-capable. By the end, each participant has **built a working agent for their own function and has a 90-day plan to lead AI in it** — not a certificate.

---

## Who it's for

5 nominated senior GCC leaders (MD / CPO / sales & business heads). They understand the AI shift is happening; they don't yet know how to incorporate it into their day-to-day operations. This is a **leadership cohort**, not a company-wide rollout.

## The outcome contract

Every participant leaves with:
- A **production-ready agent** deployed into their team's real workflow.
- A **90-day AI project plan** they sponsor and run.
- The capability to **scope, govern, and measure** AI initiatives in their function.

**No formal grading.** Capability is evidenced by what each leader ships — the working agent and the 90-day plan speak for themselves. No scores, hours, badges, or leaderboards.

## How the depth lands (full technical depth, tiered build)

The program keeps **full technical depth** — agent lifecycle, tool use, MCP, multi-agent orchestration. For a non-engineer cohort, that depth lands through a consistent move every session:

> **Trainer demos the technical internals live in Claude Code → core leaders build the no-code equivalent in Gems / Claude Projects, anchored to their own workflow.**

**Claude Code is the trainer's master instrument** — it scaffolds projects, wires MCPs, generates the ADK code, even helps author Gems. Core leaders touch its *outputs* (Gems, connected Projects), not the terminal.

Build runs on two tracks (see the Tooling section below): a **no-code core** every leader completes, and an optional **stretch track** into Claude Code + ADK for the keen. Every concept is taught through their own function's problems, not abstractly.

## Weekly rhythm

Built on a flipped-classroom model. Each week:

```
Pre-work (self-paced)  →  Session (5 hrs, trainer-led)  →  Homework (build/apply)
                          └── mid-week clinic ──┘
```

| Phase | What |
|---|---|
| **Pre-work** | Self-paced courses + a PE reading (~3–5 hrs). Full load is retained — this cohort is committed. |
| **Session** | 5 hrs in-person, trainer-led. **Hr 1 always opens by *using* the preread** (debrief / applied exercise) — this enforces completion and makes the flipped classroom work. |
| **Mid-week clinic** | 45–60 min group build-clinic, ~3 days after the session. Bring blockers, get unblocked live. |
| **Homework** | Build or apply. Produces one concrete artifact per week. |

**Weekly load is ~13–14 hrs.** This is deliberate and accepted — the bet is on a committed cohort. Preread is therefore non-optional and is enforced in Hr 1.

## The 4-week arc

| Week | Theme | Verb | Artifact produced |
|---|---|---|---|
| **1** | AI Foundations | Understand | 2-page architecture doc — **one real problem from their function**, mapped across the AI stack |
| **2** | Agentic Deep Dive | Decode | **That problem, built as a working agent** (no-code Gem) + 1-page design doc |
| **3** | Hands-On Building | Practice | **The same agent hardened into a capstone v1** + spec + colleague feedback |
| **4** | Build & Lead | Deploy | **The capstone, productionised** + 30-day deployment + 90-day project plan |

**One escalating artifact, not four.** The problem each leader picks in Week 1 is the *same* problem they scope → build → harden → deploy across all four weeks. Each week's homework advances that single artifact; no week reseeds a new use case. This is the spine that carries the outcome contract — week-level material (spec sheets, sprints) feeds this one thread, never forks it.

Each week's detail lives in [`weeks/`](weeks/).

## Customisation — tailored to each leader

Honoring "customise ruthlessly": a **15–30 min intake call with each of the 5 before Week 1** captures their function, top pain points, the data they sit on, and the tools they use. That feeds tailored Week 2 spec sheets, live demos, and worked examples — a sales head gets sales scenarios, a CPO gets people scenarios.

## Pre-program (Week 0)

- Intake call with each leader (feeds tailoring, above).
- Provision Claude access for all 5.
- A 1-page **data-sensitivity rule** — what Sandvik data can / can't go into Claude. Leaders use real problems, so this is mandatory, not optional.
- Send the Week 1 preread links.

## Mid-week clinic & support system

The client-requested support layer. Same shape every week, described once here:

- **Mid-week build clinic** — 45–60 min video call, ~3 days after each session. Open office-hours format: each leader brings a blocker, shares screen, gets unblocked. Recorded for anyone who can't attend.
- **Async doubt channel** — dedicated **Microsoft Teams** channel + a shared doubts doc. Trainer responds **within 1 business day**; live blockers go to the clinic.
- **Peer buddies** — pairs from Week 2 for peer review between sessions.

## After the 4 weeks

2 fortnightly 1-hr check-ins with the trainer to pressure-test the 90-day plans against real results and ensure AI practices land in the workflow. Validated program then scales to the wider GCC.

## Tooling & two-track delivery

Environment: **Google Workspace**. The stack, as a capability ladder:

| Rung | Tool | Who builds | Week |
|---|---|---|---|
| 1. Prompt / chat | Claude Code · Claude chat | Leader | W1 |
| 2. Connected knowledge project | Claude Projects + connectors | Leader | W1–2 |
| 3. No-code agent | **Gems** (Workspace-connected) | Leader | W2–3 |
| 4. Tooled agent | Claude Code + MCPs | Leader *with* trainer (stretch) | W3 |
| 5. Multi-agent | **Google ADK** | Trainer demo → govern (stretch build) | W4 |

**Claude Code sits at the center** — the universal builder behind every rung. Gems and ADK are what gets produced around it.

### Two tracks

- **Core (all 5, no-code)** — rungs 1–3. Carries the entire outcome contract. Claude Projects + Gems.
- **Stretch (optional, self-selecting)** — rungs 4–5. Claude Code + MCPs, ADK multi-agent.

| Week | Core — all 5, no-code | Stretch — optional |
|---|---|---|
| **W1** | Claude chat + first connected Claude Project | Drive Claude Code — scaffold a project |
| **W2** | Build a Gem, Workspace-connected | Add an MCP / tool via Claude Code |
| **W3** | Harden the capstone (Gem / Project) | Rebuild the use case in Claude Code + MCPs |
| **W4** | Deploy no-code agent + 90-day plan | ADK multi-agent: demo → keen build |

**Guardrails:**
- The outcome contract is met **entirely on the core track**. Stretch never gates the artifact or the 90-day plan.
- **Stretch lives in the mid-week clinics + recordings, not core session time** — protects the 5-hr session and keeps the room together.
- **Multi-agent = literacy for core** (trainer-demo'd in ADK so leaders can govern it), **build for stretch**.

The client may bring its own tool preferences — these are our recommendations.

## Calendar — TO CONFIRM

- Start date · the 4 session dates & times · clinic slots (~3 days after each session).
