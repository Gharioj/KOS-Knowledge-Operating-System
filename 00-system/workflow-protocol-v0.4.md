# Operational Workflow Protocol — Version 0.4

*Operational protocol recording workflow improvements observed in practice. Supersedes [Version 0.3](../06-archive/00-system/workflow-protocol-v0.3.md), per decision [008](../04-decisions/008-publication-pipeline-and-rendered-output-verification.md). This version carries every Version 0.3 section forward unchanged in substance (Prompt Completeness, Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, Continuous Improvement Process), and adds two things observed during Project 001's From Wildfires to Regeneration reaching public GitHub Pages distribution: a new section — Publication Pipeline (§12) — describing the Word → GitHub → Claude Code → Markdown → GitHub Pages workflow, and an addition to Automatic Quality Assurance (§9) requiring the rendered output itself, not only repository contents, to be verified wherever a change publishes to GitHub Pages.*

## Relationship to existing documents

This protocol extends, and does not duplicate:
- [WORKFLOW.md](../WORKFLOW.md) (root) — the editorial lifecycle of content (Capture → Research → Draft → Published → On-hold → Archived). §12 below is how the Published stage reaches a public GitHub Pages audience, where a project has one; it does not change the lifecycle itself.
- [00-system/WORKFLOW.md](WORKFLOW.md) — the git pull/push/clean-tree operating procedure. This protocol assumes that procedure and adds identity verification on top of it (§3), rather than restating it.
- [AI-WORKFLOW.md](AI-WORKFLOW.md) — the Constitutional Intent model, roles, and the human checkpoint discipline. This protocol operationalises that model's "Reducing Approval to Genuine Judgement" section (§5–6 below) rather than replacing it, and its Prompt Completeness section (§1) is a way of *expressing* an intent well, not a change to what an intent is.
- [ai/PRINCIPLES.md](ai/PRINCIPLES.md) — shared AI collaborator principles, in particular "no silent structural changes" and "one source of truth." This protocol's Repository Lock and Repository Isolation sections (§3, §7) are that principle applied specifically to working across multiple repositories; its Publication Pipeline section (§12) is "one source of truth" applied specifically to the relationship between a private master, a public Markdown copy, and a rendered public page.
- [constitutional-memory.md](constitutional-memory.md) — the specification for memory and synchronisation. This protocol's "GitHub is the authoritative source" principle is the same claim that document makes for canonical state generally, applied here to repository identity specifically.
- Decision [001](../04-decisions/001-two-repository-publication-strategy.md) — the Two-Repository Publication Strategy. §12 below is the concrete mechanism that fulfils it wherever a project's public repository is a browsable website; it does not change the strategy decision 001 establishes.

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

This does not replace the Constitutional Intent model in [AI-WORKFLOW.md](AI-WORKFLOW.md) — an intent still names a desired outcome and, at most, one checkpoint, and Planning still belongs to the AI ecosystem, not the human. Prompt Completeness is about how that intent (or any other instruction) is *expressed*, not a return to specifying workflow, roles, or sequence, which remains out of scope for the human to prescribe.

Stated identity fields (repository, path, remote, branch) are inputs to Repository Verification (§3) below, not a substitute for it — a prompt stating them is checked against the actual repository state, not trusted blindly. A mismatch between a stated field and verified reality is reported before any change is made, per §3–4, rather than silently resolved by guessing which was intended.

## 2. Repository Lock

A task that names a specific target repository locks that repository for the duration of the task. No other repository may be created, modified, or committed to while a lock is in effect, regardless of how closely related it is to the locked repository. If the active working directory does not match the named repository, execution stops immediately and the mismatch is reported before any file is created or changed.

## 3. Repository Verification

Before any change, verify and report:
- current working directory;
- the git remote (must match the expected GitHub repository);
- the current branch;
- working tree status (clean or dirty, and what is outstanding if dirty).

This extends [00-system/WORKFLOW.md](WORKFLOW.md)'s existing "pull at the start of every session" rule: that rule assumes the correct repository is already checked out and asks only whether it is up to date. Repository Verification checks identity first — *which* repository is active, and whether it matches what a prompt (§1) stated — before freshness is asked at all.

## 4. Repository Recovery Protocol

If a local clone is found missing, corrupted, or inconsistent with its expected state (for example, its `.git` directory absent, or its contents unexpectedly reduced to something the current session did not itself create), do not attempt to reconstruct it by hand. Instead:

1. Treat GitHub as authoritative and verify the remote's actual state directly (for example, `git ls-remote <url> <branch>`) before assuming anything is lost.
2. Confirm what the remote holds against what is expected (for example, the last known commit hash).
3. Report the finding plainly, including any local-only content discovered during recovery — never silently discard it.
4. Re-clone fresh from the remote rather than patching a damaged local copy, once confirmed nothing local-only would be lost.

## 5. Autonomous Execution

