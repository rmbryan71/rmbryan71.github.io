# From Swing to Screen: How a Baseball Stat Reaches Your App

## The Idea
When a Phillies player hits a home run, EBL users see their score update within minutes — sometimes while the ball is still in the air. How does that happen? This article traces the journey of a single stat from the ballpark to your browser.

## Why It's Interesting
Most people have no idea there's a live data pipeline running behind every sports app. MLB publishes a free, publicly accessible stats feed that developers can query. EBL checks it every minute during the season. Understanding this pipeline demystifies how "live" sports data actually works — it's not magic, it's a very fast game of telephone.

## Key Points to Cover
- MLB publishes live game data through an API (a structured data feed any app can read)
- EBL checks that feed every minute during game hours
- What data comes back: batting stats, pitching stats, game status
- How the app decides what's "new" and stores only changes
- The difference between a game in progress vs. final — and why that matters for scoring

## Potential Visuals
- Flow diagram: ballpark → MLB servers → EBL app → user's screen
- Timeline showing how quickly a stat appears after the event happens
- Simple illustration of what an API response looks like (humanized, not code)

## Notes / Open Questions
- Mention that in-progress game stats are treated differently (cached) than final games to avoid re-fetching
- Home runs and 20-out pitching games trigger special notifications — good hook
