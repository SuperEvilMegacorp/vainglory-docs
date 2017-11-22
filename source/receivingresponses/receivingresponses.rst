.. _receivingresponses:

Receiving Responses
====================

Payload
--------

All Server responses contain a root JSON object.

Every response will contain at least one of the following top-level members:

* ``data`` : The response's “primary data”
* ``errors`` : An array of error objects

A response may contain any of these top-level members:

* ``links``: A links object related to the primary data.
* ``included``: An array of resource objects that are related to the primary data and/or each other (“included resources”).
* ``meta``: not currently used.

If a document does not contain a top-level data key, the included member will not be present either.

.. code-block:: none

  {
    "data": {
      "type": "match",
      "id": "fe793a44-d7da-11e6-b845-0671096b3e30",
      "attributes": {
        // ... this matches attributes
      },
      "relationships": {
        // ... this matches relationships
      },
      "links": {}
    },
    "included": [
      {...},
      ...
    ],
    "links": {}
    "meta": {}
  }

.. toctree::
  :maxdepth: 2
