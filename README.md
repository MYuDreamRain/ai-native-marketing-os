# An AI-Native Marketing Operating System

**I run a marketing function where an AI agent is a full team member — not a chat window.**

I'm Mengyu Wu, a marketing leader based in Singapore (Unilever → ByteDance/TikTok → Helpling APAC → Marketing Director at an AI startup). Over the past year I deployed a persistent AI agent (built on Zylos, an autonomous-agent platform — I didn't build the AI itself) and turned it into a co-worker that carries a real share of my marketing function: content production, social listening, event operations, inbox triage, and meeting prep.

To be precise about what's mine and what isn't: the platform provides the raw capabilities — persistent memory, scheduling, multi-channel messaging. What I built on top is everything that makes those capabilities a functioning marketing team member: the workflows, the approval structures, the voice and taste standards, the guardrails, and a year of accumulated corrections that trained its judgment. That layer is what this repo documents.

Everything here is sanitized: no company data, no client names, no internal links.

## Why this exists

Most "AI marketing" is a person pasting prompts into a chatbot. What I run is different in kind:

- **Persistent** — the agent has structured long-term memory (identity, active state, per-user profiles, decision logs). It remembers last month's decisions and this morning's corrections.
- **Proactive** — a scheduler lets it act without being asked: inbox scans every 30 minutes, event radar, weekly retrospective chasing, deadline guards.
- **Multi-channel** — it lives where the team lives (enterprise chat, email, web), routes replies to the right channel, and never leaks context between them.
- **Governed** — every external-facing output passes human approval gates, an anti-AI-voice review, and hard rules about what it may never do autonomously.

## The systems

| # | System | What it does |
|---|--------|--------------|
| 1 | [Operating model](systems/01-operating-model.md) | Memory architecture, scheduling, multi-channel routing — how an AI agent becomes a durable team member |
| 2 | [Content engine](systems/02-content-engine.md) | Idea capture → topic mining → drafting → human-voice review → approval → publish, across platforms |
| 3 | [Anti-AI-voice gate](systems/03-anti-ai-voice-gate.md) | The review pipeline that keeps published copy from sounding like a machine wrote it |
| 4 | [Social listening engine](systems/04-social-listening-engine.md) | Signal scanning with a FLAG / ENGAGE / MONITOR triage and an approval-gated auto-poster |
| 5 | [Decision board](systems/05-decision-board.md) | An async web UI that turns "the exec is busy" from a blocker into a one-click queue |
| 6 | [Event marketing ops](systems/06-event-ops.md) | Event radar, clash detection, ROI-tracked retrospectives that chase their own missing data |
| 7 | [Inbox & meeting ops](systems/07-inbox-meeting-ops.md) | Email triage with team-aware routing, and auto-generated meeting prep packages with attendee research |

Plus the part most portfolios skip: [Guardrails & governance](guardrails.md) — the rules that make it safe to give an AI real autonomy, written in blood (well, incident reports).

## What I actually learned

1. **The bottleneck moves from production to judgment.** When drafting is nearly free, the scarce resources are taste, approval bandwidth, and knowing what *not* to publish. Half the systems here exist to protect those.
2. **Memory design is the real product.** An agent without structured memory relearns your preferences every session. The tiered memory model (always-loaded identity/state vs. on-demand reference files) is what makes corrections stick.
3. **Autonomy must be earned per-task, not granted globally.** Publishing needs approval gates; inbox triage doesn't. Mapping that boundary — and encoding it as rules the agent enforces on itself — is the core management skill of the next decade.
4. **AI-sounding copy is a solved problem if you treat it as QA.** A separate review pass with named tells ("not X, but Y" constructions, em-dash chains, hedge stacking) catches what the drafting pass can't see about itself.

## Contact

- LinkedIn: [linkedin.com/in/mengyuwu](https://www.linkedin.com/in/mengyuwu)
- Based in Singapore · open to conversations about AI-native marketing organizations
