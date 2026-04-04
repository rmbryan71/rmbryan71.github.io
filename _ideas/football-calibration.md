# How Do You Decide How Much a Sack Is Worth?

## The Idea
When designing a fantasy football scoring system from scratch, every scoring weight is a decision. Is a sack worth 3 points or 5? Is a tackle worth 1 or 2? The answer to these questions determines whether the game is fair, interesting, and faithful to how real football works. This project calibrated those weights using five years of actual NFL data — not intuition.

## Why It's Interesting
Calibration is a concept that shows up everywhere decisions involve measurement: clinical drug trials, financial models, weather forecasts, machine learning. The principle is always the same — you need a way to check whether your weights and thresholds reflect reality, not just your assumptions. Football scoring makes the concept concrete and low-stakes enough to explain clearly.

## Key Points to Cover
- The problem: scoring weights need to be fair but also create interesting strategic decisions
- The approach: use five years of NFL-wide performance data
- The 75th percentile anchor: an "excellent" performance in any position should score around the same points — calibrated to what 75th percentile actually looks like in the data
- What this prevents: positions where a great game is worth 2 points and positions where a mediocre game is worth 20
- The ongoing adjustment: open questions about specific positions that still need refinement

## Potential Visuals
- Chart showing 75th percentile performance across positions and how scoring aligns to that
- Before/after comparison: intuitive scoring weights vs. data-calibrated weights
- Diagram of the calibration process: gather data → measure → set weights → test → adjust

## Notes / Open Questions
- Good hook: "How much is a sack worth? It depends on how many sacks most players get, and how that compares to what a wide receiver does in a good game."
- Connect to broader calibration concept — this is how evidence-based decisions work in any domain
