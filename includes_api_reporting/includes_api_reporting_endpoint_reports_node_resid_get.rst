.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``GET`` method is used to return a list of what changed during the |chef client| run for the specified resource. 

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/ORG/reports/nodes/NODE/runs/RUNID/RESID

**Response**

The response is similar to:

.. code-block:: javascript

   {
     resource_detail :
     {
       "content_delta" : string
     }
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