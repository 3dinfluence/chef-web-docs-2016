.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to return a list of the most recent cookbook versions.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/NAME/cookbooks/_latest

**Response**

For example, if cookbooks ``foo`` and ``bar`` both exist on the |chef server| and both with versions ``0.1.0`` and ``0.2.0``, the response is similar to:

.. code-block:: javascript

  {
    "foo": "http://localhost:4000/cookbooks/foo/0.2.0",
    "bar": "http://localhost:4000/cookbooks/bar/0.2.0"
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
