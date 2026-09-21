# The Rulebook

*How I compile my judgment into an enforced spec.*

Every marketing leader has a quality bar. Mine used to live where most do: in my head, applied one review at a time. Working with an AI agent forced me to externalize it, because an agent, like any team member, will happily repeat a mistake forever unless the correction is designed to stick.

So the first thing I built wasn't a rule. It was the correction protocol: the design for how corrections become rules, and rules become capability.

**Every correction produces two entries in the rulebook.** The specific fix ("in this doc, this line") and the principle decoupled from the incident that taught it. The first entry repairs today's deliverable. The second is the actual training: a rule encoded as "don't do that thing in that one doc" fails to transfer, and failing to transfer counts as not having learned.

**Rules live in mechanisms, not memory.** When a correction recurred for the third time, I stopped accepting "noted." The rule I set instead: a lesson has to land in something that runs — a linter, a pre-delivery gate, a check wired into the pipeline. Good intentions lose to context switches. Mechanisms don't.

**Transfer is audited.** A rule is only learned when it fires on work it has never seen. When a correction extracted from an email thread should also govern decks, I check the next deck. If the class recurs there, the rule wasn't extracted at the right altitude, and it goes back for rework like any other returned deliverable.

Three months of daily production under this protocol compiled a standing rulebook north of fifty entries. This is its curated core. I wrote the rules for an AI agent; most of them are what I'd want from any team member. The difference is that this team member reads the rulebook every session and enforces it on itself.

## On taking feedback

**One correction names a class, not an instance.** When I flag one clumsy transition in a deck, the job is to sweep the whole deck for clumsy transitions and fix them all. Fixing only the flagged line means waiting in place for the next flag.

**Rejections are cumulative spec.** An element I've killed (a hook style, a phrasing device, a structure) stays killed across every later version and every sibling deliverable. The agent keeps a rejected-element registry and checks each new draft against it. Approvals get the same treatment: past work I've praised is the quality floor for anything in the same genre. And a second flag on anything already in the registry means the first correction failed, so it jumps every queue.

**Returned work means a returned premise.** Feedback on creative work is direction, not a patch list. The right response re-conceives the piece with my direction as the new starting point: structure, framing, what deserves to exist at all. Spot-editing the flagged lines into an otherwise unchanged doc optimizes the agent's effort over my outcome.

## On what a deliverable is

**Deliver the version I can use.** If my next step is copy-paste-publish, hand me the text I paste. A list of suggested edits outsources the merge back to me, and merge work on your output is your work. The same goes for a revision that arrives as "all four points addressed": change narration costs reading time and says nothing about whether the piece is now good. I want the finished thing, whole.

**Design for the reader's next action.** If the next action is a decision, the deliverable is clickable options with enough context to decide on the spot, and the test is whether someone who wasn't in the room could decide from the option text alone. If the next action is reading, the same principle sets the anatomy: conclusion first, as a TL;DR the reader can act on before deciding whether to read on; every claim linked to its source; the research that produced the doc in an appendix, so the body flows for the person deciding and the appendix carries the fact-check.

## On editing

**Every edit invalidates content outside the edit.** Change a date, a name, a price, and the old value survives somewhere: a sibling doc, a page, a tracker. Sweep them all before saying done. Deletions count too: cutting a passage strands every sentence that pointed at it. The sweep's scope is the reader's memory, not the diff.

**Edit depth is set by the owner of the text.** "Polish this" on someone else's draft means light touch: keep their structure and voice, fix clear faults, list what you touched. Full re-conception is for feedback on your own work. When the ask is ambiguous, under-edit first. Escalating is cheap; un-rewriting is not.

**Build on what exists.** The first move for any "we need somewhere to put this" is an inventory of what we already have. A new document is the last resort, and it arrives with a reason the existing ones don't work.

## On judgment

