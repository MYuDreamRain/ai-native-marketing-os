# The Decision Board

*Approval is the bottleneck. I made it a product.*

## The bottleneck nobody budgets for

The first thing an AI agent changes about a marketing function is throughput: drafts, research, event briefs, retro documents arrive faster than any team I've run could produce them. The second thing it changes is less advertised. Every one of those artifacts still needs a human to say "go," and that human is me.

Within weeks, my org's constraint had visibly moved. Work wasn't late because nothing was ready; it was late because finished items sat waiting for my verdict. The requests arrived the way requests arrive everywhere: scattered across chat threads, buried under newer messages, phrased so I'd have to scroll history to reconstruct what I was even deciding. Some expired silently. I was the queue, and the queue had no interface.

Most executives experience this as a personal failing ("I need to be more responsive") and try to fix it with discipline. I've watched that fail for years with human teams. It fails faster with an agent, because the agent's production rate doesn't have a human team's natural mercy.

So I treated my approvals as a product with exactly one user: me, on a phone, with thirty seconds.

## The design rules

The decision board is a single lightweight web page. Every pending decision is a card. The rules of the board came out of my own review comments. Each one is a complaint I got tired of writing:

**One card, one decision.** A card may not contain two questions. Bundled asks get answered at the depth of whichever question is easiest, which means the hard one gets a shallow verdict. Splitting them is the asker's job, not mine.

**A card carries everything the decision needs.** The stakes in one line, the deadline if one is real, a recommendation with a reason, and a direct link to the artifact itself. The test I gave the agent, verbatim from a correction: could someone who wasn't in the room decide from this card alone, on a phone, in thirty seconds? A request without its handle isn't a request; it's homework. That's the pattern behind most of this repo: the third repetition of a review comment means the comment should have been software.

**Clicks are instructions.** A click on a card routes back into the agent's work queue through the same channel as any typed message. Approve means the agent proceeds now, not after I remember to follow up in chat. The loop from my verdict to resumed execution has no human relay in it.

**Views are filtered, never forked.** One URL parameter renders a themed subset (one project's decisions, one week's). A focused session sees only what's relevant, but there is exactly one board and one queue underneath. The moment "the real list" lives in more than one place, no place is trusted.

## What changed

The board's direct effect was the obvious one: my verdicts got faster and stopped getting lost. The second-order effects were worth more.

**Batching replaced interruption.** Ten decisions over one coffee instead of ten context switches across a day. My decision quality went up with the batch size, which surprised me until it didn't: comparing five pending calls side by side surfaces priorities that ten scattered pings never could.

**Backlogs became honest.** When a card sits untouched for a week, that fact is visible on a screen instead of buried in a thread. The conversation it forces is the right one: should this decision exist at all, or should the default just execute? Several standing approvals got demoted to notifications this way. Silence stopped masquerading as deliberation.

**Decision hygiene moved upstream.** Because a card must be one self-contained decision with a recommendation attached, half-formed asks stopped reaching me. The agent learned to finish its thinking before requesting mine. Watching that happen taught me how many half-formed asks I used to absorb from human teams without noticing the tax.

**The queue got audited.** Every card, verdict, and timestamp is a record. When I want to know where decisions stall, mine or the system's, the data exists. Approval latency is now a metric I manage, the same as any pipeline stage.

## What stays in chat

Not everything belongs on a card. Anything I might want to *think aloud* about (strategy, positioning, tradeoffs that deserve an argument) stays conversational, because a card's whole design suppresses discussion in favor of a verdict. The board is for decisions that are genuinely ready to be one click. Sorting which is which is itself a judgment the agent had to learn, and the misfiles taught the routing rule: when a card comes back with "talk," that topic was never card-shaped.

## The general lesson

Any AI-augmented team hits this wall, usually within a month: production scales and approval doesn't. The standard responses (approve less carefully, approve less often, hire an approver) all spend the multiplier the agent was supposed to create.

The response that worked was to treat the approval surface as a designed product: one user, one interaction model, ruthless about context delivery. Nothing in it is specific to my company, my industry, or the agent platform underneath. **When judgment becomes the scarcest resource in the org, the interface to judgment deserves as much design effort as the work it approves.**
