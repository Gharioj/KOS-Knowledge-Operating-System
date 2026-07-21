---
title: Physical Repository Identity Migration — Local Folder and GitHub Repository Rename
id: 011-physical-repository-identity-migration
type: decision
status: decided
owner:
created: 2026-07-21
updated: 2026-07-21
project:
tags: []
source:
---

# Decision: Physical Repository Identity Migration — Local Folder and GitHub Repository Rename

## Context

Decisions [002](002-rename-to-initiative-launch-system-and-constitutional-methodology.md) and [007](007-evolve-to-initiative-lifecycle-system.md) each deliberately left the physical repository root folder name (`Knowledge Operating System`) and the GitHub remote name (`Gharioj/KOS-Knowledge-Operating-System`) unchanged, treating them as external identifiers out of scope for a documentation-only rename, per the exception previously recorded in [NAMING.md](../NAMING.md). Following completion of the Initiative Lifecycle System documentation migration (decisions 007–010), the Owner has explicitly directed that this exception be lifted, so that the physical identity is brought into alignment with the documented name rather than continuing to name the system's original identity indefinitely.

## Decision

1. **The local repository root folder is renamed** from `Knowledge Operating System` to `Initiative Lifecycle System`, preserving its existing full-words-with-spaces style rather than adopting the hyphenated convention the GitHub remote name uses.
2. **The GitHub remote repository `Gharioj/KOS-Knowledge-Operating-System` should be renamed** to `Gharioj/ILS-Initiative-Lifecycle-System`, following the existing ACRONYM-Full-Name convention the remote already uses. This step cannot be performed from the environment this decision was made in — it has no GitHub API or `gh` CLI access — and remains a manual action for the Owner; see the accompanying completion report for the exact manual steps.
3. **The exception previously recorded in [NAMING.md](../NAMING.md) is retired.** The folder-naming convention (`lowercase-kebab-case` for ordinary content, `UPPERCASE.md` for root standards) still does not apply to the repository root folder itself, by deliberate choice — the folder mirrors the system's own full name rather than ordinary file naming — but the folder no longer names a retired identity.
4. **Live text that described the physical folder or remote as "unchanged"** — `NAMING.md`, `02-knowledge/glossary.md` — is updated to reflect this migration. Decisions 002 and 007 are not edited; they remain accurate records of what was decided at the time, and this decision supersedes only their "left as-is" position on physical identifiers, not their substance.

## Consequences

- The local clone's root folder is renamed as part of fulfilling this decision, in the same session that decided it. Git itself is unaffected — a repository's identity lives in `.git/`, not the enclosing folder's name — so this rename does not require any git operation of its own.
- The GitHub remote rename is a manual step outside this environment's reach. Until it is performed, `git remote -v` continues to show the prior URL. GitHub redirects a renamed repository's old URL for git operations automatically, so existing clones (including this one, until updated) continue to work once the manual rename happens.
- Once the manual GitHub rename is complete, a follow-up session should run `git remote set-url origin https://github.com/Gharioj/ILS-Initiative-Lifecycle-System.git` to point the local remote at the canonical new URL, rather than relying on GitHub's redirect indefinitely.
- Any future task's stated "Expected Local Path" for this repository should be updated to `Initiative Lifecycle System`, not `Knowledge Operating System` or `KOS-Knowledge-Operating-System` — a Repository Verification step (per [workflow-protocol-v0.4.md §3](../00-system/workflow-protocol-v0.4.md)) run against the old path will now correctly fail and should be treated as an outdated prompt, not a locked repository, per §1 Prompt Completeness.
- As with decisions 007–010, this is a change within `00-system/` scope (repository identity) and is recorded here per [GOVERNANCE.md](../GOVERNANCE.md).
