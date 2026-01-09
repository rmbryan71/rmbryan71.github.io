January 8, 2026
version 0.03
# Change log
January 8, 2026: v 0.03 - documentation changes
- overhauls the auction
- removes unhelpful strategy note from roster section
- adds special case to roster move processing order
- clarifies how empty roster spots can happen
- specifies lack of remedy for injuries or suspensions
January 7, 2026: v 0.02 - documentation changes
- adds stolen bases to offense
- changes auction order to nominations
- specifies whole dollar amounts for bids
- overhauls ties
- adds missing headings
- adds future features section
- changes roster moves from daily to weekly
- specifies that ties during roster moves are handled randomly
- adds note about documentation to implementation section
- adds privacy requirement to implementation section
- adds audit trail requirement to implementation section
- adds communication plan to implementation section
January 6, 2026: v 0.01 - initial release
# Introduction
I'm launching a fantasy baseball service for the 2026 season with:
1. Phillies players only.
2. A live auction for players.
3. Scores tallied weekly.
Those core features are unlikely to change.
Everything else is experimental.
I am absolutely open to ideas and questions.
Please send ideas and questions.
# General Rules
These are the current league rules:
Participation is free.
There is no prize money.
There are 8 team franchises in the league.
Each team has 4 roster spots.
Pitchers compete based on Innings Pitched. 
That's it. Outs are all that matter.
Hitters compete based on Total Bases + Walks + HBP + Steals (aka "Offense"). 
It doesn't matter how you get on base.
# Scoring
Every week, points are awarded to teams as follows:
Team with most Innings Pitched that week gets 10 points
Team with next most Innings Pitched that week gets 8 points
Team with next most Innings Pitched that week gets 4 points
Team with most Offense that week gets 10 points
Team with next most Offense that week gets 8 points
Team with next most Offense that week gets 4 points
Partial weeks at the beginning of the year, the all-star break, and the end of the year all get the same points awarded as full weeks.
If a pitcher hits and gets on base, that counts.
If a hitter pitches and get outs, those count.
## Ties
All teams tied for a position get all the points for that spot as if there were no tie.
No points are awarded for second place if two teams tie for first place.
No points are awarded for third place if two teams tie for second place.
If there's a three-way tie for first place, all three get first place points and there are no other points awarded.
If there's a six-way tie for third, all six teams get third place points.
# Rosters
Only players on the Phillies roster can be on teams in our league.
If a player on your team gets traded away from the Phillies, retires, dies, gets picked up by another team on waivers, or leaves the organization for any reason, you have an empty roster spot to fill.
There is specifically no remedy for suspensions or injuries. Those do not create empty roster spots. 
You do not have to fill empty roster spots immediately, or ever.
Phillies players at any level of the majors and minors are eligible to be on teams, but only major league production counts.
If you have a player that gets sent down or called up, you don't have to do anything.
If you want all pitchers, all hitters, or any mix of hitters and pitchers, that's fine.
It's entirely up to you.
# Roster moves
You can make a maximum of 1 roster move attempt per week.
Even if you have more than one open roster spot, you only get one roster move attempt per week.
Roster moves happen Sunday night after points are awarded.
Your roster move attempt includes the name of the player you want to drop and the name of the player you want to add.
You can't submit a roster move for a player on another team in our league in the hope that the player gets dropped before your turn in the roster move process.
Teams with empty roster spots go first in the roster move process. If more than one team has an empty roster spot, the lowest-ranking teams go first.
Aside from teams with empty roster spots, roster move attempts are processed in reverse order of the current league standings. In the case of ties in the league standings, roster move attempts will happen between the tied franchises randomly.
If the player you attempt to add isn't available when it comes to your turn in the roster moves process, nothing happens. You don't lose the player you tried to drop. You can try again next week.
When the Phillies add a player, they become available at the end of week they are acquired.
That week's roster move process will put them on the lowest-ranking team that requests them.
If there's a tie in the standings and two teams try to acquire the same player, the player is assigned randomly.
There's no trading players between teams.
# The auction
This will be a Zoom call at 6:00 PM on Sunday, March 22, 2026.
Spring training will be wrapping up, but we should have a pretty good idea of who's who by then.
If you want to run a franchise, but can't attend the auction, let me know and I'll work on a way to make that happen.
Every team gets $100 to field their team.
All bids are whole-dollar values, no pennies.
You must fill all 4 roster spots on your team during the auction.
Owners will nominate players to be auctioned and start the bidding for that player. 
When you nominate a player, you automatically start the bidding for that player at $1. You must save enough money to be able to fill all your roster spots. You cannot spend all your money without filling all of your roster spots.
When it's your turn to nominate, you just say what player you want to come up for auction next and where you want to start the bidding. Owners will get a chance to nominate in a random order that's not decided until the auction starts.
I'll be the auctioneer, plus I'll be bidding on players for my own team, and I'll be handling bids for people who can't make the call. Should be interesting.
At the end of each player auction, we will know which team in our league that player is on and how much the owner paid for them.
If you have extra money left over at the end of the auction, that's fine, it wasn't really money anyway.
We will have exactly 32 auctions.
If an auction starts with two owners simultaneously bidding $97 for a player, the older owner gets the player.
Otherwise, it's an open auction, so owners just shout out how much they're willing to pay and that's the going price.
Ownership of players is for the 2026 season only.
# Implementation
How is this going to happen? I don't know, but I'm going to document the process in a blog at least and probably, given my history, a whole suite of requirements documents, decision documents, design documents, process flow diagrams, on-line help, test plans, and at least one matrix of some kind.
One purpose of this league is to serve as a programming and web development challenge for me.
My goal is to have an easy-to-use website that shows our standings, rosters, stats, and handles everything from roster moves to smack talk.
I'll build that as we go, so keep a flexible mindset.
If I have to start with shared text files and email, I will.
We might try a few different approaches before we find something that works, so keeping the rules simple is a key feature. If something doesn't work for you, or you think it could be better, please, I'm begging you, let me know. 
I need feedback.
For example, we need a name for the league.
## Communications plan
Owners should all have the same access to news about the league, changes to the rules, updates to the website, scores, and player transactions. 
Currently, I'm texting people links to PDFs I host on my website. Soon, I'd like to have a better system in place. People should be able to specify how they want to be contacted and change their minds later. I'm open to ideas on how to do that and maintain privacy at the same time.
## Privacy
Nobody should have to reveal who they are in order to participate. Everything should be anonymized and free of personally identifiable information. When it comes time to implement logins and security, I'll find a way to establish identity without violating privacy.
## Audit trail
The implementation has to have a detailed audit trail of everything that happens in the league, including roster move attempts, statistic updates, point awards, data corrections, and, later, logins and anonymized owner actions.
The audit trail has to be available to everyone in the league all the time.
# Future
Features I want to include, but will wait until later to plan.
- Once roster moves get automated, they should be available daily.
- Roster move attempts can specify multiple target players to add. If the top player isn't available, other players can be considered in order.
- Every way a batter can reach base should be counted. Catcher’s interference. Errors. Hit by pitch. Dropped third strike. Fan interference. Fielder's choice maybe.
- It would be nice to have a list of available players that haven't been auctioned off yet so that we can see who's available. 