# Initiative Launch System

*(Formerly the Knowledge Operating System — renamed 2026-07-18, see [CHANGELOG.md](CHANGELOG.md) and decision [002](04-decisions/002-rename-to-initiative-launch-system-and-constitutional-methodology.md).)*

A permanent knowledge architecture — not a project, not a document archive, but the structure from which projects, research, decisions and publications emerge. Its constitutional methodology — how human capacities, functions, institutions, contribution and value are defined and related — is a core, evergreen component alongside the system's other knowledge.

## The standards
| File | Answers |
|---|---|
| [GOVERNANCE.md](GOVERNANCE.md) | Who decides? |
| [WORKFLOW.md](WORKFLOW.md) | How does work move from idea to publication? |
| [METADATA.md](METADATA.md) | What does every file carry, and how is it tagged and versioned? |
| [NAMING.md](NAMING.md) | What do we call things? |
| [STYLE.md](STYLE.md) | How do we write? |
| [CHANGELOG.md](CHANGELOG.md) | What has changed about the system itself? |

## Structure
```
00-system/       The operating machinery — AI instructions, templates
01-projects/     Individual, self-contained projects
02-knowledge/    Evergreen knowledge — concepts, frameworks, glossary
03-research/     Shared research and sources
04-decisions/    System-level decision records
05-assets/       Shared media library
06-archive/      Retired or superseded material
07-constitutional-methodology/  Constitutional methodology — human capacities, functions, institutions, contribution, value
```

## Before you create anything
1. Does it belong to one project, or does it outlive it? → `01-projects/` vs `02-knowledge/`/`03-research/`.
2. What stage is it at? → its `status`, per [WORKFLOW.md](WORKFLOW.md).
3. Is there already a template for this? → [00-system/templates/](00-system/templates/).

## AI collaborators
Instructions live in [00-system/ai/](00-system/ai/), built on the shared [PRINCIPLES.md](00-system/ai/PRINCIPLES.md).

## Principles
Knowledge before documents. Structure before content. One source of truth. Human thinking first, AI implementation second. Nothing is deleted — only archived.
