---
title: Single Origination Principle — No Independent Content in Public Repositories
id: 010-single-origination-principle
type: decision
status: decided
owner:
created: 2026-07-21
updated: 2026-07-21
project:
tags: []
source:
---

# Decision: Single Origination Principle — No Independent Content in Public Repositories

## Context

A methodology consistency audit conducted 2026-07-21 found governance documentation live on Project 001's public GitHub Pages site with no corresponding master anywhere in this repository — evidence that content can originate directly in a project's public repository, bypassing this repository entirely. This contradicts decision [001](001-two-repository-publication-strategy.md)'s Two-Repository Publication Strategy, which already states that a public repository is "a one-way export, not a live mirror" holding only "approved publication material," refreshed "by re-copying approved masters when they change" — but that principle was stated once, in one decision, and was not reinforced anywhere an AI collaborator or contributor would actually encounter it while working. The audit's remediation plan recommended, among other options, reinforcing this rule explicitly across the documents that govern how work is actually done. This decision implements that recommendation only — it does not backfill the specific governance content found missing, and it does not resolve that content's visibility status; both remain open, pending a separate Owner decision, and neither the From Wildfires to Regeneration repository nor its public website is touched by this decision.

## Decision

1. **Adopt the Single Origination Principle**: every file that appears in any project's public repository must trace back to an approved master committed to this repository — the Initiative Lifecycle System repository — first. A public repository never originates content; it only receives exports produced by the publication pipeline in [workflow-protocol-v0.4.md §12](../00-system/workflow-protocol-v0.4.md).
2. **`00-system/workflow-protocol-v0.4.md` §12 is amended** to state this principle explicitly, and its converse: content found in a public repository with no traceable master in this repository is a methodology inconsistency to be reported, not ordinary content to be assumed correct.
3. **`00-system/ai/CLAUDE.md`'s checklist gains an explicit instruction**: never create or edit content directly in a project's public repository, under any circumstance — including a task explicitly locked to that repository — since a public repository's only role is to receive exports.
4. **`00-system/ai/PRINCIPLES.md`'s existing "One source of truth" principle is extended** with a cross-repository clause, so it is stated as holding between repositories, not only within one.
5. **`02-knowledge/glossary.md`'s GitHub Pages entry is extended** to state the Single Origination Principle directly, alongside its existing "not a second source of truth" wording.

## Consequences

- This is a methodology reinforcement only. It does not modify the From Wildfires to Regeneration repository or its public website, and it extends, rather than supersedes, decision [001](001-two-repository-publication-strategy.md).
- It does not resolve the specific governance-content divergence the audit identified — that remains open pending a separate Owner decision on where that content's private-repository master should live and whether draft-status content may be publicly distributed at all.
- Future work touching a public repository is now bound by an explicit, checked instruction in [ai/CLAUDE.md](../00-system/ai/CLAUDE.md), not only an inference from decision 001's Consequences section.
- As with decisions 003, 004, 007, 008 and 009, this is a change within `00-system/` and is recorded here per [GOVERNANCE.md](../GOVERNANCE.md).
