# Teaching a Computer to Play a Game It's Never Seen Before

## The Idea
Writing a computer player (a "bot") for a game usually means writing a long list of rules: "if you see this, do that." But hand-coded rules break whenever something unexpected happens. This project replaced the rulebook with a neural network that learned to play by watching thousands of games — and it figured out things the human designer hadn't thought of.

## Why It's Interesting
It's a concrete, small-scale example of how machine learning actually works — not the abstract version people usually hear about, but a real project where you can see exactly what improved and why. The jump from "300 lines of hand-coded rules" to "a model that learned its own rules" captures something important about how AI systems are different from traditional software.

## Key Points to Cover
- What a "bot" is: a computer player that follows programmed instructions
- The problem with hand-coded bots: they're rigid, they fail in unexpected situations, they need manual retuning every time the game changes
- What a neural network does differently: it watches outcomes (win/lose) and learns which decisions led to wins
- What the AI discovered that humans hadn't programmed: unexpected equipment combinations that turn out to be dominant strategies
- What "retraining" means: if you change the game rules, you just play more games — no manual retuning needed

## Potential Visuals
- Side-by-side: hand-coded rule tree vs. neural network diagram (conceptual, not technical)
- Learning curve chart: bot win rate over thousands of training games
- Flowchart comparing "if-then" bot decision vs. "learned value" bot decision

## Notes / Open Questions
- The key insight to land: traditional software tells the computer what to do; machine learning lets the computer figure out what to do
- Avoid deep ML jargon — "it learns from outcomes" is enough
