---
layout: page
title: "Tech Plan"
---
# Change log
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
# List of Challenges
## Process challenges
How to:
1. choose a technology stack
2. choose a web host
3. document a design
4. establish a construction practice
5. track defects
6. test
7. release
8. iterate
9. maintain
10. expand
## Technical challenges
How to:
1. Communicate with and between owners
2. Get roster data from MLB
3. Get performance statistics from MLB
4. Design the database
5. Design the web front end
6. Handle user accounts
7. Allow multi-tenancy (many leagues)
# Phases
## Manual
I'm not planning to do this, it's just a thought experiment.
1. Roster move requests by email
2. Shared Google Sheets workbook
	1. BLE team rosters
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
## Database
1. Roster move requests submitted by email
2. Getting data is manual
3. Calculations done by a database
4. Roster move requests done manually
5. Results served by Google Sheets
## Automated data in
1. Roster move requests submitted by email
2. Getting data is automated
3. Calculations done by a database
4. Roster move requests done manually
5. Results served by Google Sheets
## Automated roster moves
1. Roster move requests submitted by email
2. Getting data is automated
3. Calculations done by a database
4. Roster move requests processed by code
5. Results served by Google Sheets
## Informational web
1. Roster move requests submitted by email
2. Getting data is automated
3. Calculations done by a database
4. Roster move requests processed by code
5. Results served as lists on a website
## Transactional web 
Requires website supports authentication
1. Roster move requests submitted on website
2. Getting data is automated
3. Calculations done by a database
4. Roster move requests processed by code
5. Results served as lists on a website