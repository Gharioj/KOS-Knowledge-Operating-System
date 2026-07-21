---
title: Constitutional Programme Dashboard
id: constitutional-programme-dashboard
type: document
status: draft
owner:
created: 2026-07-18
updated: 2026-07-18
version: 0.5
project:
tags: []
source:
---

# Constitutional Programme Dashboard

## Purpose

The canonical operational cockpit for the Constitutional Research Programme — the first document opened at the start of any constitutional research session, and reviewed before any [Constitutional Intent](../00-system/AI-WORKFLOW.md#constitutional-intent) begins. A snapshot, not a live view: it reflects state as of its `updated` date above, and must be revised by hand as the programme moves — see Notes.

## 1. Constitutional Programme Status

| | |
|---|---|
| **Research phase** | Phase 1 — Foundational Participant Analysis — is now complete: all four participant groups recommended by the [Roadmap](constitutional-research-roadmap.md) have been analysed (seven in total, including the original three). No Phase 2 sequence has been defined; a new roadmap or continuation decision is needed. |
| **Constitutional maturity** | Early — 0 of 10 banked questions resolved into a Constitutional Principle; all evidence still accumulating. CQ-4 now has 5 evidentiary groups, well past the resolution criteria's thresholds, pending human review. The Theme A cluster (CQ-2, CQ-6, CQ-7) has four data points across three analyses and may warrant a human-reviewed Merged decision, though this is not itself a resolution criterion. |
| **Methodology maturity** | Developing — resolution criteria and the question-state model are defined and instrumented in [Constitutional Analysis Method](constitutional-analysis-method.md), but have never been exercised through a full resolution cycle. |
| **Workflow maturity** | Partially adopted — the [Constitutional Intent Inbox](../00-system/intents/README.md) is live infrastructure (decision [003](../04-decisions/003-constitutional-intent-inbox.md)); the wider Constitutional Intent model ([AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) v2) remains an unadopted proposal. No intent to date has actually been routed through the Inbox — every one has been issued directly to Claude Code. |

## 2. Participant Analysis Progress

| Status | Participant groups |
|---|---|
| **Completed** | [Independent Labels](independent-labels.md) · [Artist Managers](managers.md) · [Producers](producers.md) · [Publishers & Catalogue Funds](publishers.md) · [Session Musicians & Sidemen](session-musicians.md) · [Booking Agents & Touring Agencies](booking-agents.md) · [Streaming Platforms & DSPs](streaming-platforms.md) |
| **In Progress** | None |
| **Planned** | None — the Research Roadmap's four recommended groups are all complete |
| **Recommended Next** | None currently defined — see §8 below |

## 3. Constitutional Questions

Full register: [Constitutional Analysis Method § Constitutional Questions Bank](constitutional-analysis-method.md#constitutional-questions-bank).

| | |
|---|---|
| **Total open** (any non-resolved state) | 10 (CQ-1–CQ-10) |
| **By state** | Open: 4 (CQ-7, CQ-8, CQ-9, CQ-10) · Accumulating Evidence: 6 (CQ-1, CQ-2, CQ-3, CQ-4, CQ-5, CQ-6) · Merged / Disconfirmed / Resolved / Out of Scope: 0 |
| **Themes** | 4 — Institutional Scaling & Shared Infrastructure (CQ-2, CQ-6, CQ-7) · Capacity-to-Capital Conversion (CQ-4) · Boundary Conditions of Recognition & Value (CQ-1, CQ-5, CQ-9) · Methodological Sufficiency (CQ-3). CQ-8 (capital-native value durability) and CQ-10 (automated execution of a Constitutional Function) remain unassigned to a theme — two unassigned questions may suggest a fifth theme is emerging, not yet named. |
| **Evidence accumulated** | 20 evidence entries, from 7 completed analyses |
| **Approaching maturity** | CQ-4 — now 5 evidentiary groups (Managers, Producers, Publishers, Booking Agents, Streaming Platforms), the strongest evidence base of any question in the bank. Not resolved: every new instance has complicated rather than sharpened the claim. The Theme A cluster (CQ-2/CQ-6/CQ-7) remains at four data points across three analyses, split across three related-but-distinct question framings rather than one. |

## 4. Constitutional Principles

| State | Questions |
|---|---|
| **Validated** (Resolved into Constitutional Principle) | None |
| **Emerging** (Accumulating Evidence) | CQ-1, CQ-2, CQ-3, CQ-4, CQ-5, CQ-6 |
| **Under Observation** (Open, 1 data point) | CQ-7, CQ-8, CQ-9, CQ-10 |

## 5. Constitutional Methodology

**Recent methodological improvements:**
- Discipline established against asserting a category from a single case, after correction on the Independent Labels analysis.
- [Constitutional Questions Bank](constitutional-analysis-method.md#constitutional-questions-bank) created, consolidating evidence across analyses.
- Constitutional Resolution state model (seven states) adopted, replacing informal question "retirement."
- First analysis of an individual, project-by-project participant type (Session Musicians & Sidemen), rather than an institution or its founder — surfacing a decoupling between compensation and recognition not visible in any institution-level analysis.
- Booking Agents & Touring Agencies analysis added evidence to three existing questions (CQ-2, CQ-4, CQ-5) without raising any new one — the first analysis in the series to do so, and a sign the bank's existing categories are broad enough to absorb a new participant type without expanding further.
- First analysis of a non-human, infrastructure-native participant type (Streaming Platforms & DSPs): the vocabulary held, but Human Capacity was found to be displaced — exercised once by designers at build time, not exercised per instance at run time — rather than absent. First Constitutional Question concerning the automated execution of a Constitutional Function (CQ-10).

**Current constitutional learning cycle:** Participant Analysis → raises or evidences Constitutional Questions → banked in Constitutional Analysis Method → Roadmap sequences the next analyses against open questions → repeat. The cycle has completed a full loop: all four Roadmap-recommended participant groups are now analysed. No further participant group is currently sequenced — see Next Recommended Constitutional Intent below.

## 6. Constitutional AI Workflow

| | |
|---|---|
| **Workflow version** | [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) Version 2 — Constitutional Intent model |
| **Governance model** | Owner decides and records structural changes in [04-decisions/](../04-decisions/README.md), per [GOVERNANCE.md](../GOVERNANCE.md); 4 decisions recorded to date |
| **Operational improvements awaiting validation** | The Constitutional Intent Inbox (decision 003) has not been used in practice — no ChatGPT-authored brief has yet been routed through it. This is the highest-leverage untested assumption in the current workflow. |

## 7. Current Constitutional Intent

**Analyse Streaming Platforms & DSPs** — completing with this commit, including this Dashboard update as part of its completion condition. This was the fourth and final participant group recommended by the Research Roadmap.

## 8. Next Recommended Constitutional Intent

**None currently defined.** The Research Roadmap's four recommended participant groups (Publishers & Catalogue Funds, Session Musicians & Sidemen, Booking Agents & Touring Agencies, Streaming Platforms & DSPs) are all now complete, alongside the original three (Independent Labels, Artist Managers, Producers) — seven analyses in total. A new roadmap, or an explicit decision on what comes next, requires human direction; this dashboard does not generate one on its own.

## 9. Constitutional Milestones

| Date | Milestone |
|---|---|
| 2026-07-18 | Repository renamed Knowledge Operating System → Initiative Launch System; Constitutional Methodology established as a core component (decision [002](../04-decisions/002-rename-to-initiative-launch-system-and-constitutional-methodology.md)) |
| 2026-07-18 | AI Workflow drafted (v1), then redesigned around Constitutional Intent (v2) |
| 2026-07-18 | Constitutional Intent Inbox adopted as first working AI Workflow infrastructure (decision [003](../04-decisions/003-constitutional-intent-inbox.md)) |
| 2026-07-18 | First three participant analyses completed: Independent Labels, Artist Managers, Producers |
| 2026-07-18 | Constitutional Questions Bank and Constitutional Resolution state model established |
| 2026-07-18 | Constitutional Research Roadmap produced |
| 2026-07-18 | Constitutional Programme Dashboard established (this document) |
| 2026-07-18 | Fourth participant analysis completed: Publishers & Catalogue Funds; CQ-4 reaches resolution criteria's evidentiary count for the first time (not yet resolved) |
| 2026-07-18 | Fifth participant analysis completed: Session Musicians & Sidemen — first test of the individual, project-by-project axis; CQ-1 reaches Accumulating Evidence; CQ-9 raised (compensation/recognition decoupling) |
| 2026-07-18 | Sixth participant analysis completed: Booking Agents & Touring Agencies — all originally planned Phase 1 participant groups now analysed; Theme A cluster reaches four data points; CQ-4 exceeds resolution thresholds for the second analysis running |
| 2026-07-18 | Seventh participant analysis completed: Streaming Platforms & DSPs — first infrastructure-native participant type; Human Capacity found displaced rather than absent; CQ-10 raised (automated execution of a Constitutional Function); all four Roadmap-recommended participant groups now complete |
| 2026-07-21 | System evolved Initiative Launch System → Initiative Lifecycle System, reflecting demonstrated support for an initiative's complete lifecycle rather than only its launch; publication pipeline (Word → GitHub → Claude Code → Markdown → GitHub Pages) and rendered-output verification recorded in workflow-protocol-v0.4.md (decisions [007](../04-decisions/007-evolve-to-initiative-lifecycle-system.md) and [008](../04-decisions/008-publication-pipeline-and-rendered-output-verification.md)) |

## Relationships

- [Constitutional Analysis Method](constitutional-analysis-method.md)
- [Constitutional Research Roadmap](constitutional-research-roadmap.md)
- [Constitutional Participant Analysis](constitutional-participant-analysis.md)
- [Independent Labels — Constitutional Participant Analysis](independent-labels.md)
- [Artist Managers — Constitutional Participant Analysis](managers.md)
- [Producers — Constitutional Participant Analysis](producers.md)
- [Publishers & Catalogue Funds — Constitutional Participant Analysis](publishers.md)
- [Session Musicians & Sidemen — Constitutional Participant Analysis](session-musicians.md)
- [Booking Agents & Touring Agencies — Constitutional Participant Analysis](booking-agents.md)
- [Streaming Platforms & DSPs — Constitutional Participant Analysis](streaming-platforms.md)
- [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md)
- [Constitutional Intent Inbox](../00-system/intents/README.md)

## Notes

This is a manually maintained snapshot, not a generated or live view — nothing in the repository currently updates it automatically, so it will drift out of date unless revised after each Constitutional Intent completes. Whether dashboard maintenance should become a mandatory step of every future intent's completion condition, or remain a separately issued intent, is not decided here — see the accompanying report.
