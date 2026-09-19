# Guardrails & Governance

*The chapter most AI-adoption stories skip — and the one that decides whether the whole thing survives contact with reality.*

Giving an AI agent real autonomy inside a company is a governance problem before it's a technology problem. These are the rules my system runs under. Most were written after something went wrong; all are enforced, not aspirational.

## 1. Identity rules

The agent acts only under its own identity — its own bot account, its own name on every message and document. It is technically possible for it to act under a human's credentials; it is absolutely forbidden. One early incident (messages sent under a human's account) produced the hard rule, an owned apology, and a permanent check before every send.

**Principle: an AI teammate must be visible as one. Impersonation, even accidental and well-meant, destroys the trust the whole system depends on.**

## 2. Channel firewall

The agent sees many conversations — private DMs, team groups, cross-functional channels. Content never crosses between them: a private discussion is never referenced in a group, one team's context never leaks into another's channel, and every outbound message is checked against the target channel's scope. When content straddles a line, the agent asks where it belongs instead of guessing.

## 3. Approval gates by irreversibility

Autonomy is scoped by how reversible an action is:

| Action class | Policy |
|-------------|--------|
| Reading, triaging, drafting, internal reports | Autonomous |
| Publishing, posting, sending to external parties | Per-item human approval |
| Deleting data, spending money, anything irreversible | Explicit confirmation, always, no standing permission |

"Approval in one context doesn't extend to the next" is a literal rule — approving Tuesday's post is not approving Wednesday's.

## 4. Information-classification checks on every send

Before anything leaves the system, a checklist runs: does this contain internal metrics in an external channel? Internal document links to unapproved audiences? Draft-status content presented as final? Sharing a document *link* is treated as sharing the document — a lesson from a real incident where a well-meant "here's context for the new colleague" shared far more than intended.

## 5. Credential hygiene

Secrets live in environment files, never in messages, documents, logs, or commits. Logged-in browser sessions are used only for explicitly requested actions — never navigating to account settings or financial pages unprompted.

## 6. The incident → rule pipeline

Every failure produces two written artifacts: the specific fix, and the *generalized principle* stored where the agent loads it every session. The rulebook is versioned, dated, and cites its incidents — an audit trail of the system getting safer.

---

## The takeaway for marketing leaders

Your first AI-agent deployment will fail in governance before it fails in capability. Budget your design effort accordingly: roughly half of what makes this system production-grade is the rules above, not the automation. The good news — unlike human process documents, an agent actually reads its rulebook, every session, and enforces it on itself.
