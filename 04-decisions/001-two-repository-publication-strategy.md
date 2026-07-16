---
title: Two-Repository Publication Strategy
id: 001-two-repository-publication-strategy
type: decision
status: decided
owner:
created: 2026-07-16
updated: 2026-07-16
project:
tags: []
source:
---

# Decision: Two-Repository Publication Strategy

## Context

The Knowledge Operating System (KOS) repository is the private engine of this system: it holds every project in full, with its complete internal structure — research, drafts, decisions, publication, assets — plus the system's own governance, workflow, metadata, and naming standards. When Project 001 reached Version 1.0 and needed external distribution, sharing the KOS repository directly would have exposed internal architecture, operating procedures, and decision logs to external stakeholders who have no need to see them.

## Decision

Repositories are organised on two tiers:

1. **The KOS repository stays private** and remains the sole engine of the system — every project lives here in full, regardless of its distribution status. This is where all work happens.
2. **Each project that reaches external-distribution status receives its own standalone public repository**, created only at that point, not proactively for every project. A project's public repository contains only its approved publication material — a project-facing `README.md` and the finished documents themselves — with no KOS internals: no workflow documents, no governance, no metadata standards, no naming conventions, no decision logs, no AI operating instructions.

## Consequences

- Operating infrastructure and public-facing output are cleanly separated: external stakeholders see only finished, approved material, never the machinery or the decision history behind it.
- The KOS repository can scale to hundreds of projects without a corresponding sprawl of public repositories — a public repository is created only on demand, when a project actually needs one.
- A project's public repository is a one-way export, not a live mirror: the KOS repository's publication folder for that project remains the authoritative source, and the public repository is refreshed by re-copying approved masters when they change.
- This pattern is established precedent, demonstrated by Project 001: `Gharioj/KOS-Knowledge-Operating-System` (private) and `Gharioj/From-Wildfires-to-Regeneration` (public).
