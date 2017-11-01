.. _teams:

Teams
=====

Team objects contain aggregated lifetime information about each Team.

Get a collection of Teams
---------------------------

This endpoint retrieves a collection of up to 6 teams.

*Important - Team resources are not yet available in the API.*

**HTTP Request**

|  ``GET https://api.dc01.gamelockerapp.com/teams``

**URL Parameters**

=================  ==============  =============================================================
Parameter    	   Default         Description
=================  ==============  =============================================================
filter[teamNames]  none            Filters by team name. Usage: filter[teamNames]=team1
filter[teamIds]    none            Filter by team id. Usage: filter[teamIds]=12345
=================  ==============  =============================================================

**Shell:**

.. code-block:: shell

  curl "https://api.dc01.gamelockerapp.com/shards/na/teams?filter[teamNames]=team1" \
  -H "Authorization: Bearer <api-key>" \
  -H "Accept: application/vnd.api+json"



Get a Single Team
---------------------------

This endpoint retrieves a specific team.

**HTTP Request**

|  ``GET https://api.dc01.gamelockerapp.com/teams/<ID>``

**URL Parameters**

|  Parameter: ID
|  Description: The ID of the team to retrieve


**Javascript:**

.. code-block:: javascript

	  curl "https://api.dc01.gamelockerapp.com/teams/<ID>" \
	  -H "Authorization: Bearer <api-key>" \
	  -H "Accept: application/vnd.api+json"

	  The above command returns JSON structured like this:
	  
	{
	  "id": 2,
	  "name": "Max",
	  "breed": "unknown",
	  "fluffiness": 5,
	  "cuteness": 10
	}


Links (Coming Soon!)
---------------------------

This endpoint checks to see if a link object exists for a given code.

**HTTP Request**

|  ``GET https://api.dc01.gamelockerapp.com/link``

**Javascript:**

.. code-block:: javascript

	curl -XPOST "https://api.dc01.gamelockerapp.com/shards/na/link/{player_id}" \
  -H "Authorization: Bearer <api-key>" \
  -H "Accept: application/vnd.api+json"



Post a Link
---------------------------

This endpoint creates a PlayerLink object if the verification code matches the one provided by the game.

**HTTP Request**

|  ``POST https://api.dc01.gamelockerapp.com/link/{player_id}``

**Javascript:**

.. code-block:: javascript

	curl -XPOST "https://api.dc01.gamelockerapp.com/shards/na/link/{player_id}" \
  -H "Authorization: Bearer <api-key>" \
  -H "Accept: application/vnd.api+json"


Player Link
----------------

**Javascript:**

.. code-block:: javascript

	{
  "attributes": {
      "playerId": "fb374a7b-78be-4fcc-83ed-6a532a8a6f55",
      "shardId": "na",
      "titleId": "semc-vainglory"
  },
  "id": "2454e5ac-0a69-4468-ad12-8616f066e817",
  "type": "playerLink"
	}

.. toctree::
  :maxdepth: 2
