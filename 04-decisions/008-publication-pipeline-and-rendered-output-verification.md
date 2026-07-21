---
title: Publication Pipeline and Rendered-Output Verification (Workflow Protocol v0.4)
id: 008-publication-pipeline-and-rendered-output-verification
type: decision
status: decided
owner:
created: 2026-07-21
updated: 2026-07-21
project:
tags: []
source:
---

# Decision: Publication Pipeline and Rendered-Output Verification (Workflow Protocol v0.4)

## Context

Project 001's From Wildfires to Regeneration reached public GitHub Pages distribution during a session working across this private repository and its public counterpart, `Gharioj/From-Wildfires-to-Regeneration`, established by decision [001](001-two-repository-publication-strategy.md)'s Two-Repository Publication Strategy. That work surfaced two operational practices not yet recorded anywhere:

1. A concrete publication pipeline — an approved Word master is committed to this repository, converted to Markdown by Claude Code, and published to the project's public repository, where GitHub Pages renders it as a public website.
2. The need to verify the rendered GitHub Pages output itself, not only the repository's Markdown source, before treating a publication task as complete — repository contents and live rendered output can diverge (a build failure, a broken relative link, or a rendering error is invisible from repository contents alone).

Neither practice contradicts `00-system/workflow-protocol-v0.3.md` (adopted by decision [006](006-operational-workflow-protocol-v0.3.md); archived by this decision to [06-archive/00-system/workflow-protocol-v0.3.md](../06-archive/00-system/workflow-protocol-v0.3.md)) or decision 001, but neither was written down.

## Decision

1. **`00-system/workflow-protocol-v0.3.md` is superseded by `00-system/workflow-protocol-v0.4.md`.** The new document carries forward every v0.3 section unchanged in substance (Prompt Completeness, Repository Lock, Repository Verification, Repository Recovery Protocol, Autonomous Execution, Human Decision Points, Repository Isolation, Batch Documentation Generation, Automatic Quality Assurance, Session Completion Reports, Continuous Improvement Process), and adds:
   - A new **§12, Publication Pipeline**, documenting the Word → GitHub → Claude Code → Markdown → GitHub Pages sequence as the mechanism that fulfils decision 001's Two-Repository Publication Strategy where a project's public repository is a browsable website.
   - An addition to **§9, Automatic Quality Assurance**: wherever a change publishes to GitHub Pages, the rendered output — the live page — is checked before the task is treated as complete, not only the repository's Markdown source.
2. **The superseded v0.3 file is archived**, not deleted, to `06-archive/00-system/workflow-protocol-v0.3.md`, per the preserve-don't-delete principle in [ai/PRINCIPLES.md](../00-system/ai/PRINCIPLES.md), following the same pattern decision [006](006-operational-workflow-protocol-v0.3.md) applied to v0.2.
3. **This extends, and does not supersede, decision [001](001-two-repository-publication-strategy.md).** The Two-Repository Publication Strategy's position is unchanged; this decision adds the concrete mechanism by which a public repository's content is produced and verified where that project publishes a website, and remains optional for a project whose public repository does not require one.

## Consequences

- `00-system/README.md` and `CHANGELOG.md` are updated to reference `workflow-protocol-v0.4.md` in place of the v0.3 file.
- Root [WORKFLOW.md](../WORKFLOW.md)'s Published stage is updated to note that a project's public repository, where one exists, renders publication material via GitHub Pages.
- [02-knowledge/glossary.md](../02-knowledge/glossary.md) gains an entry for GitHub Pages, defining it as a rendering layer, not a second source of truth.
- Future revisions to the workflow protocol follow the same pattern established by decision 006: a new version, a new decision record, the prior version archived rather than edited in place.
