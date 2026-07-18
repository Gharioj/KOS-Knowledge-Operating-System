# Constitutional Intent Inbox

The concrete mechanism for the ChatGPT → Claude Code leg of the handoff described in [AI-WORKFLOW.md](../AI-WORKFLOW.md#the-handoff-problem). It removes the human from retyping or pasting ChatGPT's output into a Claude Code conversation: the output is saved once, as a file, in a fixed location and format, and Claude Code reads it directly. Adopted by decision [003](../../04-decisions/003-constitutional-intent-inbox.md).

## How it works

1. The human has a conversation with ChatGPT — research, constitutional thinking, architectural design — as described in [AI-WORKFLOW.md](../AI-WORKFLOW.md).
2. The human saves ChatGPT's output as one file in [inbox/](inbox/), following the format below. This is the only manual step; it replaces retyping into Claude Code.
3. The human tells Claude Code to process the inbox, or simply starts a new session — Claude Code checks `inbox/` for pending intents automatically, per [ai/CLAUDE.md](../ai/CLAUDE.md).
4. Claude Code fulfils each intent found — implementation, documentation, commit, push — per [AI-WORKFLOW.md](../AI-WORKFLOW.md), pausing only at the intent's defined checkpoint, then removes the fulfilled file from `inbox/`. Its content is not archived separately — the resulting commit is the record.

## Format

Filename: `YYYY-MM-DD-slug.md`, e.g. `2026-07-18-promote-constitutional-capacity.md`.

```markdown
---
intent: <name from the Constitutional Intent Registry, or a new one>
issued: YYYY-MM-DD
---

<ChatGPT's research, constitutional case, or architectural proposal, pasted as produced>
```

## For ChatGPT

If useful, the human may give ChatGPT a standing instruction along these lines: *"When I ask you to issue a Constitutional Intent, produce output in this format, ready to save directly as the inbox file — frontmatter with `intent:` and `issued:`, then the substance, with no other framing."* This keeps ChatGPT's output directly usable without editing.

## Open gap

This closes only the ChatGPT → Claude Code leg. Claude Code's output already lands in GitHub, but ChatGPT has no automatic visibility into repository state — the human still carries context back to it by hand. Closing that leg is a genuine constitutional decision, not yet made — see [AI-WORKFLOW.md](../AI-WORKFLOW.md#the-handoff-problem).
