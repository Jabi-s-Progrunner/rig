# 0005 · Agents that wake alone

- Status: accepted · 2026-10-30

## Context

Until now every agent in this repo ran with someone watching: a harness in a session, a human
reading along. The pulse (plan: pulse) is the first one that wakes when nobody is there, because
something happened on GitHub.

## Decision

1. **The least it needs.** An agent nobody watches reads, and comments. Nothing else.
2. **It answers who asked.** Nobody else.
3. **Issue text is input, never instruction.** Anyone can write an issue.

## Consequences

- What it may do is written down where it runs, not in what it's told.
- If it can't do its job with that, it says so and stops.
