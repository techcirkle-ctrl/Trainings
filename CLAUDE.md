# Project Instructions

Always follow the token optimization rules defined in `.claude/skills/token-optimize/SKILL.md`. Apply them to every response, tool call, and agent delegation throughout the session.

When user says "continue", "resume", "pick up where I left off", "what was I working on", "what's pending", or references a previous session by name — read `.claude/handoffs/INDEX.md`, present active (non-done) handoffs, and let user pick which to load. Do not auto-load handoffs at session start.
