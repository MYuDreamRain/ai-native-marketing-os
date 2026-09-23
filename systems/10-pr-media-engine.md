# System 10 — The PR & Media Engine

*The execution layer of a PR agency — monitoring, media lists, pitch drafting, competitive intel — run by the agent. The relationships stay human, and the agent never sends a pitch.*

## The daily loop

```
morning news radar ──► tag: COMMENT / HOOK / PITCH ──► journalist match + topic cards ──► reviewer pass ──► digest ──► human decides
```

**The radar.** Every morning a scheduled scan sweeps configured sources — regional business and tech outlets, the global AI majors' newsrooms, domestic-language tech press. The output is not a clipping pile: it's two to four *windows*, each one an opportunity with a suggested action attached. The strongest window leads the digest as a one-line bulletin.

**The taxonomy.** Every item gets exactly one primary tag, and the tag determines the downstream path:

- **COMMENT** — a news window worth a same-day executive take (a newsjack, in the classic sense). Ships with a drafted angle in the voice of the target platform; the [LinkedIn OS](02-linkedin-os.md) or its domestic-platform equivalent takes it from there.
- **HOOK** — a story that can anchor owned content. These get filed as *topic cards* into the [content engine's](03-content-engine.md) production pipeline, source line marked "news radar," where they compete with every other topic for a slot.
- **PITCH** — an earned-media opening: a data point, trend, or gap where the company has something real to contribute. Ships with a named journalist match and a one-line "why this person."

**Journalist matching.** Behind PITCH sits a tiered media database the agent built through research sprints: beat, recent articles, writing habits, the specific angle that would interest this specific person, and a full outreach log. Two rules from build day: **no guessed emails** — if a contact isn't public, the record says "not public," never a pattern-guess — and **every claimed article URL is verified or explicitly marked unverified**. A media list is only as good as its worst fabricated row.

**Dedup and language routing.** A seen-items log (one line per item ever featured) keeps the radar from re-serving old news. Each item is written in the language of its *target platform* — an opportunity aimed at domestic-language media arrives in that language, everything else in English.

**Reviewer pass.** Before the digest posts, an independent reviewer agent spot-checks claims against their sources (does the linked article actually carry that number?) and sweeps for AI tells — the same write/review separation as the [taste gate](04-taste-gate.md). A digest that misattributes a statistic today becomes a pitch that embarrasses an executive next month.

## The weekly competitive scan

On a weekly cadence the agent scans a named competitor list for funding rounds, product launches, key hires, pricing changes, partnerships, and M&A. Each finding gets three lines — what happened, what it means for us, recommended response — and one of four tags: **Act Now / Watch / Opportunity / Noise**. Findings are written back into a living competitive-intelligence file, so every scan diffs against history instead of rediscovering the landscape. The intel feeds positioning and pitch angles; it is never quoted externally.

## The hard rules

1. **Zero autonomous outreach.** The agent matches, drafts, and suggests; no email or DM ever goes to a journalist without a human sending it. Media relationships are the one PR asset that can't be automated and can be destroyed by automation.
2. **Approved-claims discipline.** A standing frozen-facts list names every number and case story that may not be cited externally until confirmed. Drafts are checked against it; the fallback is behavior-based proof ("customers were using it the same day") over unverified statistics. The list exists because one hallucinated metric was caught early — and became a rule the same day (see [the rulebook](../rulebook.md)).

## What it replaces, honestly

Agency benchmarks put retainer PR at thousands per month, and most of that spend is execution: monitoring, list building, draft pitches, coverage tracking. That layer is now the agent's, at near-zero marginal cost and daily cadence instead of weekly. What it doesn't replace: the trust a journalist extends to a person, crisis judgment, and the decision of what story we actually want to be telling. Those stayed exactly where they belong.
