.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``GET`` method is used to return |reporting| data for a |chef client| run. 

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/ORG/reports/nodes/NODE/runs

**Response**

The response will return something like the following:

.. code-block:: javascript

   {
     "node_name" : "pkd01234567",
     "run_id" : "550e4500-e22b-4ad4-a716-446659876500",
     "start_time" : "2014-11-14T23:33:34Z"
     "status" : "started"
   }

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``404``
     - |response code 404 not found|
   * - ``406``
     - Invalid request. The protocol version is incorrect.
