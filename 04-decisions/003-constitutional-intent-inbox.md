---
title: Constitutional Intent Inbox
id: 003-constitutional-intent-inbox
type: decision
status: decided
owner:
created: 2026-07-18
updated: 2026-07-18
project:
tags: []
source:
---

# Decision: Constitutional Intent Inbox

## Context

[AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) identifies the human as the physical carrier of content between ChatGPT and Claude Code as the one piece of orchestration current tooling had not yet removed ("The Handoff Problem"). The constitutional objective — maximise human creative capacity by minimising AI orchestration — requires closing this gap wherever it can be closed without new external integrations, so the human is no longer required to retype or paste ChatGPT's output into a Claude Code conversation.

## Decision

A new structure, `00-system/intents/`, is added:

1. **`00-system/intents/inbox/`** — the fixed location where the human saves ChatGPT's output (research, constitutional thinking, architectural design) as a single Markdown file, in a fixed frontmatter-plus-body format documented in [00-system/intents/README.md](../00-system/intents/README.md).
2. **Claude Code checks this inbox at the start of every session**, per an added instruction in [ai/CLAUDE.md](../00-system/ai/CLAUDE.md), and fulfils any pending Constitutional Intent found there — implementation, documentation, commit, push — without the human pasting its content into the conversation.
3. **[00-system/AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) and [00-system/README.md](../00-system/README.md) are updated** to reflect this as the first working piece of the Constitutional Intent model, distinct from the rest of the model, which remains an unadopted proposal.

This closes only the ChatGPT → Claude Code leg of the handoff. The Claude Code → ChatGPT leg — giving ChatGPT visibility into repository state without the human carrying it by hand — remains open and is not decided here.

## Consequences

- The human's role in a ChatGPT-originated intent narrows to one action: saving ChatGPT's output as one file in `00-system/intents/inbox/`. No further pasting into Claude Code is required.
- Claude Code's session-start behaviour changes: it now checks a fixed location for pending work before other activity, per [ai/CLAUDE.md](../00-system/ai/CLAUDE.md).
- The inbox file's content is not archived separately; it is preserved in the git commit that fulfils it and then removed from `inbox/`, keeping GitHub as the sole canonical record.
- The wider Constitutional Intent model in [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) remains an unadopted proposal; this decision adopts only the inbox mechanism as working infrastructure.
