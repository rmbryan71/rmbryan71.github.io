# How Computers Solve Sudoku (and What That Teaches Us About Thinking)

## The Idea
The most elegant computer approach to solving Sudoku isn't to try every possible number in every cell. It's to eliminate impossible options first — the same way a human expert would. That approach, called constraint propagation, is one of the most powerful ideas in artificial intelligence, and Sudoku makes it easy to understand.

## Why It's Interesting
Constraint propagation is how a lot of real AI works: instead of searching all possibilities, you use known rules to eliminate the ones that can't be right, then search the much smaller remaining space. It's more like deduction than guessing. Seeing it work on a puzzle people already know makes the concept immediately tangible.

## Key Points to Cover
- How most people think computers solve Sudoku: try every number until one works (brute force)
- How good solvers actually work: logic first, guessing only as a last resort
- What "constraint propagation" means: each cell you fill in eliminates options in related cells
- The cascade effect: one logical deduction often triggers several others
- When guessing is still needed: the hardest puzzles require a guess after logic runs out, then backtrack if wrong

## Potential Visuals
- Step-by-step diagram showing a single constraint propagation cascade
- Comparison: search space before and after constraint propagation
- Flowchart: propagate constraints → check if solved → guess if needed → backtrack if wrong

## Notes / Open Questions
- Good hook: "Computers don't solve Sudoku by trying every possibility. The best approach is closer to how a human expert thinks."
- The "backtracking" concept — trying a guess, discovering it's wrong, and undoing it — is intuitive and worth including
