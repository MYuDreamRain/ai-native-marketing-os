# System 5 — The Decision Board

*The scarcest resource in a marketing org isn't budget. It's decision bandwidth.*

## The problem

An AI agent removes the production bottleneck — and immediately exposes the next one. Work piles up not because nothing is ready, but because every finished item needs a busy human to say "go." Decisions arrive scattered across chat threads, get buried under new messages, and silently expire.

## The fix

A single lightweight web page — the decision board — where every pending decision is a card:

```
┌──────────────────────────────────────────┐
│  Poster final v2 — approve for print?    │
│  context: 1 line · deadline: today       │
│  [ Approve ]  [ Needs change ]  [ Talk ] │
└──────────────────────────────────────────┘
```

Rules of the board:

- **One card = one decision.** No card may contain two questions.
- **A card carries its own context.** The exec should never have to scroll chat history to decide. One-line stakes, link to the artifact, deadline if real.
- **Clicks flow back into the agent's queue.** A click is a message; the agent acts on it within the same routing system as any other instruction.
- **Filtered views** — the board can render themed subsets (e.g. only decisions for one project) via a URL parameter, so a focused session sees only what's relevant.

## Second-order effects

The board changed behavior in ways the chat threads never did:

1. **Batching.** The exec clears 10 cards over coffee instead of context-switching 10 times a day.
2. **Honest backlogs.** When a card sits for a week, that's visible — the conversation becomes "should this decision exist at all?" rather than silence.
3. **Decision hygiene upstream.** Because cards must be one decision with self-contained context, the agent (and the humans) learned to *frame* decisions properly before asking. Half-formed asks never make it to a card.

## The general lesson

Any AI-augmented team will hit this wall: production scales, approval doesn't. Treating approvals as a designed product surface — not an ambient chat behavior — is what keeps the multiplier from being eaten by queue time.
