---
title: Constitutional Programme Dashboard as Session-Start Checkpoint
id: 004-constitutional-programme-dashboard-checkpoint
type: decision
status: decided
owner:
created: 2026-07-18
updated: 2026-07-18
project:
tags: []
source:
---

# Decision: Constitutional Programme Dashboard as Session-Start Checkpoint

## Context

[Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) was created to be "the first document opened at the beginning of every constitutional research session" and "reviewed before any future Constitutional Intent begins." A document with that intended role has no effect unless something actually requires it be checked — otherwise it is read only when someone happens to remember it exists.

## Decision

[00-system/ai/CLAUDE.md](../00-system/ai/CLAUDE.md) is updated with a checklist item: before starting work on a Constitutional Intent, Claude Code reviews the Constitutional Programme Dashboard for current programme state, alongside the existing session-start check of the [Constitutional Intent Inbox](../00-system/intents/README.md) established by decision [003](003-constitutional-intent-inbox.md).

## Consequences

- The Dashboard's stated role is now an operating instruction, not only a description of intent.
- The Dashboard remains a manually maintained snapshot — this decision makes it *checked* at the start of constitutional work, not automatically *updated* at the end of it. Whether dashboard maintenance should become a mandatory step of every Constitutional Intent's completion condition is a separate, undecided question, flagged in the Dashboard's own Notes.
- As with decision 003, this is a change within `00-system/` and is recorded here per [GOVERNANCE.md](../GOVERNANCE.md).
