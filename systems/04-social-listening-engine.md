# System 4 — The Social Listening & Engagement Engine

*Most social listening produces dashboards. This one produces drafted responses with an approval queue.*

## The loop

```
scheduled scan ──► signal triage ──► FLAG / ENGAGE / MONITOR ──► drafted response ──► human approve ──► post
```

**Scan.** On a fixed cadence the agent sweeps configured surfaces — industry communities, relevant hashtags and keywords, competitor mentions, partner activity — through official APIs and logged-in sessions it operates under strict rules (see [guardrails](../guardrails.md)).

**Triage.** Every signal gets one of three labels:

- **FLAG** — needs a human decision (a competitor move, a complaint, a journalist asking questions). Routed to the right owner immediately, never auto-answered.
- **ENGAGE** — a comment/reply opportunity worth taking. The agent drafts the response *in the account's voice*, attaches the context, and queues it for approval.
- **MONITOR** — worth tracking, not worth acting on. Logged with a reason, so patterns surface over weeks.

**Approve → post.** Approved items post through an auto-poster that only ever executes explicitly approved drafts — approval is per-item, by ID, in writing. Batch approval exists ("post all"), but it's a human typing it, every time.

## Numbered accountability

Every signal gets a sequential ID (#422, #423...). This sounds bureaucratic; it's the opposite. It means:

- Approvals are unambiguous ("approve 423, 425" — no "yes, that one" confusion)
- The backlog is visible and countable — you can see exactly how many opportunities died waiting
- Retrospectives can audit the funnel: signals found → engaged → response received

## Daily engagement digest

Separately from outbound scanning, a daily digest summarizes inbound engagement on the accounts the team runs: who commented, what's worth replying to, drafted reply options. The exec spends five minutes choosing, not thirty minutes scrolling.

## The design principle

**The agent's job is to make the human decision as small as possible — never to make it.** Every stage compresses: raw feed → labeled signal → drafted response → one-word approval. The human's marginal cost per engagement drops to seconds, which is the only way a lean team sustains real presence across channels.
