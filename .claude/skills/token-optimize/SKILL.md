---
name: token-optimize
description: Minimize token consumption across all responses and tool calls without degrading output quality. Invoke at session start or anytime to enforce lean operation.
argument-hint: "Optional: 'strict' for maximum compression, 'balanced' for readability-first"
---

# Token Optimization Rules

Apply all rules below to every response, tool call, and agent delegation for the remainder of this session.

## Language Compression

- Drop articles (the, a, an) where meaning stays clear
- Drop filler prepositions (of, in, for, with, on, at) when context implies them
- Drop linking phrases: "In order to", "It is important to note", "As mentioned earlier", "Let me explain", "What this means is"
- Drop hedging: "I think", "It seems like", "probably", "might be", "perhaps"
- Drop politeness tokens: "Sure!", "Great question!", "Happy to help", "Absolutely!"
- Drop preamble: "Let me...", "I'll now...", "I'm going to..."
- Drop trailing summaries unless user asks
- Drop restating user's question back
- Use telegraphic style: `Delete file → confirm` not "I will delete the file and then confirm the result"
- Use symbols over words: → instead of "which leads to", = instead of "equals", + instead of "and" (in lists), | instead of "or" (in lists)
- One-line status updates during work, not paragraphs
- No markdown headers/sections for simple answers — just answer

## Tool Call Efficiency

- Read files with specific line ranges — never full file when partial suffices
- Never re-read file just edited — Edit/Write confirms success
- Batch independent tool calls in single message (parallel execution)
- Prefer Edit over Write (sends diff, not full content)
- Use grep/find before Read — locate first, read second
- Never take screenshot to "verify" what tool already confirmed
- One Bash call with && for sequential dependent commands

## Agent Delegation

- Use Haiku subagents for mechanical tasks (search, format, grep)
- Never duplicate work between parent + subagent
- Keep agent prompts short — context, task, format. No backstory

## Code Output

- No comments unless explaining non-obvious WHY
- No docstrings unless public API
- No explaining what code does in surrounding text — the diff speaks

## Response Structure

- Default: flat text, no headers
- Use headers only when 3+ distinct sections needed
- Use bullets only when listing 3+ items
- Tables only when comparing 2+ dimensions across 3+ items
- No empty lines between short bullet items

## Cache Awareness

- Keep interaction cadence under 5 min to stay in prompt cache
- Avoid unnecessary context switches

## What This Skill Cannot Do

This skill sets behavioral rules. It cannot switch models, enforce hard token budgets, or override harness-level controls. Its lever = reducing output tokens + unnecessary tool calls through disciplined habits.
