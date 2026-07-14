# Governance

## Roles
- **Owner** — sets direction, approves structural changes, final authority on publication.
- **Editor** — maintains quality and consistency, moves work through the workflow, approves most content.
- **Contributor** — adds research, drafts, and proposals.
- **AI collaborator** — implements structure and drafts under human direction; does not originate direction. See [00-system/ai/PRINCIPLES.md](00-system/ai/PRINCIPLES.md).

## Decision rights
| Change | Who decides |
|---|---|
| New top-level folder or standards change | Owner, recorded in `04-decisions/` |
| New project | Owner or Editor |
| Content within a project | Project owner (default: repository Owner) |
| Publication | Owner or designated Editor |

## Resolution
If Owner and Editor disagree, the Owner's decision stands. If no Owner is reachable, the most recent Editor holds Owner rights until one is reassigned — recorded as a decision in `04-decisions/`.

## Change control
Structural changes (anything in `00-system/`, or a new top-level folder) require a decision record before being made. Content changes within a project follow that project's own editorial process, using [WORKFLOW.md](WORKFLOW.md).

## Review cadence
The standards themselves (this file, `WORKFLOW.md`, `METADATA.md`, `NAMING.md`, `STYLE.md`) are revised when they stop fitting real use, not on a fixed schedule. Log revisions in [CHANGELOG.md](CHANGELOG.md).
