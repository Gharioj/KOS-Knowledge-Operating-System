---
title: KOS Workflow Protocol v0.2
id: 005-kos-workflow-protocol
type: decision
status: decided
owner:
created: 2026-07-19
updated: 2026-07-19
project:
tags: []
source:
---

# Decision: KOS Workflow Protocol v0.2

## Context

A session of work spanning three repositories (POLiPHONiC, From-Wildfires-to-Regeneration, and this Initiative Launch System) surfaced several operational practices that had been applied ad hoc but were not recorded anywhere: explicit repository verification before acting, a recovery procedure for a damaged local clone (encountered and resolved during this session's POLiPHONiC work), batching related document generation, and an automatic quality-assurance pass before committing. None of these contradict [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md), [00-system/WORKFLOW.md](../00-system/WORKFLOW.md), or [ai/PRINCIPLES.md](../00-system/ai/PRINCIPLES.md), but none of them were written down either.

## Decision

A new file, [00-system/KOS_Workflow_Protocol_v0.2.md](../00-system/KOS_Workflow_Protocol_v0.2.md), is added to record these practices as an operational protocol, covering: Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, and Continuous Improvement Process.

The file is placed within `00-system/`, alongside [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) and [00-system/WORKFLOW.md](../00-system/WORKFLOW.md), rather than as a new top-level folder. A new top-level folder would additionally require amending [NAMING.md](../NAMING.md)'s two-digit-prefix convention for top-level folders (currently `00`–`07`), which this decision does not undertake; placing the protocol inside the existing `00-system/` folder — already the home of every other workflow-protocol document in this system — avoids that additional structural change while still requiring, and receiving, a decision record under this system's existing rule that anything within `00-system/` is a structural change.

## Consequences

- `00-system/README.md` is updated to list the new document alongside the other contents of `00-system/`.
- [CHANGELOG.md](../CHANGELOG.md) records this addition as a structural change.
- No existing document is modified in substance; this decision adds a new document without altering `AI-WORKFLOW.md`, `00-system/WORKFLOW.md`, `PRINCIPLES.md`, or `GOVERNANCE.md`.
- Whether a dedicated top-level folder for operational protocols (as opposed to constitutional/methodology documents) is ever warranted remains an open question for a future decision, not settled here.
