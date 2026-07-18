---
title: Constitutional Programme Dashboard
id: constitutional-programme-dashboard
type: document
status: draft
owner:
created: 2026-07-18
updated: 2026-07-18
version: 0.4
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
| **Research phase** | Phase 1 — Foundational Participant Analysis: establishing the method and the Constitutional Questions Bank. Phase 2 candidates are defined in the [Roadmap](constitutional-research-roadmap.md) but not yet started. |
| **Constitutional maturity** | Early — 0 of 9 banked questions resolved into a Constitutional Principle; all evidence still accumulating. CQ-4 exceeds the resolution criteria's count and cross-type thresholds (4 groups), pending human review. The Theme A cluster (CQ-2, CQ-6, CQ-7) now has four data points across three analyses and may warrant a human-reviewed Merged decision, though this is not itself a resolution criterion. |
| **Methodology maturity** | Developing — resolution criteria and the question-state model are defined and instrumented in [Constitutional Analysis Method](constitutional-analysis-method.md), but have never been exercised through a full resolution cycle. |
| **Workflow maturity** | Partially adopted — the [Constitutional Intent Inbox](../00-system/intents/README.md) is live infrastructure (decision [003](../04-decisions/003-constitutional-intent-inbox.md)); the wider Constitutional Intent model ([AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) v2) remains an unadopted proposal. No intent to date has actually been routed through the Inbox — every one has been issued directly to Claude Code. |

## 2. Participant Analysis Progress

| Status | Participant groups |
|---|---|
| **Completed** | [Independent Labels](independent-labels.md) · [Artist Managers](managers.md) · [Producers](producers.md) · [Publishers & Catalogue Funds](publishers.md) · [Session Musicians & Sidemen](session-musicians.md) · [Booking Agents & Touring Agencies](booking-agents.md) |
| **In Progress** | None |
| **Planned** (recommended order, per [Roadmap](constitutional-research-roadmap.md)) | Streaming Platforms & DSPs |
| **Recommended Next** | Streaming Platforms & DSPs |

## 3. Constitutional Questions

Full register: [Constitutional Analysis Method § Constitutional Questions Bank](constitutional-analysis-method.md#constitutional-questions-bank).

| | |
|---|---|
| **Total open** (any non-resolved state) | 9 (CQ-1–CQ-9) |
| **By state** | Open: 3 (CQ-7, CQ-8, CQ-9) · Accumulating Evidence: 6 (CQ-1, CQ-2, CQ-3, CQ-4, CQ-5, CQ-6) · Merged / Disconfirmed / Resolved / Out of Scope: 0 |
| **Themes** | 4 — Institutional Scaling & Shared Infrastructure (CQ-2, CQ-6, CQ-7) · Capacity-to-Capital Conversion (CQ-4) · Boundary Conditions of Recognition & Value (CQ-1, CQ-5, CQ-9) · Methodological Sufficiency (CQ-3). CQ-8 (capital-native value durability) remains unassigned to a theme. |
| **Evidence accumulated** | 18 evidence entries, from 6 completed analyses |
| **Approaching maturity** | CQ-4 — exceeds the resolution criteria's count and cross-type thresholds (4 groups: Managers, Producers, Publishers, Booking Agents). Not resolved: every new instance has complicated rather than sharpened the claim. The Theme A cluster (CQ-2/CQ-6/CQ-7) now has four data points across three analyses (Secretly Group, Red Light Management, Max Martin's lineage, CAA) — the largest combined evidence base in the bank, though split across three related-but-distinct question framings rather than one. |

## 4. Constitutional Principles

| State | Questions |
|---|---|
| **Validated** (Resolved into Constitutional Principle) | None |
| **Emerging** (Accumulating Evidence) | CQ-1, CQ-2, CQ-3, CQ-4, CQ-5, CQ-6 |
| **Under Observation** (Open, 1 data point) | CQ-7, CQ-8, CQ-9 |

## 5. Constitutional Methodology

**Recent methodological improvements:**
- Discipline established against asserting a category from a single case, after correction on the Independent Labels analysis.
- [Constitutional Questions Bank](constitutional-analysis-method.md#constitutional-questions-bank) created, consolidating evidence across analyses.
- Constitutional Resolution state model (seven states) adopted, replacing informal question "retirement."
- First analysis of an individual, project-by-project participant type (Session Musicians & Sidemen), rather than an institution or its founder — surfacing a decoupling between compensation and recognition not visible in any institution-level analysis.
- Booking Agents & Touring Agencies analysis added evidence to three existing questions (CQ-2, CQ-4, CQ-5) without raising any new one — the first analysis in the series to do so, and a sign the bank's existing categories are broad enough to absorb a new participant type without expanding further.

**Current constitutional learning cycle:** Participant Analysis → raises or evidences Constitutional Questions → banked in Constitutional Analysis Method → Roadmap sequences the next analyses against open questions → repeat. Currently between cycles: Booking Agents & Touring Agencies is complete, the Theme A cluster is at its strongest evidence base yet (pending a human-reviewed Merged decision), and Streaming Platforms & DSPs — the Roadmap's highest-risk, most speculative candidate — is recommended next and last of the originally planned four.

## 6. Constitutional AI Workflow

| | |
|---|---|
| **Workflow version** | [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md) Version 2 — Constitutional Intent model |
| **Governance model** | Owner decides and records structural changes in [04-decisions/](../04-decisions/README.md), per [GOVERNANCE.md](../GOVERNANCE.md); 4 decisions recorded to date |
| **Operational improvements awaiting validation** | The Constitutional Intent Inbox (decision 003) has not been used in practice — no ChatGPT-authored brief has yet been routed through it. This is the highest-leverage untested assumption in the current workflow. |

## 7. Current Constitutional Intent

**Analyse Booking Agents & Touring Agencies** — completing with this commit, including this Dashboard update as part of its completion condition.

## 8. Next Recommended Constitutional Intent

**Analyse Streaming Platforms & DSPs** — per the [Constitutional Research Roadmap](constitutional-research-roadmap.md#recommended-sequence), the fourth-ranked and final originally planned participant group — the first candidate whose fit with the methodology's core vocabulary (Human Capacities, Constitutional Functions) is itself in question.

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
- [AI-WORKFLOW.md](../00-system/AI-WORKFLOW.md)
- [Constitutional Intent Inbox](../00-system/intents/README.md)

## Notes

This is a manually maintained snapshot, not a generated or live view — nothing in the repository currently updates it automatically, so it will drift out of date unless revised after each Constitutional Intent completes. Whether dashboard maintenance should become a mandatory step of every future intent's completion condition, or remain a separately issued intent, is not decided here — see the accompanying report.
