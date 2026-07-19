# Changelog

Structural changes to the Initiative Launch System. Content changes within projects are not logged here.

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
