# An AI-Native Marketing Operating System

**I run a marketing function where an AI agent is a full team member, not a chat window.**

I'm Mengyu Wu, a marketing leader based in Singapore (Unilever → ByteDance/TikTok → Helpling APAC → Marketing Director at an AI startup). Over the past three months I turned a persistent AI agent into a co-worker that carries a real share of my marketing function: executive LinkedIn strategy, content production, PR and competitive intelligence, social listening and social selling, event operations from radar to post-event ROI review, inbound lead routing, meeting intelligence, and the research and analysis under CMO-level planning.

This repo documents the layer that makes that possible: the workflows, approval structures, voice and taste standards, and guardrails I built and trained into it through months of daily operation.

Everything here is sanitized: no company data, no client names, no internal links.

## If you only have three minutes

Five files carry most of the signal. In order:

1. [The Rulebook](rulebook.md) — the correction protocol and four before/after corrections; the shortest path to how I manage an AI teammate
2. [The Decision Board](decision-board.md) — approval as a designed product; read "The design rules"
3. [The Field-Marketing Ops Kit](field-marketing-ops-kit.md) — ~35 event workstreams, two markets, 90 days; skim the AAR protocol
4. [The Outcomes Ledger](outcomes.md) — every number labeled measured / counted / directional, with what's deliberately excluded
5. [The Taste Gate](systems/04-taste-gate.md) — the three-layer editorial system that holds quality at machine throughput

## Why this exists

Most "AI marketing" is a person pasting prompts into a chatbot. What I run is different in kind:

- **Persistent.** The agent has structured long-term memory (identity, active state, per-user profiles, decision logs). It remembers last month's decisions and this morning's corrections.
- **Proactive.** A scheduler lets it act without being asked: inbox scans every 30 minutes, event radar, weekly retrospective chasing, deadline guards.
- **Multi-channel.** It lives where the team lives (enterprise chat, email, web), routes replies to the right channel, and never leaks context between them.
- **Governed.** Every external-facing output passes human approval gates, a taste-gate review, and hard rules about what it may never do autonomously.

## Start here: the five artifacts

The part of this system no platform ships and no prompt library contains. Each is a management artifact: judgment made inspectable and enforced.

| Artifact | What it is |
|----------|------------|
| [The Governance Charter](guardrails.md) | The constitution I wrote before the agent got autonomy: identity rules, channel firewalls, approval gates scoped by irreversibility, and the incident → rule pipeline |
| [The Rulebook](rulebook.md) | How I compile my judgment into an enforced spec: the correction protocol, the standing rules it produced, and four before/after corrections |
| [The Decision Board](decision-board.md) | Approval is the bottleneck; I made it a product: a designed surface for the scarcest resource in an AI-augmented org |
| [The Field-Marketing Ops Kit](field-marketing-ops-kit.md) | ~35 event workstreams, two markets, 90 days: event radar, go/no-go discipline, deadline guards, and retrospectives that chase their own data |
| [The Outcomes Ledger](outcomes.md) | The numbers, each labeled with how much to trust it: measured / counted / directional, with what's deliberately excluded |

## The systems underneath

Ordered from strategy to execution: how the organization runs, what the brand says, how demand gets created, how nothing drops.

| # | System | What it does |
|---|--------|--------------|
| 1 | [Operating model](systems/01-operating-model.md) | Memory architecture, scheduling, multi-channel routing: how an AI agent becomes a durable team member |
| 2 | [Executive LinkedIn OS](systems/02-linkedin-os.md) | A personal LinkedIn presence run as an operating system: one versioned strategy bible, fixed cadence, feedback that rewrites the strategy |
| 3 | [Content engine](systems/03-content-engine.md) | Idea capture → topic mining → drafting → human-voice review → approval → publish, across platforms |
| 4 | [Taste gate](systems/04-taste-gate.md) | The three-layer editorial system (tells → craft → story) that holds publishing quality at machine throughput |
| 5 | [Creative ops pipeline](systems/05-creative-ops.md) | Visuals as code: brand rules enforced from a spec file, and the agent reviews its own render before delivery |
| 6 | [Social listening engine](systems/06-social-listening-engine.md) | Market-wide signal scanning with a FLAG / ENGAGE / MONITOR triage and an approval-gated auto-poster |
| 7 | [Social selling pipeline](systems/07-social-selling.md) | A named list of prospects and partners, engaged one approved touch at a time: staged plays, per-relationship memory, zero autonomous posting |
| 8 | [Event marketing ops](systems/08-event-ops.md) | The mechanics under the ops kit: radar, clash detection, deadline guards, retro chasing |
| 9 | [Inbound response ops](systems/09-inbound-response-ops.md) | Shared-inbox triage with team-aware lead routing: minutes to routed, same-day to answered |
| 10 | [PR & media engine](systems/10-pr-media-engine.md) | Daily news radar with a comment / hook / pitch taxonomy, journalist matching, and a weekly competitive scan — zero autonomous outreach |

## What I actually learned

1. **The bottleneck moves from production to judgment.** When drafting is nearly free, the scarce resources are taste, approval bandwidth, and knowing what *not* to publish. Half the systems here exist to protect those.
2. **Autonomy must be earned per-task, not granted globally.** Publishing needs approval gates; inbox triage doesn't. Mapping that boundary, and encoding it as rules the agent enforces on itself, is the core management skill of the next decade.
3. **Memory design is the real product.** An agent without structured memory relearns your preferences every session. The tiered memory model (always-loaded identity/state vs. on-demand reference files) is what makes corrections stick.
4. **Scrubbing AI tells is QA; good writing is the real bar.** A review pass with named tells ("not X, but Y" constructions, em-dash chains, hedge stacking) reliably catches what the drafting pass can't see about itself — that half is mechanical. But scrubbed only gets a text to neutral, and neutral doesn't earn a read. The standards that raise the ceiling are positive: a stance someone could argue with, details only this author could supply, sentences that buy the next one. Rules about what not to do cap the damage; rules about what to do are the editorial system.

## Contact

- LinkedIn: [linkedin.com/in/mengyuwu](https://www.linkedin.com/in/mengyuwu)
- Based in Singapore · open to conversations about AI-native marketing organizations
