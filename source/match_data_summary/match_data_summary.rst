.. _match_data_summary:

Match Data Summary
==================

Special thanks to Kashz for helping to create this! GitHub: iAm-Kashif

Match Object
---------------------------

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
Type               str             Match
ID                 str             Match ID
createdAt          str (iso8601)   Time of Match Played
duration           int             Time of match in seconds
gameMode           str             Game Mode
patchVersion       str             Version of API
shardID            str             Match Shard
stats              map             See Match.stats
assets             obj             See Match.assets
rosters            obj             See Rosters
=================  ==============  ===========================


**Match.stats (End of game statistics)**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
endGameReason      str             "Victory" or "Defeat"
queue              str             Game Mode
=================  ==============  ===========================


**Match.assets (Telemetry Data)**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
Type               string          asset
createdAt          str (iso8601)   Time of Telemtry creation
description        str             " "
filename           str             telemetry.json
id                 str             ID of Asset
contentType        str             application/json
name               map             telemetry
url                obj             Link to Telemetry.json file
=================  ==============  ===========================


Rosters Object
---------------------------

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
id                 str             ID of Roster
type               str             Roster
participants       obj             See Participants
stats              obj             See Rosters.stats
team               obj             See Rosters.team
=================  ==============  ===========================


**Rosters.stats**

=================  =======================================
Variable    	   Type          
=================  =======================================
acesEarned         int           
gold               int  
heroKills          int           
krakenCaptures     int  
side               Either "right/red" or "left/blue"  
turretKills        int  
turretRemaining    int  
=================  =======================================


**Rosters.team**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
id                 str             ID of Team or None
name               str             Name of Team or None
type               str             team
=================  ==============  ===========================

Participants Object
---------------------------

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
actor              str             Hero
id                 str             Same as ID of Roster
player             obj             See Participants.player
stats              map             See Paticipants.stats
type               str             participants
=================  ==============  ===========================

**Participants.player**

=================  ==============  ===========================
Variable    	   Type            Description
=================  ==============  ===========================
id                 str             UID of player
name               str             IGN of player
stats              map             See Participants.player.stats
type              str             palyer
=================  ==============  ===========================

**Particpants.stats**

======================  =================================
Variable    	        Type          
======================  =================================
assists	                int
crystalMineCaptures    	int
deaths	                int
farm                	int
firstAfkTime        	int: -1 for no AFK
goldMineCaptures	    int
itemGrants          	map of {itemsBought : int}
itemSells	            map of {itemsSold : int}
itemUses	            map of {itemsUsed : int}
items	                list of final build (Len: 6)
jungleKills          	int
karmaLevel	            int
kills	                int
krakenCaptures         	int
level	                int
minionKills         	int
nonJungleMinionKills	int
skillTier             	int
skinKey             	str
turretCaptures	        int
wentAfk	                bool
winner              	bool
======================  =================================


**Particpants.player.stats**

======================  =================================
Variable    	        Type          
======================  =================================
level	                int
lifetimeGold         	float
lossStreak            	int
played               	int
played_ranked          	int
winStreak               int
wins                	int
xp	                    int
======================  =================================


.. toctree::
  :maxdepth: 2
