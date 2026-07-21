# AI Workflow — Constitutional Operating Model

*Version 2 — first-principles redesign. Supersedes the Version 1 draft (commit `b50717c`). Replaces the term "Constitutional Directive" with "Constitutional Intent": a directive specifies workflow; an intent specifies the desired constitutional outcome and leaves implementation to the AI ecosystem. Not yet implemented, not yet linked from other documents, not yet a decision. Awaiting approval.*

This is not documentation of a process. It is Project Zero: the operating architecture through which every initiative in the Initiative Lifecycle System is designed, developed, governed, documented, published, collaborated on, maintained and continuously improved across its complete lifecycle — not only researched, designed, built and recorded at launch — so that human creative capacity is spent on discovery, reflection, judgment and decision, and on nothing else.

## Constitutional Objective

Maximise human creative capacity by minimising AI orchestration. The human is removed from implementation as far as possible and remains only for discovery, reflection, judgment and decision-making. Everything else — research assembly, drafting, editing, committing, cross-referencing, record-keeping — is constitutional infrastructure, not something the human does or routes by hand.

## Constitutional Principle: Orchestration Belongs to the System, Not the Human

> The human should disappear from orchestration, not from authorship.

The human remains responsible for:
- Discovery
- Reflection
- Judgment
- Constitutional Intent

The AI ecosystem becomes responsible for:
- Planning
- Orchestration
- Implementation
- Documentation
- Repository management
- Editorial workflow

Constitutional Intent is the highest layer of this operating model — the only layer the human interacts with directly. Everything beneath it is free to change, be replaced, or be automated further without changing the human's way of working: issue an intent, exercise judgment at its one checkpoint. Nothing beneath that layer is contractually visible to the human.

## Why Version 1 Does Not Meet This Objective

Version 1 named the right systems and the right responsibilities, but it left the human performing three jobs the objective forbids:

1. **The human was the message bus.** Every brief moved from ChatGPT to Claude Code by being retyped or pasted by a person. The workflow called this a "structured handoff," but structuring the artifact does not remove the human from carrying it.
2. **Approval was granted per artifact, not per judgment.** Each document required an explicit "approved, continue" before the next began. That is repetitive prompting by another name — the human was asked to make the same low-stakes decision, over and over, rather than one real decision at the point it actually mattered.
3. **There was no repeatable unit of work.** "One discovery → one document → one commit" was a convention the human had to keep re-asserting each turn, not a structure the system enforced on its own. Every session re-invented its own granularity.

Version 1 described roles. It did not remove orchestration from the human — it just gave the human's orchestration better labels. Version 2 replaces the unit of interaction itself, and this refinement corrects a residual error in that replacement: a *directive* still specifies workflow, which quietly puts the human back in the business of designing sequence. An *intent* does not.

## Constitutional Intent

The prompt is not the unit of work. The Constitutional Intent is.

A Constitutional Intent is a named, desired constitutional outcome, issued as a single instruction from the human. It does not specify workflow, roles or sequence — those are Planning, an AI-ecosystem responsibility. What it fixes is the outcome sought and, at most, one point where human judgment is required. Issuing an intent replaces what would otherwise be a chain of prompts and a chain of approvals with one instruction and, at most, one checkpoint.

### Anatomy of a Constitutional Intent

| Element | Description |
|---|---|
| **Name** | A short constitutional verb phrase — e.g. "Promote Constitutional Capacity." What the human actually says. |
| **Desired Outcome** | The constitutional state that should exist once the intent is fulfilled — not a description of steps. |
| **AI Ecosystem Response** | Determined by the ecosystem's own planning, not prescribed by the human — typically some combination of research, drafting, implementation and repository management, chosen to fit the intent. |
| **Human Checkpoint** | The single point, if any, where judgment is required — never more than one per intent. |
| **Completion Condition** | What must be true in the GitHub repository for the intent to count as fulfilled. |

An intent that requires the human to specify sequence, assign roles, or decide mid-execution has collapsed back into a directive — a sign it was issued at the wrong altitude, not a normal feature of the model. The checkpoint belongs at the start (issuing the intent) or the end (reviewing the outcome), never scattered through the middle, and never in specifying how.

### Constitutional Intent Registry (illustrative)

