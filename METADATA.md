# Metadata Standard

Every substantive file opens with YAML frontmatter.

## Fields
```yaml
---
title:
id:
type:            # project | document | decision
status:
owner:
created:         # YYYY-MM-DD
updated:         # YYYY-MM-DD
version:
project:         # project id, if applicable — omit for system-level files
tags: []
source:          # originating source or reference, if applicable
---
```

## Status
Documents and projects share one lifecycle: `capture → research → draft → review → published`, plus `on-hold` (paused at any stage) and `archived` (terminal — see [WORKFLOW.md](WORKFLOW.md)).

Decisions have their own, shorter lifecycle: `proposed → decided`, then `archived` if superseded.

`status` must always match the file's physical location.

## Type
`type` is deliberately minimal. Where something lives already signals what kind of thing it is — a file in `02-knowledge/concepts/` is a concept, one in `03-research/notes/` is a research note. `type` doesn't repeat that signal; it only distinguishes the three structurally different kinds of file: `project`, `document`, and `decision`.

## Versioning
- `0.x` — draft, pre-publication. Increment freely.
- `1.0` — first published version.
- `1.x` — minor revision after publication.
- `2.0` — a substantive rewrite or change in position.
- Decisions do not use this scale — a decision is immutable once decided; a changed position is filed as a new decision that supersedes the old one (see [WORKFLOW.md](WORKFLOW.md)).

## Tags
Tags must already appear in [02-knowledge/glossary.md](02-knowledge/glossary.md) before use — this keeps vocabulary controlled without needing separate tooling.
