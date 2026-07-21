# Editorial Workflow

## Stages (documents and projects)
1. **Capture** — an idea or question is recorded, before any project folder exists.
2. **Research** — supporting material is gathered, in a project's `01-research/` or shared [03-research/](03-research/README.md).
3. **Draft** — written, in a project's `02-drafts/`. *Review* is a status within this stage, not a separate folder.
4. **Published** — finished work moves to a project's `04-publication/`. Where a project has reached external-distribution status, its public repository (decision [001](04-decisions/001-two-repository-publication-strategy.md)) may render that material as a public website via GitHub Pages — see [00-system/workflow-protocol-v0.4.md §12](00-system/workflow-protocol-v0.4.md).
5. **On-hold** — paused at any stage; resume by restoring the appropriate status.
6. **Archived** — superseded or retired, moved to [06-archive/](06-archive/README.md), never deleted.

A project's folders (`01-research` … `05-assets`) group work for browsing, not a strict sequential gate — a decision may be filed before any draft exists.

## Decisions
Decisions follow a separate, shorter lifecycle: `proposed → decided → (archived if superseded)`. A decision is immutable once decided — a changed position is filed as a new decision that references and supersedes the old one, kept side by side so the history of reasoning stays visible.

System-level decisions live in [04-decisions/](04-decisions/README.md); project-level decisions live in each project's own `03-decisions/`.

## Promotion
Research, decisions, and assets created inside a project sometimes prove useful beyond it. When that happens, they are promoted: moved to the matching system-level folder (`03-research/`, `04-decisions/`, `05-assets/`), leaving a one-line pointer in the project's own folder. The system-level copy becomes the source of truth — the project keeps a reference, never a duplicate.

## Principle
A file's location signals its stage. Moving it between folders is how it advances; status metadata and physical location should always agree.
