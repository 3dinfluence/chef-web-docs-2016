.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``DELETE`` method is used to delete an environment.

This method has no parameters.

**Request**

.. code-block:: xml

   DELETE /organizations/ORG_NAME/environments/NAME

**Response**

The response will return the |json| for the environment that was deleted, similar to:

.. code-block:: javascript

   {
     "name":"backend",
     "description":"",
     "cookbook_versions":{},
     "json_class":"Chef::Environment",
     "chef_type":"environment",
     "default_attributes":{},
     "override_attributes":{}
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