# Your Roster Fixed Itself Overnight

## The Idea
When a Phillies player gets traded mid-season, EBL owners don't need to do anything. The app notices the next morning, removes the player automatically, and presents the owner with replacement options — no manual intervention required.

## Why It's Interesting
This is a great example of software that watches the world and reacts to it. The app compares the current MLB roster against what it knew yesterday, spots the difference, and takes action. It's the same pattern behind things like bank fraud alerts, package tracking notifications, and smart home automations. The baseball context makes it easy to understand; the concept generalizes everywhere.

## Key Points to Cover
- The problem: players get traded, injured, or cut mid-season — a real thing that happens
- How the app checks the MLB roster every morning at 3:30 AM
- What it does when it finds a mismatch: creates a replacement request, offers 3 options
- The Sunday processing run: when all pending moves execute in fairness order
- The owner's experience: wake up to a notification, pick a replacement, done

## Potential Visuals
- Timeline diagram: trade happens → morning check → owner notified → Sunday processing → new player on roster
- Flowchart of the roster-check logic: compare lists → find differences → create request
- Before/after roster card showing a player removed and replaced

## Notes / Open Questions
- The fairness ordering (lower-ranked teams get priority) is worth mentioning
- This is also a story about automation reducing burden on users — a recurring theme in good software design
