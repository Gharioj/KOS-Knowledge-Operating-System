# Constitutional Memory — Constitutional Specification

*This is a constitutional specification, not an implementation plan. No technology, platform, storage mechanism, or vendor is specified, implied, or recommended anywhere in this document. It defines what Constitutional Memory would be and how it would relate to the system's existing participants, so that a future, separate decision can be made about whether and how to build it. Not yet adopted. Awaiting human review.*

## Constitutional Purpose

This system currently has no single, accountable answer to "what does this system remember, where does that memory live, who may change it, and how does it stay consistent across every participant that relies on it?" The answer today is implicit and scattered: [AI-WORKFLOW.md](AI-WORKFLOW.md) states that GitHub is the sole canonical record and that conversation history is working memory, not the record — but nothing specifies what counts as memory versus working context, how a derived summary like the [Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) relates to the canonical sources it summarises, or how a participant that cannot read the repository directly — ChatGPT, today — is meant to know what the system currently believes.

Constitutional Memory's purpose is to give this system a defined, accountable participant responsible for that question, on the same footing as the human, ChatGPT, Claude Code and GitHub already have in [AI-WORKFLOW.md](AI-WORKFLOW.md#roles-under-the-constitutional-intent-model) — not to build anything, but to specify what such a participant would need to be true of it before anything is built.

## Constitutional Functions

- **Persistence** — ensuring constitutional state (decisions, Constitutional Questions, Constitutional Principles, dashboard summaries) survives beyond any single session or conversation, rather than existing only in whichever participant last held it in working context.
- **Retrieval** — making current, accurate state available to whichever participant needs it, at the point they need it, without requiring the human to manually reconstruct or re-explain it each time.
- **Synchronisation** — keeping every participant's view of state consistent with the canonical record, closing the gap [AI-WORKFLOW.md](AI-WORKFLOW.md#the-handoff-problem) already named as unsolved for ChatGPT specifically.
- **Provenance** — preserving the record of how memory changed: what changed, when, and through which act — the same append-only, nothing-deleted discipline already practised by the [Constitutional Questions Bank](../07-constitutional-methodology/constitutional-analysis-method.md#constitutional-questions-bank), generalised to memory as a whole.
- **Boundary-setting** — distinguishing what is memory (durable, accountable, part of the constitutional record) from what is not (ephemeral working context, draft reasoning, a single conversation's scratch space) — a distinction [AI-WORKFLOW.md](AI-WORKFLOW.md) asserts in principle but has not yet had to specify precisely, because no participant besides GitHub has needed to rely on it directly.

## Relationships

**To the Human.** Constitutional Memory exists to remove the human from being the thing that remembers and manually re-supplies context between participants — the same objective [AI-WORKFLOW.md](AI-WORKFLOW.md#constitutional-principle-orchestration-belongs-to-the-system-not-the-human) already states for orchestration generally. The human should be able to trust that memory is accurate without personally verifying or re-carrying it, while remaining the party who resolves what memory disagrees about or cannot resolve on its own.

**To ChatGPT.** ChatGPT today has no access to this system's canonical state at all, beyond what the human pastes into it. Constitutional Memory would need to define what read access to canonical state means for a participant that cannot directly read the repository — without this document choosing, recommending, or assuming any particular mechanism for providing it.

**To Claude Code.** Claude Code already reconstructs memory by reading files at the start of a session — the [Constitutional Intent Inbox](intents/README.md) and the [Constitutional Programme Dashboard](../07-constitutional-methodology/constitutional-programme-dashboard.md) are both, in effect, informal instances of this already happening. Constitutional Memory would formalise this as the specification Claude Code's session-start behaviour already follows in practice: Claude Code has no private memory of its own; everything it treats as known must trace back to something actually written in the repository.

**To GitHub.** GitHub is already established as the sole canonical record. Constitutional Memory's relationship to GitHub is not competitive but definitional: GitHub is where Constitutional Memory would physically live; Constitutional Memory is the specification of how that record is structured, written to, read from, and kept trustworthy — the rules, not a second repository.

## Governance

Constitutional Memory does not introduce a new governance system. It inherits [GOVERNANCE.md](../GOVERNANCE.md) and the resolution discipline already established in [Constitutional Analysis Method](../07-constitutional-methodology/constitutional-analysis-method.md) in full: structural changes to memory require a decision record; nothing is resolved or deleted by an automatic process; the Owner remains the final authority on what memory is permitted to assert as settled. A separate governance layer for memory specifically would duplicate, and risk contradicting, rules this system already has.

## Synchronisation Principles

- **Single source of truth.** GitHub remains canonical. Any other participant's held state — ChatGPT's own memory of a prior conversation, Claude Code's context within a session — is a cache or a derivative, never authoritative, and defers to GitHub whenever the two disagree.
- **Freshness over convenience.** A participant should prefer re-reading canonical state over relying on its own possibly-stale recollection, particularly at the start of a session or a new conversation — the practice [ai/CLAUDE.md](ai/CLAUDE.md) already requires of Claude Code for the Inbox and the Dashboard, generalised as a principle rather than left as two specific checklist items.
- **Explicit staleness.** Any derived or summarising memory — the Dashboard is the existing example — must state plainly that it is a snapshot, not a live view, and must be revised deliberately rather than assumed current.
- **No silent divergence.** If a participant's held state and the canonical record disagree, that disagreement should be surfaced, not silently resolved in favour of whichever the participant happens to trust more.
- **Minimal duplication.** Each fact should have one home. Derived summaries should point back to their source rather than becoming a second, independently maintained copy of the same truth.

## Constitutional Constraints

- Constitutional Memory must never become a second canonical source competing with GitHub.
- Constitutional Memory must never silently overwrite or delete prior state — a correction is a visible act, not a quiet edit, matching the Constitutional Questions Bank's existing discipline.
- Constitutional Memory must never substitute for human judgment. It may inform a decision; it may not stand in for the accountable act — resolution, a decision record — that this system already requires a human to take.
- Constitutional Memory must not require the human to be its synchronisation mechanism indefinitely. That is the condition it exists to change, not a constraint it is permitted to reproduce under a different name.

## Open Constitutional Questions

These are raised, not resolved, and are not yet assigned into the [Constitutional Questions Bank](../07-constitutional-methodology/constitutional-analysis-method.md#constitutional-questions-bank) — whether they belong there, in a separate registry for AI-workflow infrastructure, or somewhere not yet specified is itself the first open question below.

1. **Does Constitutional Memory belong in the same Questions Bank as the creative-ecosystem participant analyses, or does AI-workflow infrastructure need its own, separate track?** The existing bank was built around evidence from participant analyses (labels, managers, producers, and so on); Constitutional Memory's evidence, if any accumulates, would come from operating this system itself, not from researching external institutions.
2. **Is the Constitutional Programme Dashboard already an early, informal instance of Constitutional Memory, and should it eventually be reclassified or absorbed into whatever this specification becomes, rather than continuing to exist as a separate document?**
3. **How should a disagreement between ChatGPT's own memory of a prior conversation and GitHub's canonical record actually be detected**, given that this document deliberately does not specify any mechanism by which ChatGPT would compare the two?
4. **Does Constitutional Memory need its own resolution or maturity discipline, analogous to the Constitutional Question states**, or does it simply inherit [GOVERNANCE.md](../GOVERNANCE.md) wholesale, with no additional apparatus of its own?
5. **At what point does this specification stop being a specification and require an actual decision record and build** — the same threshold the [Constitutional Intent Inbox](intents/README.md) crossed when it moved from proposal to live infrastructure — and who decides that threshold has been reached?
