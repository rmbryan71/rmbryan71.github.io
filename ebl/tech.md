---
layout: page
title: "Tech Plan"
---
# Change log
January 11, 2026 v 0.03 - documentation changes
- removes long-range plans to [future](/ebl/future.md)
- simplifies plan drastically
- replaces list of tech challenges with development plan
- replaces list of process challenges with a process plan
- updates status

January 10, 2026 v 0.02 - documentation changes
- formatting and layout

January 9, 2026 v 0.01 - initial release

# Introduction
The league rules lead to technical requirements.

This document defines my approach and tracks my progress toward providing the league as a service.
# Principles
1. Simplicity : choose less complicated paths 
2. Documentation : write to clarify
3. Decomposition : divide problems
4. Openness : share and listen
5. Fun : Enjoy this

# A manual league
I'm not planning to do this; it's a starting point for thinking about how the league works.  
This is how I would run the league if I had no automation.
{:start="1"}
1. Roster move requests by email
2. Shared Google Sheets workbook
	1. EBL team rosters
	2. Available Phillies
	3. Weekly stats
	4. Leaderboard
	5. Roster move history
3. Sunday night: 
	1. look at MLB website
	2. tally scores by hand
	3. award points
	4. update workbook
	5. process roster moves by hand
	6. send out comms

# Development plan
{:start="1"}
1. Get some data from MLB - [Done](/ebl/40-man-roster.md) 2026-01-10
2. Design a database - [Done](/ebl/db-design.md) 2026-01-11
3. Make the database as designed - [Done](https://github.com/rmbryan71/ebl/blob/main/db-make.py) 2026-01-11
3. Put data in
4. Get data out
5. Get all necessary data from MLB in database
6. Write code to enforce league rules
7. Build web front-end
8. Authenticate users
9. Roster move request form
10. Roster move processing

# Process plan
{:start="1"}
1. choose a technology stack - [Happening](/ebl/lab.md)
2. choose a web host
3. document a design
4. establish a construction practice
5. track defects
6. test
7. release
8. iterate
9. maintain
10. expand