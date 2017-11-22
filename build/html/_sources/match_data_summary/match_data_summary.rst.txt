.. _match_data_summary:

Match Data Summary
==================

Match Object
---------------------------

=================  ==============  ================================
Variable    	   Type            Description
=================  ==============  ================================
type               str             Match
id                 str             Match ID
createdAt          str (iso8601)   Time of Match Played
duration           int             Duration of match in seconds
gameMode           str             Game Mode
patchVersion       str             Version of the game
shardId            str             Region Shard
stats              map             Stats particular to the match
assets             obj             See Match.assets
rosters            obj             See Rosters
rounds             obj             NA
spectators         obj             Spectating participants
titleId            str             Identifies the studio and game
=================  ==============  ================================

**Match.assets (Telemetry Data)**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
type               string          Asset
createdAt          str (iso8601)   Time of Telemtry creation
description        str             NA
filename           str             telemetry.json
id                 str             ID of Asset
contentType        str             application/json
name               map             Telemetry
URL                obj             Link to Telemetry.json file
shardId            str             Region Shard
=================  ==============  ===========================

Rosters Object
---------------------------

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
id                 str             ID of Roster
type               str             Roster
participants       obj             See Participants
stats              obj             Stats particular to rosters
team               obj             See Rosters.team
won                str             Indicates if a roster won
shardId            str             Region Shard
=================  ==============  ===========================

**Rosters.team**

=================  ==============  ================================
Variable    	   Type            Description
=================  ==============  ================================
id                 str             ID of Team or None
name               str             Name of Team or None
type               str             Team
titleId            str             Identifies the studio and game
=================  ==============  ================================

Participants Object
---------------------------

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
actor              str             Hero
id                 str             Same as ID of Roster
player             obj             See Participants.player
stats              map             Stats particular to the participant
type               str             Participants
shardId            str             Region Shard
=================  ==============  ===========================

**Participants.player**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
id                 str             UID of player
name               str             IGN of player
stats              map             Stats particular to a player
type               str             Player
titleId            str             The studio and game title
shardId            str             Region Shard
assets             obj             Same structure as Match.assets
patchVersion       str             Version of the game
=================  ==============  ===========================

.. toctree::
  :maxdepth: 2
