.. _changelog:

Changelog
==========

[API] v1.2.0
------------------------------
New Features:

- VG patch version match filter

New Data:

- player: guildTag
- player: rankPoints
- player: gamesPlayed

Deprecated:

- schema links
- player lifetimeGold
- player winStreak
- player lossStreak
- player elo_earned_season_4
- player elo_earned_season_5
- player elo_earned_season_6
- player elo_earned_season_7
- player elo_earned_season_8
- player elo_earned_season_9
- player played_aral
- player played_blitz
- player played_casual
- player played_ranked


[API] v1.1.0
------------------------------
New Data:

- New game mode added: blitz_rounds_pvp_casual 
- New game mode added: private_party_blitz_rounds_match

[API] Alpha
-------------------------------
We have opted to separate this API Data changelog version from the internal Gamelocker version to make it more consistent and easy to track for users. Therefore, we have grouped all of the previous changelog entries below this point into one "alpha" version to separate them from the new system above which is restarting at '1.0.0'.

- Data retention period is set to 120 days.
- Future search times are defaulted to now()
- Player shardId is now up-to-date.
- TELEMETRY DATA IS LIVE!!
- New match data reaper: quicker match data availability!
- Player filters: you can now filter by up to six players
- Optimizations and bug fixes

.. toctree::
  :maxdepth: 2
