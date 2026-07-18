# AI Workflow — Operating Architecture

*First draft — architecture only. Not yet implemented, not yet linked from other documents, not yet a decision. Awaiting approval.*

An operating architecture for how research, thinking, implementation and record-keeping are divided between AI collaborators and the human, so that the scarcest resource in this system — human judgment — is spent on discovery and decision, never on administration.

## Constitutional Purpose

This workflow exists to protect and multiply human creative capacity by minimising AI orchestration overhead. Every function it defines — research, design, implementation, documentation, record-keeping — exists to be performed *for* the human, not *by* the human. In the terms of [07-constitutional-methodology/constitutional-institutions.md](../07-constitutional-methodology/constitutional-institutions.md), this workflow is itself a constitutional institution: it has no standing beyond how faithfully it serves the human capacity it exists to organise around, and it is answerable to that standard, not to its own continuity.

## Principles

1. **Human capacity is the constrained resource.** Every AI function in this workflow exists to protect the human's time and attention for discovery, judgment and decision — not to occupy it with administration.
2. **One system, one constitutional function.** Each AI performs the function it is structurally suited to, without overlapping general-purpose duplication — so responsibility for any given output traces cleanly to one system.
3. **GitHub is the sole canonical record.** A decision, definition or draft is not yet real within this system until it is written to the repository and committed. Conversation history, in either AI, is working memory, not the record.
4. **Human involvement concentrates at decision points, not administration.** Approvals are reserved for moments that genuinely require judgment — a new direction, a structural change, a constitutional position — not for mechanical steps that follow directly from a decision already made.
5. **Handoffs are structured, not manual.** What moves between AI systems is a defined artifact — a scoped brief, a drafted document — not free-form text the human must retype, reformat or reconcile by hand.
6. **The workflow is reusable, not bespoke.** It applies uniformly to every initiative launched within the Initiative Launch System; it is not rebuilt per project.

## Architecture

### ChatGPT — Research, Constitutional Thinking, Architectural Design

Responsible for gathering and synthesising research, working through constitutional concepts, and proposing structure and architecture before anything is built. Its output is a scoped brief or draft precise enough that Claude Code can act on it directly — naming the target document, the intended sections, and the substance to develop — without the human mediating the handoff.

### Claude Code — Implementation, Documentation, GitHub Management, Repository Maintenance

Responsible for turning approved direction into actual repository state: creating and editing files, applying [METADATA.md](../METADATA.md) and [NAMING.md](../NAMING.md), committing, pushing, and keeping the changelog and decision records current. Implements direction; does not originate it, per [PRINCIPLES.md](ai/PRINCIPLES.md).

### GitHub — Canonical Knowledge Base

The repository is the only place a decision, definition or draft is considered to exist. Both AI systems operate against the same repository state rather than diverging copies of context carried in separate conversations — this is what allows a handoff between them to be a pointer to a commit, not a manual transcript.

### Human — Discovery, Judgment, Decision-Making

The human's role narrows deliberately to what only a human can do here: originate direction, evaluate proposals, decide, approve. Not retyping content between systems. Not manually tracking what has or hasn't been committed. Not performing mechanical edits that either AI can already do correctly once given a clear brief.

## Reducing Repetitive Prompting and Approvals

- Work proceeds in scoped units — one discovery, one document, one commit — so each approval covers a complete, reviewable piece of work rather than an open-ended stream.
- Approval is requested at structural or constitutional decision points, not at every routine edit that follows from a decision already approved.
- This document itself is the standing brief for the division of labour, so each new initiative starts from a known architecture instead of re-explaining roles from scratch.

## Notes

This is a first draft: architecture only, not yet implemented, and not yet linked from [00-system/README.md](README.md) or recorded as a decision in [04-decisions/](../04-decisions/README.md). Per [GOVERNANCE.md](../GOVERNANCE.md), formal adoption of this workflow — and any change to it once adopted — requires a decision record, since it is a change within `00-system/`.
