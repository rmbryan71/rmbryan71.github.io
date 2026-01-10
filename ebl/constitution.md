---
layout: page
title: "Constitution"
---
# Change log
January 10, 2026: v 0.04 - documentation changes
- overhauls wording throughout
- updates formatting for readability
- work in progress

January 9, 2026: v 0.04 - overhaul, move to web
- removes implementation section to [tech plan](/ebl/tech.html)
- removes irrelevant conversational tangents
- removes communications plan to [comms plan](/ebl/comms.html)

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
The Experimental Baseball League includes:
1. Phillies players only.
2. A live auction for players.
3. Scores tallied weekly.

# General Rules
These are the current league rules:
1. Participation is free, and there is no prize money.
3. There are 8 teams in our league.
4. Each team has 4 roster spots.
5. Pitching is measured by Innings Pitched.
7. Offense is measured by the sum of Total Bases + Walks + HBP + Steals.

# Scoring
Every week, points are awarded to teams as follows:
2. Team with most pitching that week gets 10 points.
3. Team with next most pitching that week gets 8 points.
4. Team with next most pitching that week gets 4 points.
5. Team with most offense that week gets 10 points.
6. Team with next most offense that week gets 8 points.
7. Team with next most offense that week gets 4 points.
8. Partial weeks at the beginning of the year, the all-star break, and the end of the year all get the same points awarded as full weeks.
9. If a pitcher gets on base, that counts as offense.
10. If a hitter gets pitching outs, those count.

## Ties

1. All teams tied for a position get all the points for that spot as if there were no tie.
2. No points are awarded for second place if two teams tie for first place.
3. No points are awarded for third place if two or more teams tie for second place.
4. If there's a three-way tie for first place, all three teams get first place points, and there are no other points awarded.
5. If there's a six-way tie for third, all six teams get third place points.

# Rosters
1. Only players on the Phillies roster can be on teams in our league.
2. If a player on your team gets traded away from the Phillies, retires, dies, gets picked up by another team on waivers, or leaves the organization for any reason, you have an empty roster spot to fill.
3. There is specifically no remedy for suspensions or injuries. Those do not create empty roster spots. 
4. You do not have to fill empty roster spots immediately, or ever.
5. Phillies players at any level of the majors and minors are eligible to be on teams, but only major league production counts.
6. If you have a player that gets sent down or called up, you don't have to do anything.
7. If you want all pitchers, all hitters, or any mix of hitters and pitchers, that's fine. It's entirely up to you.
# Roster moves
1. You can make a maximum of 1 roster move attempt per week.
2. Even if you have more than one open roster spot, you only get one roster move attempt per week.
3. Roster moves happen Sunday night after points are awarded.
4. Your roster move attempt includes the name of the player you want to drop and the name of the player you want to add.
5. You can't submit a roster move for a player on another team in our league in the hope that the player gets dropped before your turn in the roster move process.
6. Teams with empty roster spots go first in the roster move process. If more than one team has an empty roster spot, the lower-ranking teams go first.
7. Aside from teams with empty roster spots, roster move attempts are processed in reverse order of the current league standings. In the case of ties in the league standings, roster move attempts will happen between the tied franchises randomly.
8. If the player you attempt to add isn't available when it comes to your turn in the roster moves process, nothing happens. You don't lose the player you tried to drop. You can try again next week.
9. When the Phillies add a player, they become available at the end of week they are acquired.
11. If there's a tie in the standings and two teams try to acquire the same player, the player is assigned randomly.
12. There's no trading players between teams.

# The auction
1. This will be a Zoom call at 6:00 PM on Sunday, March 22, 2026.
2. Every team gets $100 to field their team.
3. All bids are whole-dollar values, no pennies.
4. You must fill all 4 roster spots on your team during the auction.
5. Owners will nominate players to be auctioned. 
6. When you nominate a player, you automatically start the bidding for that player at $1. 
7. You must save enough money to be able to fill all your roster spots. You cannot spend all your money without filling all of your roster spots.
7. When it's your turn to nominate, you just say what player you want to come up for auction next. 
8. Owners will nominate in a random order that's not decided until the auction starts.
9. At the end of each player auction, we will know which team in our league that player is on and how much the owner paid for them.
10. If you have extra money left over at the end of the auction, that's fine, it wasn't really money anyway.
11. We will have exactly 32 auctions.
12. If an auction starts with two owners simultaneously bidding $97 for a player, the older owner gets the player.
13. Otherwise, it's an open auction, so owners just shout out how much they're willing to pay and that's the going price.
14. Ownership of players is for the 2026 season only.

# Privacy
1. Nobody should have to reveal who they are in order to participate. 
2. Everything should be anonymized and free of personally identifiable information.

# Audit trail
1. The league implementation has to have a detailed audit trail of everything that happens in the league, including roster move attempts, statistic updates, point awards, data corrections, and, later, logins and anonymized owner actions.
2. The audit trail has to be available to everyone in the league all the time.