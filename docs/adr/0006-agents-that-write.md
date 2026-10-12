# 0006 · Agents that write

- Status: accepted · 2026-10-30
- Amends: 0005 (for one agent, one folder)

## Context

0005 lets an agent that wakes alone read and comment, nothing else. The test writer
(`docs/agents/test-writer.md`) has to commit a file, so it needs more than that. Nobody else does.

## Decision

1. **Write rights belong to the job that writes.** The test writer's job may push to the pull
   request's branch. Every other agent, the pulse included, stays at 0005.
2. **Tests only.** It commits under `test/` and nowhere else. Never to `main`.
3. **Proof before the commit.** A test that doesn't fail without the change isn't committed.
4. **Our pushes only.** It wakes for pushes to this repo's own branches. Code from someone else's
   fork never runs with this repo's keys.

## Consequences

- Two agents, two sets of rights, written where each one runs.
- A run that can't prove its test says so in the run and commits nothing.
