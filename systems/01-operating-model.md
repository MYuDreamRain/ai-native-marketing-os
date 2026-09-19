# System 1 — The Operating Model

*How an AI agent goes from "tool you open" to "colleague who's already working when you wake up."*

## The shape of it

```
                       ┌─────────────────────────┐
  Enterprise chat  ──► │                         │ ──► replies (channel-exact)
  Email inboxes    ──► │   Persistent AI agent   │ ──► published content (gated)
  Web console      ──► │   (24/7, single brain)  │ ──► dashboards, reports
  Scheduler        ──► │                         │ ──► calendar events, alerts
                       └───────────┬─────────────┘
                                   │
                       ┌───────────▼─────────────┐
                       │   Tiered memory (files) │
                       └─────────────────────────┘
```

One agent, one continuous identity, many channels. Messages from every source flow through a single communication bridge with a database queue; every incoming message carries its return path, and the agent replies on exactly that path.

## Tiered memory

The design problem: context windows are finite, but a colleague's knowledge isn't. The answer is tiering by load frequency:

| Tier | Loaded | Contains |
|------|--------|----------|
| Identity | Every session | Who the agent is, principles, communication style |
| Standing directives | Every session | Hard rules learned from incidents (see [guardrails](../guardrails.md)) |
| Active state | Every session | Current focus, pending tasks, blockers — a living to-do file |
| References | Every session | Pointers: channel IDs, key documents, API endpoints |
| User profiles | On demand | Per-person preferences, correction history |
| Decision & project logs | On demand | Why things were decided; full project context |
| Session archive | Rarely | Cold storage, day-by-day event logs |

The always-loaded tiers are kept deliberately lean (single-digit KB each) — they're a table of contents, not an encyclopedia. When the agent needs depth, it reads the on-demand file. **A file read is cheaper than a wrong assumption** is a literal rule in the system.

## The correction loop

The highest-leverage rule in the whole system is meta: **every time I correct the agent, it must write down two things — the specific lesson, and the underlying principle decoupled from the incident.** Rules encoded too narrowly don't transfer; that counts as not having learned.

Example: after it once buried a deliverable link under three paragraphs of preamble, the rule it wrote wasn't "put links first in weekly reports" — it was "LINE 1 of every outbound message = the link / conclusion / decision needed."

## Proactive operation

A scheduler turns the agent from reactive to proactive. Real recurring jobs in production:

- Inbox scans (every 30 min, business hours) with routing rules per email type
- Meeting-invite detection → calendar event + attendee research + prep package
- Weekly social listening scans and daily engagement digests
- Deadline guards ("if no reply by 14:30 on deadline day, send one nudge with the fallback ready")
- Retrospective chasers that escalate politely on day 8, day 19...

The management insight: you delegate *outcomes with deadlines*, not steps. "Guard this deadline; the fallback is already delivered; if she's silent, nudge once" is a real task description from the system.

## What this replaces

Not a person. It replaces the *coordination tax*: the follow-ups nobody sends, the inbox nobody triages at 7am, the retrospective data nobody chases, the meeting prep nobody has time for. The humans keep judgment, relationships, and taste.
