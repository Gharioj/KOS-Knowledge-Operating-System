---
title: Constitutional Programme Dashboard as a Mandatory Completion Condition
id: 009-mandatory-dashboard-completion-condition
type: decision
status: decided
owner:
created: 2026-07-21
updated: 2026-07-21
project:
tags: []
source:
---

# Decision: Constitutional Programme Dashboard as a Mandatory Completion Condition

## Context

Decision [004](004-constitutional-programme-dashboard-checkpoint.md) made the [Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) a required session-start checkpoint — reviewed before any Constitutional Intent begins — but explicitly left open "whether dashboard maintenance should become a mandatory step of every Constitutional Intent's completion condition, or remain a separately issued intent." The Dashboard's own Notes section has carried this as an open question since. A checkpoint that is only ever read and never required to be written back to drifts out of date exactly as its own Notes warn — the Dashboard states plainly it is "a manually maintained snapshot... [that] will drift out of date unless revised after each Constitutional Intent completes." Reviewing state at the start of work without any obligation to record how that state changed is an incomplete discipline.

## Decision

For any Constitutional Intent whose outcome changes Constitutional Research Programme state — a participant analysis completed, a Constitutional Question raised, evidenced, or resolved, a methodology or workflow-maturity change, a new roadmap or programme milestone — updating the [Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) to reflect that outcome is part of the intent's **Completion Condition**, per the anatomy defined in [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md#anatomy-of-a-constitutional-intent). An intent of this kind is not complete until the Dashboard reflects it, in the same commit or batch that completes the rest of the intent's work.

This does not extend to every Constitutional Intent without qualification — an intent with no bearing on Constitutional Research Programme state (for example, ordinary editorial or operational work outside `07-constitutional-methodology/`) carries no Dashboard obligation. Where it is genuinely unclear whether an intent's outcome touches programme state, [ai/PRINCIPLES.md](../00-system/ai/PRINCIPLES.md)'s existing default — treat it as structural and ask — applies.

This resolves, and closes, the open question decision 004 and the Dashboard's own Notes section left unresolved. It does not change decision 004's session-start review requirement, which stands alongside this one: the Dashboard is now both read before an affected intent begins and written to before it completes.

## Consequences

- [00-system/ai/CLAUDE.md](../00-system/ai/CLAUDE.md)'s checklist gains a new item, alongside the existing session-start review from decision 004: update the Dashboard before completing a Constitutional Intent that changes programme state.
- [00-system/workflow-protocol-v0.4.md](../00-system/workflow-protocol-v0.4.md)'s Automatic Quality Assurance (§9) gains a corresponding check, so this is verified before the completing commit, not assumed.
- The Dashboard's own Notes section is updated to record that this question is now resolved, referencing this decision.
- A Constitutional Intent that changes programme state but omits the Dashboard update is not complete under [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md)'s own definition of a Completion Condition, and per [workflow-protocol-v0.4.md](../00-system/workflow-protocol-v0.4.md) §9–10, should not be reported as finished.
- As with decisions 003, 004, 007 and 008, this is a change within `00-system/` and is recorded here per [GOVERNANCE.md](../GOVERNANCE.md).