| Constitutional Intent | Desired Outcome | Human Checkpoint |
|---|---|---|
| **Promote Constitutional Capacity** | A Human Capacity being exercised but not yet recognised becomes formally recognised in the constitutional record. | Review the recognition case, or the committed result — not both. |
| **Promote Constitutional Contribution** | An exercised but unrecorded Contribution becomes Recognised Contribution. | Same as above. |
| **Analyse Independent Labels** | A constitutional participant analysis of this group exists in the repository. | Review the finished analysis. |
| **Refine Constitutional Economics** | The existing definition is developed and improved. | Review the revision as a single diff. |
| **Bank Discovery** | A raw discovery or insight is captured to the repository before it can be lost. | None — capture is never gated on approval. |
| **Prepare Editorial Review** | A single packet summarising all pending changes and open questions exists, ready for one review pass. | Review the packet. |

This registry is illustrative, not exhaustive; new intents are named as recurring constitutional outcomes are recognised. In every case, *how* the outcome is reached — which system researches, drafts, implements or commits, in what order — is Planning, not something the registry or the human prescribes. The registry names outcomes and checkpoints; it does not name steps.

## Roles Under the Constitutional Intent Model

### ChatGPT — Constitutional Thinking, Research, Architectural Design
Contributes the constitutional thinking, research and architectural design an intent's outcome depends on, and participates in Planning how that outcome is reached. Its output is substance for the ecosystem's plan, not a fixed brief dictating Claude Code's steps.

### Claude Code — Orchestration, Implementation, Documentation, Repository Management, Editorial Workflow
Plans and executes what an intent requires — implementation, documentation, committing, pushing, and assembling editorial review packets — without pausing mid-execution for approval. Pauses only at the intent's one defined checkpoint. Implements constitutional direction; does not originate it, per [ai/PRINCIPLES.md](ai/PRINCIPLES.md).

### GitHub — Canonical Constitutional Knowledge Base
The only state that counts as *done*. An intent is not fulfilled until its output is committed. Both AI systems act against this one shared state rather than private, diverging context — this is what makes an intent portable between sessions and between systems.

### Human — Discovery, Reflection, Judgment, Constitutional Intent
Issues intents. Sits at the one checkpoint each intent defines. Is not consulted on planning, sequence or roles — those belong to the ecosystem — and does not carry content between systems by hand where that can be avoided.

## The Handoff Problem

ChatGPT and Claude Code have no live connection to each other. The ChatGPT → Claude Code leg is addressed by the [Constitutional Intent Inbox](intents/README.md), adopted by decision [003](../04-decisions/003-constitutional-intent-inbox.md): the human saves ChatGPT's output as one file, in a fixed format, at `00-system/intents/inbox/`, and Claude Code reads it directly at the start of a session — no retyping, no pasting into a Claude Code conversation. This is a first working version of the mechanism, not a final one.

The Claude Code → ChatGPT leg remains open: ChatGPT has no automatic visibility into repository state, so the human still carries context back to it by hand. Closing this — a repository connector for ChatGPT, or a direct API-based integration — was raised as a genuine constitutional decision, since it involves external configuration, credentials or cost only the human can authorise, and could change whether ChatGPT remains a distinct participant in this workflow at all. **Decided 2026-07-18: left manual for now.** No connector or integration is being built; this is revisited once the Intent Inbox has been used in practice and its actual friction is known, rather than designed against a guess.

## Reducing Approval to Genuine Judgment

A checkpoint is genuine when it involves a new direction, a structural or constitutional position, or a judgment call the system cannot resolve on its own. It is not genuine when it merely confirms that an already-issued intent was fulfilled as planned — that is verification, and verification is Claude Code's job, not a reason to interrupt the human. This does not relax [GOVERNANCE.md](../GOVERNANCE.md): structural changes and new top-level folders still require a decision record. What changes is that routine fulfilment of an intent is no longer treated as if it carried the same weight.

## Constitutional Status of This Document

The Constitutional Intent model described here is Version 2 of a proposal, not yet formally adopted as a whole. Per [GOVERNANCE.md](../GOVERNANCE.md), adopting it — and any later change to it — requires a decision record, since it is a change within `00-system/`. No intent in the registry above has been executed; the registry describes the target model, not current practice.

One piece is live infrastructure, not just proposal: the [Constitutional Intent Inbox](intents/README.md), adopted by decision [003](../04-decisions/003-constitutional-intent-inbox.md), which closes the ChatGPT → Claude Code leg of [the handoff problem](#the-handoff-problem). Its adoption does not constitute adoption of the wider model.

## Notes

Refinement continues in a future session: sharpening how ChatGPT's output reaches Claude Code without human retyping, deciding which intents are core versus initiative-specific, and specifying how the human-carried handoff step is eventually retired rather than merely shortened.
