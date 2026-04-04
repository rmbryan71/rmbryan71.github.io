# The Jobs That Run While Everyone Sleeps

## The Idea
Every Sunday at 4 AM, with no one watching, EBL calculates the week's scores, processes every roster move request, and updates the standings — automatically. These scheduled tasks (called cron jobs) are a fundamental part of how software keeps running without a human at the wheel.

## Why It's Interesting
There's an entire invisible layer of software that runs the internet while everyone sleeps. Bank statements, email digests, weather forecasts, backup systems — all scheduled tasks. EBL's 4 AM Sunday run is a small, relatable example of a pattern that shows up everywhere in computing. It's also a story about fairness: doing all the roster moves at once, in a specific order, so no one gets an advantage from being awake at the right moment.

## Key Points to Cover
- What a cron job is: a task scheduled to run automatically at a specific time
- EBL's three scheduled tasks: nightly roster check (3:30 AM), weekly scoring (4:00 AM Sunday), roster move processing (4:10 AM Sunday)
- Why 4 AM? No games are happening; the day's stats are final
- The fairness logic: lower-ranked teams get first pick on roster moves — this only works when all moves process at the same time
- What happens if the job fails: stakes are real (wrong standings), so logging and error-handling matter

## Potential Visuals
- Weekly calendar showing when each cron job fires relative to the baseball schedule
- Flowchart of Sunday morning: score calculation → standings update → roster move processing → notifications sent
- Simple clock diagram showing 3:30 AM / 4:00 AM / 4:10 AM sequence

## Notes / Open Questions
- The time zone detail (Eastern Time, America/New_York) is a small but important point — a job that fires at 4 AM ET runs at 1 AM PT; DST can cause bugs
- Good hook: "Your fantasy team's fate was decided while you slept"
