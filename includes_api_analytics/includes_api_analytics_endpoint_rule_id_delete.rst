.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

The ``DELETE`` method is used to delete a rule.

This method has no parameters.

**Request**

.. code-block:: xml

   DELETE /organizations/NAME/rules/ID

This method has no request body.
   
**Response**

The response is similar to:

.. code-block:: javascript

   {
     
   }

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``204``
     - Success.
