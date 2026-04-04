# Seeing Stories as Maps

## The Idea
Every story has a structure. Linear stories are a line. Branching stories are a map — a network of scenes connected by choices. When you make that map visible, authors can see their story's architecture at a glance: where the branches are, which scenes are hubs, which paths lead to dead ends, how the story flows from beginning to endings. Visualizing the structure changes how you write it.

## Why It's Interesting
Graph visualization is one of those tools that becomes indispensable once you've seen it applied to something familiar. A branching story is naturally a directed graph — nodes are scenes, edges are choices — and the same algorithms that route GPS navigation and organize social networks can automatically lay out a story's structure in a way that makes sense visually. It's a beautiful collision of mathematics and narrative.

## Key Points to Cover
- What a graph is (plain language: nodes connected by edges, like a map of cities connected by roads)
- How a branching story maps to a graph: scenes are nodes, choices are directed edges
- What automatic layout does: algorithms position the nodes so the structure is readable without the author placing each one manually
- What you see when the map is visible: hubs, branches, convergences, dead ends
- Why this changes writing: you can spot structural problems visually that would be invisible in text

## Potential Visuals
- Side-by-side: a branching story as text vs. the same story as a visual graph
- Animation-style diagram: nodes appear as scenes are added, edges appear as choices connect them
- Real graph from Weft showing a story's complete structure (anonymized)

## Notes / Open Questions
- The Dagre layout algorithm (industry standard for graph arrangement) is worth naming but not explaining in depth
- Good hook: "A map of a story looks nothing like a story. But seeing it changes how you write one."
