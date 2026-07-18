# Changelog

Structural changes to the Initiative Launch System. Content changes within projects are not logged here.

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
