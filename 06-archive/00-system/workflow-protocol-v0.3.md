*Archived 2026-07-21. Superseded by [00-system/workflow-protocol-v0.4.md](../../00-system/workflow-protocol-v0.4.md), per decision [008](../../04-decisions/008-publication-pipeline-and-rendered-output-verification.md). Kept here, unedited in substance, per the preserve-don't-delete principle in [ai/PRINCIPLES.md](../../00-system/ai/PRINCIPLES.md). Internal links below have been updated only so far as needed to resolve from this archived location; no other content has changed.*

---

# Operational Workflow Protocol — Version 0.3

*Operational protocol recording workflow improvements observed in practice. Supersedes [Version 0.2](KOS_Workflow_Protocol_v0.2.md), per decision [006](../../04-decisions/006-operational-workflow-protocol-v0.3.md), which also corrects that version's naming: it was written the day after the system's rename from Knowledge Operating System to Initiative Launch System (decision [002](../../04-decisions/002-rename-to-initiative-launch-system-and-constitutional-methodology.md)) but still carried the retired name in its title and filename. This version carries every Version 0.2 section forward unchanged in substance, and adds one new section — Prompt Completeness (§1) — covering how a prompt or instruction to an AI collaborator should itself be structured, a question Version 0.2 did not address.*

## Relationship to existing documents

This protocol extends, and does not duplicate:
- [WORKFLOW.md](../../WORKFLOW.md) (root) — the editorial lifecycle of content (Capture → Research → Draft → Published → On-hold → Archived). Unchanged by this document.
- [00-system/WORKFLOW.md](../../00-system/WORKFLOW.md) — the git pull/push/clean-tree operating procedure. This protocol assumes that procedure and adds identity verification on top of it (§3), rather than restating it.
- [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md) — the Constitutional Intent model, roles, and the human checkpoint discipline. This protocol operationalises that model's "Reducing Approval to Genuine Judgement" section (§5–6 below) rather than replacing it, and its Prompt Completeness section (§1) is a way of *expressing* an intent well, not a change to what an intent is.
- [ai/PRINCIPLES.md](../../00-system/ai/PRINCIPLES.md) — shared AI collaborator principles, in particular "no silent structural changes" and "one source of truth." This protocol's Repository Lock and Repository Isolation sections (§3, §7) are that principle applied specifically to working across multiple repositories.
- [constitutional-memory.md](../../00-system/constitutional-memory.md) — the specification for memory and synchronisation. This protocol's "GitHub is the authoritative source" principle is the same claim that document makes for canonical state generally, applied here to repository identity specifically.

## 1. Prompt Completeness

A prompt or instruction issued to an AI collaborator should be self-contained wherever practical, so it can be acted on correctly without relying on context accumulated earlier in a conversation. A complete prompt states:

- repository name and purpose;
- the expected local path and GitHub remote;
- the branch;
- the project or programme the work belongs to;
- the objective;
- constraints;
- deliverables;
- verification steps;
- completion criteria.

This does not replace the Constitutional Intent model in [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md) — an intent still names a desired outcome and, at most, one checkpoint, and Planning still belongs to the AI ecosystem, not the human. Prompt Completeness is about how that intent (or any other instruction) is *expressed*, not a return to specifying workflow, roles, or sequence, which remains out of scope for the human to prescribe.

Stated identity fields (repository, path, remote, branch) are inputs to Repository Verification (§3) below, not a substitute for it — a prompt stating them is checked against the actual repository state, not trusted blindly. A mismatch between a stated field and verified reality is reported before any change is made, per §3–4, rather than silently resolved by guessing which was intended.

## 2. Repository Lock

A task that names a specific target repository locks that repository for the duration of the task. No other repository may be created, modified, or committed to while a lock is in effect, regardless of how closely related it is to the locked repository. If the active working directory does not match the named repository, execution stops immediately and the mismatch is reported before any file is created or changed.

## 3. Repository Verification

Before any change, verify and report:
- current working directory;
- the git remote (must match the expected GitHub repository);
- the current branch;
- working tree status (clean or dirty, and what is outstanding if dirty).

This extends [00-system/WORKFLOW.md](../../00-system/WORKFLOW.md)'s existing "pull at the start of every session" rule: that rule assumes the correct repository is already checked out and asks only whether it is up to date. Repository Verification checks identity first — *which* repository is active, and whether it matches what a prompt (§1) stated — before freshness is asked at all.

## 4. Repository Recovery Protocol

If a local clone is found missing, corrupted, or inconsistent with its expected state (for example, its `.git` directory absent, or its contents unexpectedly reduced to something the current session did not itself create), do not attempt to reconstruct it by hand. Instead:

