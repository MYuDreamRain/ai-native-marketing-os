# System 7 — Inbox & Routing Operations

*The unglamorous system that pays for all the others.*

## The problem it solves

Shared inboxes (contact@, marketing@) are where revenue goes to die. A real incident started this system: a customer reply sat unanswered for 15 days because it landed in a monitored-by-nobody inbox. The response wasn't "check more often" — it was to make checking a machine's job.

## Team-aware routing

Every 30 minutes during business hours, the agent scans the shared inboxes and routes each new email by type — and by *team topology*:

| Email type | Route |
|-----------|-------|
| Sales inquiry (international) | → regional sales lead, DM |
| Sales inquiry (domestic-language) | → domestic sales lead, DM |
| Customer support / refunds / account issues | → the CS owner's dedicated group, with an @mention |
| Event organizers, partners, press | → marketing owner immediately, with suggested action |
| Newsletters, job applications, system notices | filtered, no human interruption |

Before routing, the agent checks the thread: **if a teammate already replied, it says so** ("already answered by X") instead of creating duplicate work. After routing, a same-day digest goes to a shared channel — sender, ask, who it went to, status — so the whole team sees inbox health without anyone reading the inbox.

## Design details that matter

- **Deduplication state.** Every processed email is marked; the scan is idempotent. No email surfaces twice, none slips between scan windows.
- **Noise discipline.** An empty scan produces *no message at all*. Alert fatigue kills routing systems faster than missed emails do; silence must mean "nothing new," reliably.
- **Suggested action attached.** A routed email arrives with a proposed next step ("this is the organizer's spec question — want me to draft the reply?"), not just a forward.

## Why it's in a marketing portfolio

Marketing owns more shared surfaces than any other function — event inboxes, contact forms, social DMs, press lines. Response latency on those surfaces *is* brand experience. This system took ours from "days, sometimes never" to "minutes to routed, same-day to human answer" — with zero additional headcount and zero heroics.
