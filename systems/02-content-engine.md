# System 2 — The Content Engine

*From "I saw something interesting" to published post, with humans only at the judgment points.*

## Pipeline

```
capture ──► context bank ──► topic mining ──► draft ──► anti-AI-voice gate ──► approval ──► publish ──► backfill
```

**Capture.** A one-tap drop form (mobile-friendly web page) where anyone on the team can toss in a link, screenshot, or half-formed thought. Zero-friction capture is the whole point — ideas die in the gap between "saw it" and "wrote it down."

**Context bank.** Captures land in a structured table with dedup checks. The agent enriches each entry: what it is, why it might matter, which content lane it could feed.

**Topic mining.** On a weekly cadence the agent proposes a shortlist — e.g. a two-week topic slate with a one-line angle per topic — and the human circles winners. Selection is a judgment call; it stays human.

**Drafting.** The agent drafts platform-native versions (a long-form newsletter section is not a LinkedIn post is not a carousel script). Platform grammar is encoded per channel: hook conventions, length norms, CTA placement.

**Review.** Every draft passes the [anti-AI-voice gate](03-anti-ai-voice-gate.md) before a human ever sees it — reviewer time is spent on substance, not on fixing robotic phrasing.

**Approval.** Nothing publishes without an explicit human "approved" per piece. The approval request is designed for a busy exec: the draft, a one-line summary of what changed since last round, and a single decision to make.

**Backfill.** After publishing, the agent writes results back to the content library (what ran, where, when) so the next topic-mining pass learns from history.

## Multi-lane, one engine

The same pipeline runs several lanes in parallel with different cadences and different approval owners:

- A weekly AI-industry digest (long-form, editorial voice)
- Executive thought-leadership posts (personal voice — the hardest lane; see the voice gate)
- An employee-advocacy lane: drafts prepared *for* team members to post under their own names, each requiring that person's approval
- Platform-specific series (carousels, short video scripts) with visual briefs handed to design

## The two numbers that matter

Content engines are usually judged on volume. Wrong lens. The two numbers I manage are:

1. **Approval-to-publish latency** — how long a finished draft waits for a human decision. This is where throughput actually dies, which is why the [decision board](05-decision-board.md) exists.
2. **Revision depth per piece** — how many correction rounds before approval. Every correction becomes a standing rule (see the correction loop in [System 1](01-operating-model.md)), so this number trends down per lane over time.
