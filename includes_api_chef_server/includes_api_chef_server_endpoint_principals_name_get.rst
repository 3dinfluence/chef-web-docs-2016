.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The GET method is used to get a list of public keys for clients and users in order to ensure that enough information is present for authorized requests.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /principals/NAME

with a request body that looks something like:

.. code-block:: javascript

   {
     "name": "normal_user",
     "type": "client",
     "public_key": true,
   }

**Response**

The response will return something like the following for a user:

.. code-block:: javascript

   {
     "name": "normal_user",
     "type": "user",
     "public_key": "-----BEGIN PUBLIC KEY-----\n
                   MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCyVPW9YXa5PR0rgEW1updSxygB\n
                   wmVpDnHurgQ7/gbh+PmY49EZsfrZSbKgSKy+rxdsVoSoU+krYtHvYIwVfr2tk0FP\n
                   nhAWJaFH654KpuCNG6x6iMLtzGO1Ma/VzHnFqoOeSCKHXDhmHwJAjGDTPAgCJQiI\n
                   eau6cDNJRiJ7j0/xBwIDAQAB\n
                   -----END PUBLIC KEY-----"
   }

or something like the following for a client:

.. code-block:: javascript

   {
     "name": "client_node",
     "type": "client",
     "public_key": "-----BEGIN PUBLIC KEY-----\n
                   MIEfGVG0GCSqGSIb3DQEBAQUAA4RRFEDCVgftg67j8dgsdfges0rgEW1updSxygB\n
                   wmVpDnHuqwe7/gbh+PmY49EZsfrZSbKgSKy+rxKJHREGJ5tgCtHvYIwVfr2tk0FP\n
                   nhAWJaFH654KpuCNG6x6iMLt5FGH1Ma/VzHnFqoOeSCKHDhmHwJAjGDTPAgCJQiI\n
                   elk8UFCN45Jj0/xBwIDAQAB\n
                   -----END PUBLIC KEY-----"
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
