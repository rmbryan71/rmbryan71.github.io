---
layout: page
title: "Database Design"
---
# Tables and fields
1. leagues
   2. id
   3. name
   3. year
   3. mlb_team
4. users
   5. id
   6. email
5. teams
   4. id
   5. league_id
   5. user_id
   5. name
3. players
   4. id
   5. name
6. team_player
   7. id
   8. team_id
   8. player_id
4. stats
   5. id
   5. player_id
   6. team_id
   6. date
   7. offense INT
   8. pitching INT
9. points
   10. id
   11. team_id
   12. date
   13. value
   14. type (offense or defense)
10. roster_move_requests
   10. id
   12. team_id
   13. submitted DATETIME
   13. status
11. roster_move_request_players
    12. id
    13. roster_move_request_id
    14. player_id
    15. action (add, drop)
18. audit
    19. id
    20. datetime
    20. league_id
    21. user_id
    20. operation TEXT
    21. old_value
    22. new_value