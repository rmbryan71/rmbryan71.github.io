# Where Fantasy Football Numbers Come From

## The Idea
During an Eagles game, somewhere a server is pulling play-by-play data from the NFL's official data feed, parsing it, computing scores, and updating a leaderboard in real time. Most fantasy football players have no idea this infrastructure exists. This is the data pipeline behind the game — and it's more interesting than it sounds.

## Why It's Interesting
Real-time sports data is a surprisingly complex engineering problem. Play-by-play data arrives in bursts, needs to be parsed and interpreted, and then calculated into meaningful statistics on the fly. The NFL data ecosystem — which includes free, open-source datasets that anyone can access — is one of the richest public data resources available. Understanding it opens up a world of analysis that most fans don't know exists.

## Key Points to Cover
- Where the data comes from: nflverse, a free open-source NFL data project
- What play-by-play data contains: every play, every player, every outcome
- How snap count data works: a separate feed tracking which players were on the field
- The pipeline: data comes in → gets parsed → scoring formulas run → database updates → leaderboard refreshes
- What you can do with this data yourself: the same data is available to anyone, for free

## Potential Visuals
- Flow diagram: NFL game → data feed → parsing → scoring calculation → leaderboard
- Sample of what play-by-play data looks like (humanized, not raw JSON)
- Diagram showing the different data streams: play-by-play, snap counts, advanced metrics

## Notes / Open Questions
- The nflverse project is worth mentioning — it's a community resource that makes this kind of project accessible
- Good hook: "The number next to your player's name in a fantasy app didn't calculate itself. Here's what actually happened."
