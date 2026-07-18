---
title: Rename to Initiative Launch System and Add Constitutional Methodology
id: 002-rename-to-initiative-launch-system-and-constitutional-methodology
type: decision
status: decided
owner:
created: 2026-07-18
updated: 2026-07-18
project:
tags: []
source:
---

# Decision: Rename to Initiative Launch System and Add Constitutional Methodology

## Context

The Knowledge Operating System (KOS) has evolved beyond a general-purpose knowledge architecture. Its actual use has become launching and structuring initiatives, and a body of constitutional-methodology thinking — human capacities, constitutional functions, institutions, capacity, contribution, recognised contribution, value, economics, participant analysis, and analysis method — has emerged as a core, evergreen part of how that work is done. The system's name needs to reflect what it now is, and the constitutional methodology needs a permanent home alongside the other top-level components.

## Decision

1. **The system is renamed** from Knowledge Operating System (KOS) to Initiative Launch System (ILS), throughout live documentation. Historical records that describe the system as it was at the time — decision [001](001-two-repository-publication-strategy.md), and past entries in [CHANGELOG.md](../CHANGELOG.md) — are left untouched, per the immutability rule in [WORKFLOW.md](../WORKFLOW.md). The physical repository root folder name (`Knowledge Operating System`) and the GitHub remote name are external identifiers and are out of scope for this decision; they are left as-is, consistent with the existing exception already recorded in [NAMING.md](../NAMING.md).
2. **A new top-level folder, `07-constitutional-methodology/`, is created** to hold the constitutional methodology as evergreen material, parallel in status to `02-knowledge/`. The next available numeric prefix (`07`) is used rather than reusing `02`, to preserve the sort-order guarantee described in [NAMING.md](../NAMING.md) — `00`–`06` are already assigned. It is seeded with skeleton documents only (`README.md` plus ten concept documents); content is populated later, following the normal editorial workflow in [WORKFLOW.md](../WORKFLOW.md).

## Consequences

- Every live reference to "Knowledge Operating System" / "KOS" in root standards and system documentation is updated to "Initiative Launch System" / "ILS"; historical/decision records keep their original wording.
- `07-constitutional-methodology/` becomes a core, evergreen component of the Initiative Launch System, alongside `02-knowledge/`, and is added to the root [README.md](../README.md) structure map.
- The glossary ([02-knowledge/glossary.md](../02-knowledge/glossary.md)) records both the current name (Initiative Launch System) and the retired name (Knowledge Operating System) so historical references and repository identifiers (e.g. `Gharioj/KOS-Knowledge-Operating-System`) remain interpretable.
- Future structural changes to `07-constitutional-methodology/` (new documents are ordinary content, but folder-level or standards-level changes) continue to require a decision record, per [GOVERNANCE.md](../GOVERNANCE.md).
