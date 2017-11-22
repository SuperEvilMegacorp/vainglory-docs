.. _telemetry:

Telemetry
=========

Telemetry provides further insight into a match.


To retrieve Telemetry Data
---------------------------

You start by pulling a list of matches using the matches endpoint.

**HTTP Request**

|  ``GET https://api.dc01.gamelockerapp.com/shards/na/matches``

**Shell:**

.. code-block:: shell

  curl "https://api.dc01.gamelockerapp.com/shards/na/matches" \
  -H "Authorization: Bearer <api-key>" \
  -H "Accept: application/vnd.api+json"

The above commands returns JSON structured like this:

.. code-block:: none

  "data": [
    {
      "type": "match",
      "id": "f5373c40-0aa9-11e7-bcff-0667892d829e",
      "attributes": {
        "createdAt": "2017-03-17T00:38:00Z",
        "duration": 259,
        "gameMode": "blitz_pvp_ranked",
        "patchVersion": "2.9",
        "shardId": "na",
        "stats": {
          "endGameReason": "victory",
          "queue": "blitz_pvp_ranked"
        },
        "titleId": "semc-vainglory"
      },
      "relationships": {
        "assets": {
          "data": [
            {
              "type": "asset",
              "id": "b900c179-0aaa-11e7-bb12-0242ac110005"
            }
          ]
        },
        "rosters": {
          "data": [
            {
              "type": "roster",
              "id": "b8f6640a-0aaa-11e7-bb12-0242ac110005"
            },
            {
              "type": "roster",
              "id": "b8f65271-0aaa-11e7-bb12-0242ac110005"
            }
          ]
        },
      }
    }
  ]

You need to look for an ``Assets`` JSON node which points to telemetry. Check for the following in the response:

.. code-block:: none

  "relationships": {
    "assets": {
      "data": [
        {
          "type": "asset",
          "id": "b900c179-0aaa-11e7-bb12-0242ac110005"
        }
      ]
    }
  }

Once you have located this ID, you now have to search for the following JSON segment in the response object. The following response object will provide you a link to the Telemtry data

.. code-block:: none

  {
    "type": "asset",
    "id": "b900c179-0aaa-11e7-bb12-0242ac110005",
    "attributes": {
      "URL": "https://gl-prod-us-east-1.s3.amazonaws.com/assets/semc-vainglory/na/2017/03/17/00/43/b900c179-0aaa-11e7-bb12-0242ac110005-telemetry.json",
      "contentType": "application/json",
      "createdAt": "2017-03-17T00:43:22Z",
      "description": "",
      "filename": "telemetry.json",
      "name": "telemetry"
    }
  }

You can download the data with following commands. Please note that you do not need API Key to get this data.

.. code-block:: shell

  curl "https://gl-prod-us-east-1.s3.amazonaws.com/assets/semc-vainglory/na/2017/03/17/00/43/b900c179-0aaa-11e7-bb12-0242ac110005-telemetry.json" \
  -H "Accept: application/vnd.api+json"

This request will return you a response as follows:

.. code-block:: none

  {
    "time": "2017-02-18T06:37:15+0000",
    "type": "DealDamage",
    "payload": {
      "Team": "Left",
      "Actor": "*Ringo*",
      "Target": "*Turret*",
      "Source": "Unknown",
      "Damage": 405,
      "Delt":  613,
      "IsHero": 1,
      "TargetIsHero": 0
    }
  }



.. toctree::
  :maxdepth: 2