1. Treat GitHub as authoritative and verify the remote's actual state directly (for example, `git ls-remote <url> <branch>`) before assuming anything is lost.
2. Confirm what the remote holds against what is expected (for example, the last known commit hash).
3. Report the finding plainly, including any local-only content discovered during recovery — never silently discard it.
4. Re-clone fresh from the remote rather than patching a damaged local copy, once confirmed nothing local-only would be lost.

## 5. Autonomous Execution

Once a task's repository has been locked and verified, execution proceeds without pausing for intermediate confirmation, except at the checkpoints defined in §6. This extends, rather than replaces, [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md#reducing-approval-to-genuine-judgment)'s existing position that a checkpoint is genuine only when it involves a new direction or a judgement the system cannot resolve on its own — not routine confirmation that already-issued work is proceeding as instructed.

## 6. Human Decision Points

Execution pauses only for:
- a genuine constitutional or structural judgement the system cannot resolve on its own, per [GOVERNANCE.md](../../GOVERNANCE.md)'s decision-rights table;
- an action that is destructive, irreversible, or that would affect a repository or system beyond the one currently locked;
- a privileged system permission (credentials, force-push, rewriting remote history, or similar);
- genuine ambiguity about which repository, document, or objective is intended, where guessing would risk acting on the wrong target — including a mismatch surfaced by Repository Verification (§3) between a prompt's stated identity fields (§1) and the repository's actual state, where the discrepancy is more than a clerical slip.

Routine execution, batch drafting, verification and reporting are not decision points and should not be treated as ones.

## 7. Repository Isolation

Work performed under a task locked to Repository A must never modify Repository B, even where the two are closely related — for example, a private methodology repository and a public repository whose documentation it informs. Cross-repository consistency is achieved through separate, explicitly-scoped tasks, each with its own lock, never by a single task silently touching more than one repository. Every repository is treated as an independent project; an AI collaborator never switches which repository it is working in without explicit instruction naming the new target.

## 8. Batch Documentation Generation

Where a task defines a known, enumerable set of related documents — a numbered suite of governance documents, or a parallel-language translation of an existing suite, for example — all documents in the set should be drafted, verified and committed as a single coherent batch rather than issued as separate ad hoc requests. Commit granularity (one commit per document, or one consolidated commit for the whole batch) follows whatever the issuing task specifies; where the task is silent on this, one consolidated commit per batch is the default.

## 9. Automatic Quality Assurance

Before any commit that completes a documentation task, verify:
- document integrity — required frontmatter and structure present where the file's own conventions call for it;
- internal links resolve;
- structure (headings, numbering, tables of contents) is internally consistent, and consistent across parallel documents where applicable;
- cross-references between documents point to their correct target;
- terminology is used consistently, including that no live document introduces a retired term as if it were current;
- repository consistency — no file outside the task's intended scope has been modified;
- the commit pushes successfully and the remote is verified to hold it (see §10).

This QA pass is automatic and, on its own, does not constitute a Human Decision Point under §6 — it is part of routine execution, not a pause for judgement.

## 10. Session Completion Reports

Every execution — a single Constitutional Intent or a full autonomous batch — concludes with one concise report, produced once, covering: what was verified, what was created or changed, the outcome of automatic QA, commit hash(es), push status (verified against the remote, not assumed from the local command's exit status alone), and any issues or judgement calls requiring future review. Reports are not produced mid-task.

## 11. Continuous Improvement Process

At the end of an operational session, workflow improvements actually observed in practice — not hypothetical ones — are recorded back into this protocol, or a successor version of it, following the same decision-record discipline [GOVERNANCE.md](../../GOVERNANCE.md) already requires for any structural change within `00-system/`. Version 0.2 was the first product of this process; this version, and the naming correction it also carries, is the second.

## Principles

- GitHub is the authoritative source.
- A prompt or instruction should be self-contained wherever practical, so it does not depend on context the AI collaborator would otherwise have to reconstruct or guess.
- Always verify the repository before making changes.
- Never switch repositories without explicit instruction; treat every repository as an independent project.
- Batch related work wherever possible.
- Minimise human administrative effort — human input is reserved for governance, strategy, creativity and decision-making, per [AI-WORKFLOW.md](../../00-system/AI-WORKFLOW.md#constitutional-objective)'s constitutional objective, which this protocol implements operationally rather than restates.
- Interrupt the user only when a genuine decision or privileged system permission is required.
- Perform automatic QA before every commit.
- Verify push completion against the remote.
- Produce one concise completion report at the end of every execution.
- Record workflow improvements after every operational session.
