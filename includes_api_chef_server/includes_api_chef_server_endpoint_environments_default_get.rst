.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to get information about the ``_default`` environment on the |chef server|.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/NAME/environments/_default

**Response**

The response is similar to:

.. code-block:: javascript

   {
     "name": "_default",
     "description": "The default Chef environment",
     "json_class": "Chef::Environment",
     "chef_type": "environment",
     "default_attributes": {
   
     },
     "override_attributes": {
   
     },
     "cookbook_versions": {
   
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
   * - ``401``
     - |response code 401 unauthorized|
   * - ``403``
     - |response code 403 forbidden|
   * - ``404``
     - |response code 404 not found|
