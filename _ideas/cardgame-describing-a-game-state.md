# How Do You Describe a Game to a Computer?

## The Idea
Before a computer can make a decision in a game, it needs to understand what's happening. That means converting the entire game state — temperatures, equipment, cards in hand, opponents' positions — into a format a neural network can process. The way you describe the situation turns out to matter as much as the algorithm itself.

## Why It's Interesting
This is a universal challenge in AI and data science: representing reality in a way a machine can reason about. It's called "feature engineering," and it's one of the hardest and most creative parts of building AI systems. The card game example is small enough to make the problem concrete and tractable — you can see exactly what information matters and why.

## Key Points to Cover
- The problem: a neural network takes numbers as input, not a picture of a game board
- What needs to be captured: your temperature, your distance from winning, what cards you have, what opponents have
- The challenge: some information isn't available (hidden cards), and some information changes meaning over time (the same hand is strong early, weak late)
- What "feature engineering" means: deciding which aspects of reality to measure and how to measure them
- Why unused information gets zeroed out: the same network plays both auction and battle phases, so auction-only features are set to zero during battle

## Potential Visuals
- Diagram: complex game state → list of numbers → neural network input
- Table showing which features matter in which phase (auction vs. battle)
- Illustration of the "translation" problem: converting qualitative game state to quantitative features

## Notes / Open Questions
- Good analogy: a doctor describing a patient to a specialist — you include the relevant details, omit the irrelevant ones, and the quality of the summary determines the quality of the advice
- Keep the focus on the concept, not the specific implementation
