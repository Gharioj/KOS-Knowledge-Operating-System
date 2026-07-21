---
title: Evolve Initiative Launch System to Initiative Lifecycle System
id: 007-evolve-to-initiative-lifecycle-system
type: decision
status: decided
owner:
created: 2026-07-21
updated: 2026-07-21
project:
tags: []
source:
---

# Decision: Evolve Initiative Launch System to Initiative Lifecycle System

## Context

Decision [002](002-rename-to-initiative-launch-system-and-constitutional-methodology.md) (2026-07-18) renamed this system from Knowledge Operating System to Initiative Launch System, because its actual use had become launching and structuring initiatives. Since then, Project 001 (From Wildfires to Regeneration) has demonstrated the system in a fuller role than "launch" describes: its methodology carried the project through drafting, decision-making and a Version 1.0 publication suite, and then — beyond initial launch — through the Word → GitHub → Claude Code → Markdown → GitHub Pages publication pipeline that keeps the project's public website current as approved masters change, and through the operational workflow protocol (`00-system/workflow-protocol-v0.3.md` at the time, now [00-system/workflow-protocol-v0.4.md](../00-system/workflow-protocol-v0.4.md) per decision [008](008-publication-pipeline-and-rendered-output-verification.md)) that governs how the system verifies, executes and improves its own work session over session. None of this is "launch" in the sense of a one-time event — it is the system operating across an initiative's complete lifecycle: design, development, governance, documentation, publication, collaboration, maintenance and continuous improvement. The name "Initiative Launch System" undersells what has actually been demonstrated in practice, and risks steering future use back toward a launch-only framing that no longer matches how the system is used.

## Decision

1. **The system's name evolves** from Initiative Launch System to Initiative Lifecycle System, throughout live documentation. The acronym ILS is unchanged — only what "L" stands for changes, from "Launch" to "Lifecycle." Historical records that describe the system as it was at the time — decisions [001](001-two-repository-publication-strategy.md)–[006](006-operational-workflow-protocol-v0.3.md), and prior [CHANGELOG.md](../CHANGELOG.md) entries — are left untouched, per the immutability rule in [WORKFLOW.md](../WORKFLOW.md), consistent with how decision 002 itself treated the Knowledge Operating System → Initiative Launch System rename.
2. **The system adopts one canonical description**, used consistently wherever it is introduced: *"a complete operating system for designing, developing, governing, documenting, publishing, collaborating on, maintaining and continuously improving initiatives."* This replaces any description that frames the system primarily around initial creation or launch.
3. **[AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md)'s description of the constitutional operating model's scope is broadened** to name the same lifecycle explicitly, rather than "researched, designed, built and recorded" alone.

## Consequences

- Every live reference to "Initiative Launch System" in root standards and system documentation is updated to "Initiative Lifecycle System"; historical and decision records keep their original wording, per the same treatment decision 002 applied to the Knowledge Operating System → Initiative Launch System rename.
- [02-knowledge/glossary.md](../02-knowledge/glossary.md) records the full naming lineage: Knowledge Operating System (KOS, retired 2026-07-18) → Initiative Launch System (ILS, 2026-07-18 to 2026-07-21) → Initiative Lifecycle System (ILS, current).
- The repository root folder name (`Knowledge Operating System`) and the GitHub remote name (`Gharioj/KOS-Knowledge-Operating-System`) remain unchanged, consistent with the exception already recorded in [NAMING.md](../NAMING.md) and left unchanged by decision 002.
- This decision does not itself adopt the publication-pipeline mechanism referenced in its Context — that mechanism is decided separately in decision [008](008-publication-pipeline-and-rendered-output-verification.md), which this decision references but does not depend on.
