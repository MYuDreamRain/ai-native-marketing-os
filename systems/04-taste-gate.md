# System 4 — The Taste Gate

*AI made content volume free, which made taste the entire game. This is the editorial system that holds publishing quality at machine throughput.*

## The problem

Most teams frame this as "make the AI not sound like AI," buy a detector, and stop there. That solves the wrong problem. Scrubbing the tells gets a text to neutral, and neutral doesn't earn a read. A piece can pass every AI-detection check and still have no stance, no story, and nothing only this author could say.

So the gate here judges three things, in order of depth: does it sound like a machine, is the writing any good, and does it move like a story. A detector answers the first question with a score. An editor answers all three with named faults and rewrite rules. This system is built as the editor.

## Layer 1 — the tell check (baseline)

The shallow layer, kept because it's cheap and catches real damage. The reviewer hunts named patterns, each with a concrete fix:

| Tell | Example | Fix |
|------|---------|-----|
| Negation-pivot | "It's not just a tool — it's a teammate" | Say the actual claim once, directly |
| Hedge stacking | "could potentially help enable" | One verb, committed |
| Empty superlatives | "game-changing", "revolutionary" | Replace with the specific difference |
| Symmetric triads | "faster, smarter, better" | Break the rhythm or cut two |
| Universal opener | "In an era of rapid change..." | Start with the concrete thing |
| Fake-candid theater | "Honestly?", "Here's the thing" | Delete; candor is content, not a costume |
| Bow-tie ending | "Exciting times ahead!" | End on the last real point |

The list is versioned and rots on purpose: vocabulary tells drift with every model generation, so the durable value is in the layers below.

The Chinese checklist is not a translation of the English one. Chinese AI prose has its own fingerprints (translated-English syntax, empty grand words, couplet pile-ups), so the CN rules were built separately, from Chinese stylists (Yu Guangzhong, Si Guo, Wang Zengqi), not ported over. I run a bilingual APAC content operation; there, that distinction is the difference between a gate and a decoration.

## Layer 2 — craft (what editors actually check)

The middle layer is a craft checklist distilled from working writers and editors (Orwell and Zinsser on prose; Ogilvy and Schwartz on advertising), compressed into checks a reviewer can run mechanically:

- **The stance test.** At least one claim someone could disagree with. An opinion no one could argue against is not an opinion, and text with no stake in its claims is the deepest tell of all.
- **The only-this-author test.** Does any sentence contain something only this writer could say: a real number, a named decision, a lived detail? Zero such sentences fails the piece regardless of polish.
- **Concreteness quota.** Two particulars per hundred words. The portability check: if a sentence could move unchanged to another company's post, it's filler.
- **Strongest word last.** The period amplifies what sits before it; move the payoff to the end of the sentence.
- **Ladder of abstraction.** Live at the bottom (things you can see), earn one line at the top (what it means), never camp in the middle: half-abstract management language is where B2B slop lives.
- **One example dug deep** beats three examples queued. Unpack the mechanism of one case instead of stacking citations.
- **The self-persuasion detail.** Ogilvy's old trick: give the reader one detail specific enough that they draw the conclusion themselves, instead of being handed the adjective.

## Layer 3 — story (why anyone keeps reading)

The deepest layer, and the one no detector even attempts:

- **A lead is a promise.** The opening's bar is fidelity to what follows: no blind leads that withhold the name as a tease, no cute leads that use wit as warm-up.
- **The next-sentence principle.** Each sentence's job is to buy the next one. Each paragraph's first sentence grows out of the previous paragraph's last.
- **Story means gap, not events.** The minimal story unit is the distance between what someone expected and what happened. No gap, no story: just a list.
- **The beat audit.** Pull each paragraph's first sentence and label its link to the previous beat: *but*, *therefore*, or *and-then*. Every "and-then" is a break point.
- **Open loops close.** Curiosity gaps are fuel, with a quota. And every loop opened must close before the piece ends, or the reader stops trusting the writer's hooks.
- **Endings echo, never inflate.** Returning to a concrete object from the opening works; a closing sentence that introduces a new abstraction (meaning, the future, an era) gets deleted, and the piece ends on its last real point.

## The recalibration — when passing the gate became the tell

The gate itself gets corrected, and the hardest correction came late: a draft that passed every layer above still read as machine-made. The fault wasn't a banned construction; it was that *every line was polished and load-bearing*. Written tidiness — no rough edges, every sentence earning its place, uniform density — turned out to be an AI fingerprint of its own, invisible to any checklist because each individual sentence is fine.

Two mechanisms came out of that incident:

- **The read-aloud test against a human anchor.** The final pass judges the draft against a reference the way a human ear would: a real transcript, a great speech, plain journalism. The register bar is prose that never performs — staged reveals, significance narration ("here's why this matters"), aphoristic beat-drops all fail, because staged writing dies when spoken. "Too tidy" is now a named failing verdict. Lint alone is never sufficient to pass.
- **The human-source rule.** The human touch is sourced, never synthesized: before drafting anything substantive, the agent asks the piece's owner for lived material — what they saw, a real story, where they disagree. That answer becomes the center of the piece. No answer means lower ambition, stated in the plan; it never means fabricating texture.

## Enforcement — what makes this a system instead of advice

```
draft agent ──► lint ──► reviewer agent (fresh context) ──► read-aloud vs human anchor ──► pass token ──► publish
```

- **Writer and gate are never the same instance.** The reviewer judges the text cold, without the drafting conversation, the way a reader would — and reads the human anchor before the draft, so the ear is calibrated before judgment starts. Longer outbound pieces are blocked at the transport layer without a valid reviewer token: a hard gate in the pipeline, not a convention. I tried self-certification first: under deadline pressure it degraded to rubber-stamping every time.
- **A mechanical lint runs first**, catching the grep-able layer (banned constructions, leaked citation markup, formatting violations) so the reviewer spends its judgment on judgment.
- **Voice files.** Each publishing voice has a profile built from that person's real writing, and the profile updates when the person edits a draft — their edits are ground truth, outranking every generic rule.
- **Taste memory.** Every element the owner has ever rejected (a hook style, a phrasing device, a structure) lives in a registry that each new draft is checked against. Rejections are cumulative spec: killed once means killed in every future version.

That last mechanism is the real difference from any detector on the market. A detector's verdict is a score that teaches nothing. This gate's verdict is a named pattern with a rewrite rule, and every human correction becomes a permanent new check. The standing [rulebook](../rulebook.md) behind it has grown from zero to north of fifty entries in three months, calibrated to one team's taste rather than to an average of the internet.

## Why this is a marketing system, not a writing trick

When volume is free, distinctiveness is the entire game. This gate runs in production daily, in two languages.
