# Changelog

Structural changes to the Initiative Lifecycle System. Content changes within projects are not logged here.

## 4.4.0 — 2026-07-21
Began physical repository identity migration: the local repository folder is renamed from `Knowledge Operating System` to `Initiative Lifecycle System`, completing the documentation-to-identity alignment decisions 002 and 007 deliberately deferred. See decision [011](04-decisions/011-physical-repository-identity-migration.md).

- `NAMING.md`'s Exception section rewritten to record the migration rather than a permanent "left as-is" position.
- `02-knowledge/glossary.md`'s Knowledge Operating System (KOS) entry updated: the physical identifiers are no longer described as unchanged.
- Root `README.md`'s subtitle updated to reference decision 011.
- The GitHub remote rename (`Gharioj/KOS-Knowledge-Operating-System` → `Gharioj/ILS-Initiative-Lifecycle-System`) is a manual step outside this environment's reach — see the accompanying completion report for exact steps. `git remote -v` will continue to show the prior URL until it is performed and the local remote is updated to match.
- Decisions 002 and 007 are not edited; this decision supersedes only their "left as-is" position on physical identifiers.

## 4.3.0 — 2026-07-21
Adopted the Single Origination Principle: a project's public repository never originates content — every file it holds must trace back to an approved master in this repository first. Reinforces decision [001](04-decisions/001-two-repository-publication-strategy.md) explicitly, following a methodology consistency audit that found public-repository content with no traceable private-repository master. See decision [010](04-decisions/010-single-origination-principle.md).

- `00-system/workflow-protocol-v0.4.md` §12 (Publication Pipeline) amended to state the principle explicitly, including that content found in a public repository with no traceable master is a methodology inconsistency to be reported, not assumed correct.
- `00-system/ai/CLAUDE.md`'s checklist gains an explicit instruction: never create or edit content directly in a project's public repository, even under a task locked to that repository.
- `00-system/ai/PRINCIPLES.md`'s "One source of truth" principle extended with a cross-repository clause.
- `02-knowledge/glossary.md`'s GitHub Pages entry extended to state the principle directly.
- This audit and remediation touched only this repository; the From Wildfires to Regeneration repository and its public website were not modified.

## 4.2.0 — 2026-07-21
Made updating the Constitutional Programme Dashboard a mandatory Completion Condition for any Constitutional Intent that changes Constitutional Research Programme state, resolving the question decision [004](04-decisions/004-constitutional-programme-dashboard-checkpoint.md) left open. See decision [009](04-decisions/009-mandatory-dashboard-completion-condition.md).

- `00-system/ai/CLAUDE.md`'s checklist gains a new item: update the Dashboard before completing a Constitutional Intent that changes programme state, alongside the existing session-start review from decision 004.
- `00-system/AI-WORKFLOW.md`'s Anatomy of a Constitutional Intent section notes that an affected intent's Completion Condition includes the Dashboard update.
- `00-system/workflow-protocol-v0.4.md`'s Automatic Quality Assurance (§9) and Principles gain a corresponding check.
- `07-constitutional-methodology/constitutional-programme-dashboard.md`'s own Notes section updated to record the question as resolved.

## 4.1.0 — 2026-07-21
Added `00-system/workflow-protocol-v0.4.md`, recording the publication pipeline demonstrated by Project 001's From Wildfires to Regeneration reaching public GitHub Pages distribution, and adding rendered-output verification to Automatic Quality Assurance. See decision [008](04-decisions/008-publication-pipeline-and-rendered-output-verification.md).

- New `00-system/workflow-protocol-v0.4.md` — carries every Version 0.3 section forward unchanged in substance, adds a new §12 Publication Pipeline (Word → GitHub → Claude Code → Markdown → GitHub Pages), and adds a rendered-output-verification requirement to §9 Automatic Quality Assurance.
- `00-system/workflow-protocol-v0.3.md` archived to `06-archive/00-system/workflow-protocol-v0.3.md`, per the preserve-don't-delete principle — not deleted, its content unchanged in substance.
- `00-system/README.md` updated to reference the new document.
- Root `WORKFLOW.md`'s Published stage updated to note that a project's public repository, where one exists, may render publication material via GitHub Pages.
- `02-knowledge/glossary.md` gains an entry for GitHub Pages.
- This extends, and does not supersede, decision [001](04-decisions/001-two-repository-publication-strategy.md)'s Two-Repository Publication Strategy.

## 4.0.0 — 2026-07-21
Evolved from Initiative Launch System (ILS) to Initiative Lifecycle System (ILS), reflecting the system's demonstrated support for an initiative's complete lifecycle — design, development, governance, documentation, publication, collaboration, maintenance and continuous improvement — rather than only its initial launch. See decision [007](04-decisions/007-evolve-to-initiative-lifecycle-system.md).

- All live references to "Initiative Launch System" updated to "Initiative Lifecycle System" across root standards and system documentation; the acronym ILS is unchanged. Historical records — decisions [001](04-decisions/001-two-repository-publication-strategy.md)–[006](04-decisions/006-operational-workflow-protocol-v0.3.md) and prior entries below — keep their original wording.
- `README.md`'s opening definition updated to the canonical description: "a complete operating system for designing, developing, governing, documenting, publishing, collaborating on, maintaining and continuously improving initiatives."
- `02-knowledge/glossary.md` updated: new entry for Initiative Lifecycle System (ILS); the prior Initiative Launch System (ILS) entry retained, marked as an interim, retired name, alongside the existing Knowledge Operating System (KOS) entry.
- `00-system/AI-WORKFLOW.md`'s description of the constitutional operating model's scope broadened to name the full lifecycle explicitly.
- The repository root folder name and GitHub remote name are unchanged, per the existing exception in [NAMING.md](NAMING.md).

