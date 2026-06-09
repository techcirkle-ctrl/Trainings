# Trainer notes & parked decisions

Working notes for the program. Not the contract — that's `overview.md`.

## Open decisions

- **Scaffold the leadership half earlier? — PARKED (Shekhar, decide later).**
  The outcome contract has three obligations: production agent, 90-day plan, and scope/govern/measure capability. The agent thread is cleanly scaffolded W1→W4. The **90-day plan and the govern/measure capability are currently back-loaded entirely into Week 4** — a leader drafts the plan cold in W4 Hr4 with no antecedent in W1–3.
  Option on the table: seed the 90-day plan and a lightweight "how will you measure this" hook in Week 3 so Week 4 isn't a cold start on two-thirds of the contract.
  Revisit after the Week-0 intakes (need the leader mission blocks before deciding how heavy the leadership thread should be).

## Resolved

- **Tooling** — Gems for the no-code core; **Claude Code + MCP, run as a Claude Project, is the facilitator behind everything** (trainer's master instrument). Locked in `overview.md` → Tooling & two-track delivery.
- **Agent-seed continuity** — W1 problem → W2 build → W3 capstone → W4 production is **one escalating artifact**, not four separate ones. Locked in `overview.md` → The 4-week arc. This is the spec week-planning builds to (e.g. W2 homework = "build the agent for your own W1 problem," not a provided generic spec sheet).

## Status

- **Prework format (locked, ADR 0001):** one self-contained, tabbed, interactive HTML file per week (`week-N-prework.html`). Sections teach concepts in-file (Brilliant-style widgets), mirror the run-of-show, track completion locally (localStorage), and treat external courses as optional "go deeper" links. No flow-back / no copy-to-Teams. Reference: `weeks/week-1-foundations/00-preread/week-1-prework.html`. Week 1 prework is fully built.

- **Week-level files (preread / run-of-show / homework) are indicative only.** Scaffolding from the v3 proposal — not yet authored. Real per-week planning hasn't started. The contract lives in `overview.md`; week files get built to it during week planning. Don't treat current week-file contents as decisions.
