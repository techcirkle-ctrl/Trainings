---
name: handoff
description: Generate a cumulative session handoff document capturing all context needed for the next chat session to continue seamlessly.
argument-hint: "Optional: 'partial' for mid-session snapshot, or 'mark done [session name]' to close a handoff"
---

# Handoff Skill

Generate a cumulative handoff document at `.claude/handoffs/session-YYYY-MM-DD-HHMMSS.md`.

## When Invoked

### `/handoff` or `/handoff partial`

1. Read `.claude/handoffs/INDEX.md` to find previous handoffs for this session (match by session name)
2. If previous handoff exists, read it and merge unresolved/ongoing items with current session context
3. Drop items fully resolved in this session — they're in git history now
4. Write new handoff file using template in `HANDOFF-TEMPLATE.md`
5. Update `.claude/handoffs/INDEX.md` — add entry with filename, session name, one-line summary of pending work
6. If this is a cumulative update, mark the previous handoff entry as `[superseded]` in INDEX.md

### `/handoff mark done [session name]`

1. Read `.claude/handoffs/INDEX.md`
2. Find matching session entry
3. Append `[done]` to that entry

### Auto-done detection

When creating a handoff where all tasks from previous handoff are resolved and no new pending items exist, mark it `[done]` automatically in INDEX.md.

## Rules

- **Cumulative**: latest handoff for a session = complete context. Next session reads only that file
- **No caps**: capture everything relevant. No bullet or line limits
- **Compressed language**: apply token-optimize rules — telegraphic, no filler, no articles where unnecessary
- **No code blocks**: reference files by path:line, don't paste code
- **No raw tool output**: summarize outcomes, not stdout
- **Separate from memory**: handoff = session continuity. Don't write to memory system
- **Session name**: use the session name if given (e.g. "Master Plan"). If no name, derive from primary task

## INDEX.md Format

Each entry in INDEX.md follows this format:
```
- [session-YYYY-MM-DD-HHMMSS.md](session-YYYY-MM-DD-HHMMSS.md) — **Session Name** — summary of pending work
```

Statuses appended at end of line:
- No status = active, has pending work
- `[done]` = all work completed, no pending items
- `[superseded]` = replaced by newer cumulative handoff for same session

## Invocation Modes

- `/handoff` — full end-of-session handoff
- `/handoff partial` — mid-session snapshot, marked as partial at top
- `/handoff mark done [session name]` — mark a session's handoff as completed