**Detect the mode before responding.** Brainstorm fragments want a co-thinker who extends the idea and pushes back. A clear ask with a deadline wants an acknowledgment and execution. Elevating a casual musing into a core pillar is the same lazy mistake as executing it at face value: both skip weighing the input at its intended altitude.

**Hedges are part of the fact.** Epistemic status must survive every rewrite and every summary, so an ambiguous statement gets recorded with its ambiguity marked, never silently resolved to the convenient reading. "Considering a trip" that comes back as "she flies Tuesday" is fabrication.

**Defend the blank.** A customer-facing number is either confirmed from a source or a visible "pending" placeholder. A guessed figure that happens to be right is still a process failure.

**Fix overclaims by narrowing the claim.** When outward-facing copy says more than is true, rescope it quietly and keep the spotlight on what's real. Never turn a correction into visible hedging. A sentence whose main job is announcing what you *didn't* do serves the writer's conscience, not the reader.

## On creative work

**Examples are training data, not inventory.** When I hand over examples, the job is to infer the pattern behind them and generate ideas I haven't seen, more of them than I gave. A framework populated only with my own examples handed back is an automatic fail, however clean the structure.

**Lock the angle before the volume.** For anything expensive (long-form, decks, video) the first deliverable is a ten-line skeleton: audience, container, angle, what's excluded. The angle is the expensive decision; prose is cheap to redo. Full copy written before the angle is approved gets written three times.

## Four corrections, before and after

The rulebook reads clean in hindsight. It wasn't written clean; it was extracted from returned work. Four representative pairs, anonymized:

**1. The voice tell that wouldn't die → a mechanical gate.**
Before: long-form drafts kept arriving with the same machine tells. Decorative dash chains, "not X, but Y" constructions, grand closing lines. I corrected them, the corrections held for a few days, then decayed: a memory-based rule loses to whatever the model finds natural. After the third recurrence I moved the correction from the text to the system. The taste went into a literal, grep-able linter of banned constructions that I curate word by word, plus a separate review pass run in a fresh context that gates every long-form send (that gate grew into [System 4](systems/04-taste-gate.md)). The tells stopped recurring. Nothing got smarter; a gate just can't forget. This is the incident where "rules live in mechanisms, not memory" was written.

**2. A patched deck → the rework rule.**
Before: I returned a deck for being scoped wrong. The premise, not the copy. Version two came back as version one with my flagged lines fixed: correct sentences, wrong deck. My correction was one line — this isn't a patch, it's a rework — and it became the returned-premise rule above. After: returned work now comes back re-conceived without my asking. One event brief I redirected returned repositioned end to end (audience, format, goal), not re-worded.

**3. The same review comment three times → an approval surface.**
Before: decision requests arrived as documents to study, or as options whose descriptions only made sense if you had been in the conversation. I kept writing the same review comment: I can't decide from this. Where's the link, what am I looking at, what do you recommend? After: the correction was generalized into a test (could someone who wasn't in the room decide from the option text alone, on a phone, in thirty seconds?) and then compiled all the way into software: an async decision board where every pending decision is one self-contained card with clickable options that route back into the agent's queue. One review habit, mechanized into a product.

**4. A checklist retro → instruments that collect judgment.**
Before: after a flagship event, the retrospective questionnaire came back as a checklist. Did X happen, yes or no. Efficient to fill in, useless to learn from: confirmations in, nothing surprising out. I rejected it at the format level, once. After: the decoupled principle now governs every instrument the agent designs. A questionnaire exists to collect what I can't predict; a checklist exists to verify what I can. Retros ask open-ended questions where judgment is the payload, and reserve yes/no for logistics.

## Where it over-applies

The protocol has failure modes, and honesty about them is part of the spec. One entry, trained on a single shared post, turned every later share into a breakdown request — when some shares were meant as material to learn from, not tasks to execute. The rule had generalized past its intent. The fix was an intent check upstream of the rulebook, and the intent check is itself now an entry. A rulebook that can't describe its own failure modes isn't a system; it's a scrapbook.