## 3.4.0 — 2026-07-20
Replaced `00-system/KOS_Workflow_Protocol_v0.2.md` with `00-system/workflow-protocol-v0.3.md`, adding a Prompt Completeness section and correcting the prior version's use of the retired "KOS" name. See decision [006](04-decisions/006-operational-workflow-protocol-v0.3.md).

- New `00-system/workflow-protocol-v0.3.md` — carries every section of Version 0.2 forward unchanged in substance (Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, Continuous Improvement Process), and adds a new Prompt Completeness section specifying that a prompt to an AI collaborator should be self-contained (repository identity, purpose, objective, constraints, deliverables, verification steps, completion criteria).
- `00-system/KOS_Workflow_Protocol_v0.2.md` archived to `06-archive/00-system/KOS_Workflow_Protocol_v0.2.md`, per the preserve-don't-delete principle — not deleted, its content unchanged in substance.
- `00-system/README.md` updated to reference the new document.
- No change to `AI-WORKFLOW.md`, `GOVERNANCE.md`, or `ai/PRINCIPLES.md` — this is an operational-methodology-layer change only.

## 3.3.0 — 2026-07-19
Added `00-system/KOS_Workflow_Protocol_v0.2.md`, recording workflow improvements observed during a session spanning work across the POLiPHONiC, From-Wildfires-to-Regeneration and Initiative Launch System repositories. See decision [005](04-decisions/005-kos-workflow-protocol.md).

- New `00-system/KOS_Workflow_Protocol_v0.2.md` — covers Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, and Continuous Improvement Process. Extends, and does not duplicate, `AI-WORKFLOW.md`, `00-system/WORKFLOW.md`, and `ai/PRINCIPLES.md`.
- `00-system/README.md` updated to reference the new document.
- No existing document modified in substance.

## 3.2.0 — 2026-07-18
Prepared `07-constitutional-methodology/` to receive the Constitutional Library integration, without integrating any content or creating any new constitutional concept.

- `07-constitutional-methodology/README.md` reorganised into four named tiers — Foundational Concepts, Participant Analyses, Programme Operations, and a prepared Constitutional Library destination — covering all 20 existing documents by name for the first time; no file was moved or renamed.
- New `07-constitutional-methodology/library/` — an empty, documented destination for the Constitutional Library. Its README states explicitly that placement (subfolder versus a new top-level folder) is not yet decided, and that a new top-level folder would require a decision record before content arrives.

## 3.1.0 — 2026-07-18
Added the Constitutional Intent Inbox (`00-system/intents/`) as the first working infrastructure closing the ChatGPT → Claude Code leg of the AI Workflow's handoff problem. See decision [003](04-decisions/003-constitutional-intent-inbox.md).

- New `00-system/intents/inbox/` — fixed location and format for the human to hand ChatGPT's output to Claude Code as a single file, replacing manual retyping into a Claude Code conversation.
- `00-system/ai/CLAUDE.md` updated: Claude Code now checks the inbox at the start of every session.
- `00-system/README.md` and `00-system/AI-WORKFLOW.md` updated to reference the new mechanism. The wider Constitutional Intent model remains an unadopted proposal; only the inbox itself is adopted as working infrastructure.

## 3.0.0 — 2026-07-18
Renamed from Knowledge Operating System (KOS) to Initiative Launch System (ILS), reflecting the system's evolution from a general knowledge architecture toward launching and structuring initiatives. See decision [002](04-decisions/002-rename-to-initiative-launch-system-and-constitutional-methodology.md).

- All live references to "Knowledge Operating System" / "KOS" updated to "Initiative Launch System" / "ILS" across root standards and system documentation. Historical records — decision [001](04-decisions/001-two-repository-publication-strategy.md) and prior entries below — keep their original wording.
- New top-level folder `07-constitutional-methodology/` added: evergreen constitutional-methodology material, seeded with a `README.md` and ten skeleton concept documents (content not yet populated).
- The repository root folder name and GitHub remote name are unchanged; see [NAMING.md](NAMING.md).

## 2.0.0 — 2026-07-14
Complete redesign following architectural review.

- Root standards consolidated from nine files to seven: `GUIDE.md` and `MAP.md` merged into `README.md`; `VERSIONING.md` merged into `METADATA.md`. `STYLE.md` added as a root standard.
- `05-shared/` removed: its style guide promoted to root `STYLE.md`; its `references/` folder folded into `03-research/sources/`. Remaining folders renumbered — assets is now `05-assets/`, archive is now `06-archive/`.
- Project metadata unified onto one frontmatter schema. `metadata-template.yml` removed; `00-system/templates/project/README.md` is now the single copyable project record.
- Metadata `type` enum reduced to `project | document | decision` — file location now carries the finer distinction (concept, framework, research note) that `type` used to duplicate.
- Decision lifecycle separated from the document lifecycle (`proposed → decided`, immutable once decided — a changed position files a new, superseding decision) instead of sharing the document status list and version scale.
- Added a `on-hold` status and a `Promotion` rule (WORKFLOW.md) for moving project-scoped research, decisions, and assets to system level with a pointer left behind.
- Archiving defined as a move that preserves a project's depth in the tree, so internal relative links keep resolving.
- Added a Governance `Resolution` rule for Owner/Editor disagreement and Owner succession.
- `AI-PRINCIPLES.md` renamed to `PRINCIPLES.md`; `CLAUDE.md` and `CHATGPT.md` trimmed to agent-specific content only, deferring shared rules to `PRINCIPLES.md`.
- Template files dropped the redundant "-template" suffix; `project-template/` renamed to `project/`.

## 0.1.0 — 2026-07-14
Repository foundation created (superseded by 2.0.0).
