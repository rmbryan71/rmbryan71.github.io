---
layout: page
title: "Lab notebook"
---
# Introduction
This is where I keep track of what I'm thinking and doing.

# January 11, 2026
Worked on documentation. Drastically simplified the [tech plan](/ebl/tech.md).  
It's time to make a [database](https://en.wikipedia.org/wiki/Database).  
All of my experience is with [Postgres](https://en.wikipedia.org/wiki/PostgreSQL).  
In this case, though, I'm going to start with [SQLite](https://en.wikipedia.org/wiki/SQLite) because:
1. It doesn't require a server.
2. It's simpler.
3. It's similar enough to Postgres that I'll be able to write SQL for it.

I'm going to invest an hour into installing and working with SQLite.  
An hour? More like, what, 8 minutes?  
That could not _possibly_ have been any easier.  
Cool. Okay, now what?  
[Database design](https://en.wikipedia.org/wiki/Database_design), probably.  
I'm working [here](/ebl/db-design.md).  
8:55 PM - Design is complete. I have a [db-make.py](https://github.com/rmbryan71/ebl/blob/main/db-make.py) that creates all the tables, fields, and foreign key constraints.  
Do I want my db file in git? Oh, it's binary, probably not.  

# January 10, 2026
I'm removing the .pdf's I used to launch the league before moving to the web.  
The website is okay for now.  
The rules have stabilized enough.  
I'm going to put an hour into trying to write a Python program to fetch the Phillies 40-man roster from the MLB API and write that data to a local text file that gets served to the website. No database. Wipe any previous results, replace with the new results.  
1. I started a [fresh Python project](https://github.com/rmbryan71/ebl).
2. I registered for an MLB Advanced Media API account. They're going to review my application.  
3. I found a [Python wrapper for the MLB API](https://github.com/toddrob99/MLB-StatsAPI).
4. I made a request and got data. Didn't need an account.
5. I got the [current Phillies 40-man roster](https://www.mlb.com/phillies/roster/40-man) and [wrote it to a file](/ebl/40-man-roster.md).  

That was easy.