Once a task's repository has been locked and verified, execution proceeds without pausing for intermediate confirmation, except at the checkpoints defined in §6. This extends, rather than replaces, [AI-WORKFLOW.md](AI-WORKFLOW.md#reducing-approval-to-genuine-judgment)'s existing position that a checkpoint is genuine only when it involves a new direction or a judgement the system cannot resolve on its own — not routine confirmation that already-issued work is proceeding as instructed.

## 6. Human Decision Points

Execution pauses only for:
- a genuine constitutional or structural judgement the system cannot resolve on its own, per [GOVERNANCE.md](../GOVERNANCE.md)'s decision-rights table;
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
- the commit pushes successfully and the remote is verified to hold it (see §10);
- **where a change publishes to GitHub Pages, the rendered output — the live page — is checked, not only the repository's Markdown source (see §12).** Repository contents and rendered output can diverge: a build failure, a broken relative link, or a rendering error is invisible from repository contents alone;
- **where a Constitutional Intent changes Constitutional Research Programme state, the [Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) has been updated to reflect the outcome**, per decision [009](../04-decisions/009-mandatory-dashboard-completion-condition.md) — a required Completion Condition, not an optional courtesy.

This QA pass is automatic and, on its own, does not constitute a Human Decision Point under §6 — it is part of routine execution, not a pause for judgement.

## 10. Session Completion Reports

Every execution — a single Constitutional Intent or a full autonomous batch — concludes with one concise report, produced once, covering: what was verified, what was created or changed, the outcome of automatic QA, commit hash(es), push status (verified against the remote, not assumed from the local command's exit status alone), and any issues or judgement calls requiring future review. Reports are not produced mid-task.

## 11. Continuous Improvement Process

At the end of an operational session, workflow improvements actually observed in practice — not hypothetical ones — are recorded back into this protocol, or a successor version of it, following the same decision-record discipline [GOVERNANCE.md](../GOVERNANCE.md) already requires for any structural change within `00-system/`. Version 0.2 was the first product of this process; Version 0.3 was the second; this version, adding the Publication Pipeline and rendered-output verification, is the third.

## 12. Publication Pipeline

Demonstrated in practice by Project 001 (From Wildfires to Regeneration) reaching public GitHub Pages distribution, this section describes how approved publication material moves from its authored form into a public, rendered form — the concrete mechanism that fulfils decision [001](../04-decisions/001-two-repository-publication-strategy.md)'s Two-Repository Publication Strategy wherever a project's public repository is a browsable website, without changing that strategy itself:

1. **Word.** A publication master is authored and approved as a Microsoft Word (`.docx`) document, per existing editorial practice in a project's `04-publication/`.
2. **GitHub (private).** The approved master is committed to this repository — the Initiative Lifecycle System repository — where it remains the authoritative source for that document's content.
3. **Claude Code.** Claude Code converts the approved master to Markdown, preserving content and structure, as a Constitutional Intent or ordinary editorial task, with the human's role limited to reviewing the result rather than performing the conversion by hand — the same "human thinking first, AI implementation second" principle in [ai/PRINCIPLES.md](ai/PRINCIPLES.md) applied to format conversion specifically.
4. **Markdown.** The converted file is committed to the project's public repository, per decision [001](../04-decisions/001-two-repository-publication-strategy.md). It is a one-way export refreshed by re-running the conversion when the private master changes, never edited independently in the public repository and never a second, divergently-maintained copy of the master's content.
5. **GitHub Pages.** The public repository renders its Markdown as a public website via GitHub Pages — the public documentation layer. GitHub Pages is a rendering of the public repository's Markdown, not a separate source of truth: the public repository's Markdown remains authoritative for what is displayed, and the private repository's Word master remains authoritative for content, per the "single source of truth" principle in [constitutional-memory.md](constitutional-memory.md#synchronisation-principles).

This pipeline is available to any project reaching external-distribution status; it is not mandatory where a project's public repository does not need a browsable website — decision 001 itself remains format-agnostic. Per §9 above, completing a task that runs this pipeline includes checking the rendered GitHub Pages output itself, not only the repository contents at either end.

## Principles

- GitHub is the authoritative source.
- A prompt or instruction should be self-contained wherever practical, so it does not depend on context the AI collaborator would otherwise have to reconstruct or guess.
- Always verify the repository before making changes.
- Never switch repositories without explicit instruction; treat every repository as an independent project.
- Batch related work wherever possible.
- Minimise human administrative effort — human input is reserved for governance, strategy, creativity and decision-making, per [AI-WORKFLOW.md](AI-WORKFLOW.md#constitutional-objective)'s constitutional objective, which this protocol implements operationally rather than restates.
- Interrupt the user only when a genuine decision or privileged system permission is required.
- Perform automatic QA before every commit.
- Verify push completion against the remote.
- Where a change publishes to GitHub Pages, verify the rendered output, not only the repository's Markdown source.
- GitHub Pages renders a public repository's Markdown; it is a display layer, never a second source of truth.
- Where a Constitutional Intent changes Constitutional Research Programme state, update the Constitutional Programme Dashboard as part of completing it, not only reviewing it at the start.
- Produce one concise completion report at the end of every execution.
- Record workflow improvements after every operational session.
