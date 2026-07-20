---
title: Operational Workflow Protocol v0.3 — Self-Contained Prompts and Naming Correction
id: 006-operational-workflow-protocol-v0.3
type: decision
status: decided
owner:
created: 2026-07-20
updated: 2026-07-20
project:
tags: []
source:
---

# Decision: Operational Workflow Protocol v0.3 — Self-Contained Prompts and Naming Correction

## Context

A set of proposed operational-workflow enhancements was reviewed against `00-system/KOS_Workflow_Protocol_v0.2.md` (adopted by decision [005](005-kos-workflow-protocol.md); now archived at [06-archive/00-system/KOS_Workflow_Protocol_v0.2.md](../06-archive/00-system/KOS_Workflow_Protocol_v0.2.md) as a result of this decision). Nearly all of the proposed enhancements — Repository Lock, Repository Verification, autonomous execution, batching related work, automatic quality assurance, session completion reports, treating GitHub as authoritative, and continuous methodology improvement — are already present in v0.2 in substance. Genuinely new is a single requirement not previously specified: that a prompt issued to an AI collaborator should be self-contained (repository identity, purpose, objective, constraints, deliverables, verification steps, completion criteria), rather than relying on accumulated conversational context.

Separately, v0.2's own filename and title use "KOS" — the retired name of this system, per decision [002](002-rename-to-initiative-launch-system-and-constitutional-methodology.md) — despite having been created the day after that rename decision was recorded. This is a live-document naming inconsistency, not a preserved historical reference, and this decision corrects it while the document is already being revised.

## Decision

1. **`00-system/KOS_Workflow_Protocol_v0.2.md` is superseded by `00-system/workflow-protocol-v0.3.md`.** The new document carries forward every v0.2 section unchanged in substance (Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, Continuous Improvement Process), and adds one new section — **Prompt Completeness** — specifying the self-contained-prompt structure. The new filename follows [NAMING.md](../NAMING.md)'s lowercase-kebab-case convention, which `KOS_Workflow_Protocol_v0.2.md` did not.
2. **The superseded v0.2 file is archived**, not deleted, to `06-archive/00-system/KOS_Workflow_Protocol_v0.2.md`, per the preserve-don't-delete principle in [ai/PRINCIPLES.md](../00-system/ai/PRINCIPLES.md), with a note pointing to this decision and its replacement.
3. **This is an operational-methodology-layer change only.** It does not alter [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md)'s Constitutional Intent model, [GOVERNANCE.md](../GOVERNANCE.md), or [ai/PRINCIPLES.md](../00-system/ai/PRINCIPLES.md) — the Prompt Completeness section extends how an intent or instruction is best expressed; it does not change who decides what, or the constitutional objective those documents already establish.

## Consequences

- `00-system/README.md`, `CHANGELOG.md`, and `04-decisions/README.md` are updated to reference `workflow-protocol-v0.3.md` in place of the v0.2 file.
- Decision [005](005-kos-workflow-protocol.md) is left untouched, per the immutability rule in [WORKFLOW.md](../WORKFLOW.md) — it remains an accurate historical record of what was decided on 2026-07-19, even though the document it adopted has since been superseded.
- Future revisions to the workflow protocol follow the same pattern: a new version, a new decision record, the prior version archived rather than edited in place.
