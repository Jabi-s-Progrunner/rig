---
plan: pulse
status: ready
owner: rook
opened: 2026-10-30
---

# Pulse

rig is in the lane now, and the lane is empty most of the day. Rook still wants to know where
things stand, and he won't open anyone's machine to find out. He asks on a pull request. The
answer has to be there, from whatever stays up when nobody is at the keyboard.

Out of scope: dashboards, notifications, answering anywhere but the pull request.

## 1. The file

`.github/workflows/pulse.yml`. Rook asks for it on the PR: `pulse? <phrase>`. The phrase is new
every time.

Done when: Rook's ask gets an answer on the PR without anyone touching it.

## 2. What it reads

- this file, and `docs/plans/done/` for what already happened
- the tracker: the issues on the upstream repo (`rig`'s home, not your copy of it)

Done when: every issue the pulse names is one the tracker shows that way when it answers.

## 3. What it posts

One comment on the PR:

- Rook's phrase, quoted
- one open issue that matters for this plan, linked
- one recommendation tied to that issue

Never call an open issue shipped.

Done when: Rook reads the comment and doesn't have to ask twice.

## 4. When it stops

A check fails (no phrase, no tracker, nothing open): say what failed, in one line, and stop.

Done when: a failed check leaves one line on the PR, not silence and not a guess.

## Known issues (as of 30 Oct)

| # | Issue | State |
|---|-------|-------|
| 8 | Board shows a stale beat after the laptop sleeps | open |
| 9 | Digest counts a retried-then-ok job as failed | open |
| 10 | Board link 404s for a night with an empty file | open |
| 11 | Heartbeat drifts a few seconds an hour | open |
| 12 | Digest prints `null` instead of `—` for a missing owner | shipped |
