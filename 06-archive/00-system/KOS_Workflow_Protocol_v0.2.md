*Archived 2026-07-20. Superseded by [00-system/workflow-protocol-v0.3.md](../../00-system/workflow-protocol-v0.3.md), per decision [006](../../04-decisions/006-operational-workflow-protocol-v0.3.md), which also corrects this document's use of the retired "KOS" name. Kept here, unedited in substance, per the preserve-don't-delete principle in [ai/PRINCIPLES.md](../../00-system/ai/PRINCIPLES.md). Internal links below have been updated only so far as needed to resolve from this archived location; no other content has changed.*

---

# KOS Workflow Protocol — Version 0.2

*Operational protocol recording workflow improvements observed during practice, most recently a session spanning work across the POLiPHONiC, From-Wildfires-to-Regeneration and Initiative Launch System repositories. This document sits alongside [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md) and [WORKFLOW.md](../../00-system/WORKFLOW.md): it does not restate either, but adds the operational detail practice has since shown to be necessary. Version 0.1 did not exist as a separate document; this is the first version, consolidating practice that had previously been applied ad hoc.*

## Relationship to existing documents

This protocol extends, and does not duplicate:
- [WORKFLOW.md](../../WORKFLOW.md) (root) — the editorial lifecycle of content (Capture → Research → Draft → Published → On-hold → Archived). Unchanged by this document.
- [00-system/WORKFLOW.md](../../00-system/WORKFLOW.md) — the git pull/push/clean-tree operating procedure. This protocol assumes that procedure and adds identity verification on top of it (Section 2), rather than restating it.
- [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md) — the Constitutional Intent model, roles, and the human checkpoint discipline. This protocol operationalises that model's "Reducing Approval to Genuine Judgement" section (Sections 4–5 below) rather than replacing it.
- [ai/PRINCIPLES.md](../../00-system/ai/PRINCIPLES.md) — shared AI collaborator principles, in particular "no silent structural changes" and "one source of truth." This protocol's Repository Lock and Repository Isolation sections are that principle applied specifically to working across multiple repositories.
- [constitutional-memory.md](../../00-system/constitutional-memory.md) — the specification for memory and synchronisation. This protocol's "GitHub is the authoritative source" principle is the same claim that document makes for canonical state generally, applied here to repository identity specifically.

## 1. Repository Lock

A task that names a specific target repository locks that repository for the duration of the task. No other repository may be created, modified, or committed to while a lock is in effect, regardless of how closely related it is to the locked repository. If the active working directory does not match the named repository, execution stops immediately and the mismatch is reported before any file is created or changed.

## 2. Repository Verification

Before any change, verify and report:
- current working directory;
- the git remote (must match the expected GitHub repository);
- the current branch;
- working tree status (clean or dirty, and what is outstanding if dirty).

This extends [00-system/WORKFLOW.md](../../00-system/WORKFLOW.md)'s existing "pull at the start of every session" rule: that rule assumes the correct repository is already checked out and asks only whether it is up to date. Repository Verification checks identity first — *which* repository is active — before freshness is asked at all.

## 3. Repository Recovery Protocol

If a local clone is found missing, corrupted, or inconsistent with its expected state (for example, its `.git` directory absent, or its contents unexpectedly reduced to something the current session did not itself create), do not attempt to reconstruct it by hand. Instead:

1. Treat GitHub as authoritative and verify the remote's actual state directly (for example, `git ls-remote <url> <branch>`) before assuming anything is lost.
2. Confirm what the remote holds against what is expected (for example, the last known commit hash).
3. Report the finding plainly, including any local-only content discovered during recovery — never silently discard it.
4. Re-clone fresh from the remote rather than patching a damaged local copy, once confirmed nothing local-only would be lost.

This generalises a real recovery performed during this session's POLiPHONiC work, where a local clone's content had disappeared between sessions; the remote was verified intact before a clean re-clone was performed.

## 4. Autonomous Execution

Once a task's repository has been locked and verified, execution proceeds without pausing for intermediate confirmation, except at the checkpoints defined in Section 5. This extends, rather than replaces, [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md#reducing-approval-to-genuine-judgment)'s existing position that a checkpoint is genuine only when it involves a new direction or a judgement the system cannot resolve on its own — not routine confirmation that already-issued work is proceeding as instructed.

## 5. Human Decision Points

Execution pauses only for:
- a genuine constitutional or structural judgement the system cannot resolve on its own, per [GOVERNANCE.md](../../GOVERNANCE.md)'s decision-rights table;
- an action that is destructive, irreversible, or that would affect a repository or system beyond the one currently locked;
- a privileged system permission (credentials, force-push, rewriting remote history, or similar);
- genuine ambiguity about which repository, document, or objective is intended, where guessing would risk acting on the wrong target.

Routine execution, batch drafting, verification and reporting are not decision points and should not be treated as ones.

## 6. Repository Isolation

Work performed under a task locked to Repository A must never modify Repository B, even where the two are closely related — for example, a private methodology repository and a public repository whose documentation it informs. Cross-repository consistency is achieved through separate, explicitly-scoped tasks, each with its own lock, never by a single task silently touching more than one repository. This reflects this session's own experience of working across three separate repositories (POLiPHONiC, From-Wildfires-to-Regeneration, and this one) in sequence, each under its own explicit repository lock.

## 7. Batch Documentation Generation

Where a task defines a known, enumerable set of related documents — a numbered suite of governance documents, or a parallel-language translation of an existing suite, for example — all documents in the set should be drafted, verified and committed as a single coherent batch rather than issued as separate ad hoc requests. Commit granularity (one commit per document, or one consolidated commit for the whole batch) follows whatever the issuing task specifies; where the task is silent on this, one consolidated commit per batch is the default.

## 8. Automatic Quality Assurance

Before any commit that completes a documentation task, verify:
- internal links resolve;
- structure (headings, numbering, tables of contents) is internally consistent, and consistent across parallel documents where applicable;
- cross-references between documents point to their correct target;
- terminology is used consistently;
- no file outside the task's intended scope has been modified.

This QA pass is automatic and, on its own, does not constitute a Human Decision Point under Section 5 — it is part of routine execution, not a pause for judgement.

## 9. Session Completion Reports

Every execution — a single Constitutional Intent or a full autonomous batch — concludes with one concise report, produced once, covering: what was verified, what was created or changed, the outcome of automatic QA, commit hash(es), push status (verified against the remote, not assumed from the local command's exit status alone), and any issues or judgement calls requiring future review. Reports are not produced mid-task.

## 10. Continuous Improvement Process

At the end of an operational session, workflow improvements actually observed in practice — not hypothetical ones — are recorded back into this protocol, or a successor version of it, following the same decision-record discipline [GOVERNANCE.md](../../GOVERNANCE.md) already requires for any structural change within `00-system/`. This document is itself the first product of that process.

## Principles

- GitHub is the authoritative source.
- Always verify the repository before making changes.
- Never switch repositories without explicit instruction.
- Batch related work wherever possible.
- Interrupt the user only when a genuine decision or privileged system permission is required.
- Perform automatic QA before every commit.
- Verify push completion against the remote.
- Produce one concise completion report at the end of every execution.
- Record workflow improvements after every operational session.
