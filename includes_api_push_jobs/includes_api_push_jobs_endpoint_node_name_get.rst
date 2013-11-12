.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to get the status (``up`` or ``down``) for an individual node.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/ORG_NAME/pushy/node_states/NODE_NAME

**Response**

The response will return something similar to:

.. code-block:: ruby

   {
     "node_name": "FIONA", 
     "status": "down", 
     "updated_at": "Tue, 04 Sep 2012 23:17:56 GMT"
   }

where ``updated_at`` shows the date and time at which a node's status last changed.

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``400``
     - |response code 400 bad request|
   * - ``401``
     - |response code 401 unauthorized|
   * - ``403``
     - |response code 403 forbidden|
   * - ``404``
     - |response code 404 not found|