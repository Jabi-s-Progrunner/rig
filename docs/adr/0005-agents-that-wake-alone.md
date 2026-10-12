# 0005 · Agents that wake alone

- Status: accepted · 2026-10-30

## Context

Until now every agent in this repo ran with someone watching: a harness in a session, a human
reading along. The pulse (plan: pulse) is the first one that wakes when nobody is there, because
something happened on GitHub.

## Decision

The pulse runs on GitHub, not on anyone's machine. A comment on a pull request wakes it, and it
answers on that pull request.

## Consequences

- Nobody watches it run. Whatever its file lets it do, it can do with nobody there.
