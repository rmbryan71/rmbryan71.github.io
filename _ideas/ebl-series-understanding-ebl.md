# SERIES: Understanding EBL

## Series Overview
A five-article sequence for a reader who has never heard of the Experimental Baseball League. Each article is self-contained but builds on the previous one. A reader who finishes all five has a complete picture of what EBL is, how it works, and why it's interesting.

**Series name:** Understanding EBL
**Target length:** 5 articles, each under 750 words
**Audience:** Someone who follows baseball casually or is curious about fantasy sports — no technical knowledge required

## Reading Order

### Part 1: Why One Team Makes Better Competition
*File: ebl-one-team-constraint.md*

The entry point. Explains why limiting the player pool to a single team — the Philadelphia Phillies — creates a better game than drawing from all 30 MLB teams. This is the "why does EBL exist?" article. It establishes the design philosophy that everything else flows from.

**Reader leaves knowing:** EBL is a specialized fantasy league where everyone competes for the same pool of players, creating deeper knowledge requirements and higher stakes for every roster decision.

### Part 2: The $100 Auction Budget Problem
*File: ebl-auction-budget.md*

How the draft works. Every team starts with $100 and bids on players in a live auction. The budget constraint shapes every decision — spend too much early and you're limited later. This article covers strategy, tradeoffs, and the mechanics of real-time bidding.

**Reader leaves knowing:** Teams build their rosters through a live auction with a fixed budget, creating a strategic puzzle that plays out before the season even starts.

### Part 3: The Strange Stats That Actually Win
*File: ebl-scoring-formula.md*

How scoring works, and why it's surprising. Total bases + walks + hit-by-pitches + stolen bases for hitters. Outs recorded for pitchers. These aren't the stats casual fans track, and the weekly leaders are often unexpected.

**Reader leaves knowing:** EBL uses a scoring system based on what players actually contribute, not just the flashy numbers — and the results are often counterintuitive.

### Part 4: From Swing to Screen
*File: ebl-live-stats-pipeline.md*

The technology under the hood. How a home run in Citizens Bank Park shows up in EBL scores within minutes. MLB publishes a live data feed; EBL checks it every minute during games; scores update in real time.

**Reader leaves knowing:** EBL scores update live during games, pulling from MLB's official data feed — and the journey from ballpark to browser is faster and more automated than most people would guess.

### Part 5: Your Roster Fixed Itself Overnight
*File: ebl-auto-roster.md*

What happens when a Phillies player gets traded mid-season. The app notices the next morning, removes the player automatically, and presents replacement options — no manual intervention needed. This article closes the series by showing how the system takes care of itself.

**Reader leaves knowing:** EBL is designed to run smoothly without owners having to monitor every MLB transaction — the app watches the roster so you don't have to.

## Series Arc
The five articles move from **why** (design philosophy) → **strategy** (how you build a team) → **rules** (how scoring works) → **technology** (how live data flows) → **automation** (how the system maintains itself). Each article answers the natural next question a curious reader would have after finishing the previous one.

## Notes
- The five standalone EBL articles not in this series (concurrency, live auction technology, tie scoring, simulation, cron jobs) are deeper technical dives — they assume the reader already understands what EBL is, making this series the right prerequisite
- Link to the series landing page from the EBL topic section on the home page as "New to EBL? Start here →"
- Consider a brief series intro paragraph at the top of Part 1 explaining that this is a 5-part series and linking the full sequence
