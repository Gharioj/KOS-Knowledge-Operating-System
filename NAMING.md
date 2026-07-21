# Naming Conventions

## Files and folders
- `lowercase-kebab-case` for everything except the root standards docs and AI instruction files, which use `UPPERCASE.md` to signal "operating rule, read first" — see the list in [README.md](README.md).
- No spaces, no underscores.
- Template files drop the word "template" when the parent folder already says so (`templates/document.md`, not `templates/document-template.md`).

## Numeric prefixes
Top-level folders use two-digit prefixes (`00`–`06`) to fix sort order. Numbering signals function, not importance or chronology.

## IDs
- Projects: `NNN-slug`, three digits, sequential, assigned once and never reused — even if archived.
- Decisions: `NNN-slug`, three digits, sequential — but scoped to where the decision lives. System decisions in `04-decisions/` share one sequence; each project's own `03-decisions/` runs its own sequence starting at 001. The folder path disambiguates them, so both use the same three-digit format.

## Dates
ISO 8601 (`YYYY-MM-DD`) everywhere.

## Exception
The repository root folder name (`Knowledge Operating System`) predates this convention — and predates the system's evolution, first to Initiative Launch System, now to Initiative Lifecycle System (ILS) — and is left as-is. See decisions [002](04-decisions/002-rename-to-initiative-launch-system-and-constitutional-methodology.md) and [007](04-decisions/007-evolve-to-initiative-lifecycle-system.md).
