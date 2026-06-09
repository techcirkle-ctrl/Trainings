# Learning Record Format

Learning records live in `ai-capability-program/learning-records/` (create the directory lazily — only when the first record is written). They are the teaching equivalent of ADRs: short, decision-grade insights **about a specific leader** that change how you tailor future lessons, demos, and the zone of proximal development.

Numbered sequentially: `0001-slug.md`, `0002-slug.md`. Scan the directory for the highest number and increment.

## Template

```md
# {Leader name} — {short title of the insight}

{1–3 sentences: what was learned about this leader, and why it changes what to teach or how to tailor next.}
```

That's the whole format. A record can be one paragraph. The value is recording *that* this is now known and *why* it changes the plan.

## When to write one

- A leader **demonstrated real capability** with something non-trivial — sets a new floor; don't re-teach it.
- A leader **disclosed prior knowledge** ("I already use X") — record it and the depth claimed.
- A **misconception surfaced and was corrected** — high value; predicts where related material will trip them.
- A leader's **mission shifted** — cross-link to `MISSION.md` and update their block.

## What does NOT qualify

- Material merely covered. Coverage isn't learning — wait for evidence.
- Anything already captured in the glossary as a term.
- Session-by-session activity logs. This is not a journal — it's insights that steer tailoring.

## Supersession

When a later record corrects an earlier one, mark the old one `Status: superseded by 00NN` rather than deleting it — how a leader's understanding evolved is useful signal for the cohort.
