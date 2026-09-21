# System 5 — The Creative Ops Pipeline

*Every visual asset is generated from code, checked against a brand spec, and reviewed by the agent looking at its own render before I ever see it.*

## The core move: visuals as code

Decks, interactive product demos, key visuals, event collateral, data dashboards — all built as HTML/SVG and rendered to whatever the channel needs. That one decision buys three things:

1. **Revisions are diffs.** "Make the logo mark the hero, not a letterform" is an edit, not a redo.
2. **Brand rules are enforceable.** Colors, typography, logo usage live in one quick-reference file the agent must read before any visual work; violations are checkable, not a matter of taste-on-the-day.
3. **Delivery is a URL.** A sales deck ships as a web page with an access policy I set, not an attachment that forks into six stale copies.

## The render-and-look loop

The agent doesn't hand me its first output. It renders the asset to an image, *looks at the render*, and fixes what it sees — clipped text, crowded composition, a stray stroke across a character's face — before delivery. The same discipline as the writing system's [taste gate](04-taste-gate.md), applied to pixels: the producing pass can't see its own mistakes; a looking pass can.

My feedback rounds work like the writing corrections: each verdict ("too crowded — remove background elements") applies to the class, not the instance, and rejected elements go on a registry so they never come back in asset #40.

## What it did in practice

The cycle that used to be a week of designer back-and-forth: a client-specific interactive product demo, briefed in a chat message before noon, live at a URL for the afternoon meeting. Same-day key-visual iterations at three feedback rounds before lunch. None of this replaces the designer on brand-defining work; it removes the queue for everything that shouldn't need one.
