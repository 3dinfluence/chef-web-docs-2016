.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``PUT`` method is used to replace the contents of a data bag item with the contents of this request.

This method has no parameters.

**Request**

.. code-block:: xml

   PUT /organizations/ORG_NAME/data/NAME/ITEM

with a request body that looks something like:

.. code-block:: javascript

   {
     "real_name": "Adam Brent Jacob",
     "id": "adam"
   }

where ``id`` is required.

**Response**

The response will return something like the following:

.. code-block:: javascript

   {
     "real_name": "Adam Brent Jacob",
     "id": "adam"
   }

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``401``
     - |response code 401 unauthorized|
   * - ``403``
     - |response code 403 forbidden|
   * - ``404``
     - |response code 404 not found|
   * - ``413``
     - |response code 413 entity_too_large|
