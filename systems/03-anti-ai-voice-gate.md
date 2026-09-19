# System 3 — The Anti-AI-Voice Gate

*AI drafting is free. AI-sounding copy is expensive. This is the QA layer between the two.*

## The problem

Readers have learned the tells. A piece that opens with "In today's fast-paced digital landscape," pivots on "It's not just X — it's Y," and closes on "The future is here" doesn't just read badly — it signals *nobody senior looked at this*. For an executive's personal voice, that's brand damage.

The fix isn't "prompt it to sound human." A model can't reliably see its own tells in the same pass that produced them. The fix is structural: **a separate review pass, by a separate agent instance, with a named checklist.**

## Write / review separation

```
draft agent ──► file ──► reviewer agent (fresh context) ──► pass token ──► send/publish
```

The reviewer never sees the drafting conversation — it judges the text cold, the way a reader would. Longer outbound pieces are *blocked at the transport layer* unless they carry a valid pass token from the reviewer. Not a convention — a hard gate in the pipeline. (The same pattern as code review: authors don't approve their own PRs.)

## The tell checklist (excerpt)

The reviewer hunts named patterns, each with a concrete rewrite rule:

| Tell | Example | Fix |
|------|---------|-----|
| Negation-pivot | "It's not just a tool — it's a teammate" | Say the actual claim once, directly |
| Hedge stacking | "could potentially help enable" | One verb, committed |
| Em-dash chains | three per paragraph | Max one; restructure the sentence |
| Empty superlatives | "game-changing", "revolutionary" | Replace with the specific difference |
| Symmetric triads | "faster, smarter, better" | Break the rhythm or cut two |
| Universal opener | "In an era of rapid change..." | Start with the concrete thing |
| Bow-tie ending | "Exciting times ahead!" | End on the last real point |

Plus a positive test: does any sentence contain something only *this author* would say — a real number, a named incident, an opinion someone could disagree with? Zero such sentences = fail, regardless of tells.

## Voice files

Each publishing voice (the company account, each executive who posts) has a voice profile built from their real writing: sentence-length distribution, favored constructions, what they'd never say. Drafts are checked against the profile, and the profile is updated when the person edits a draft — their edits are ground truth.

## Why this is a marketing system, not a writing trick

Every brand is about to face this: AI makes content volume free, which makes *distinctiveness* the entire game. A repeatable, auditable process for keeping a human voice at machine throughput is a competitive asset. This one runs in production daily.
