.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``admin``
     - Use to specify whether the |chef client| is an API client.
   * - ``chef_server``
     - |chef_server_url|
   * - ``complete``
     - Use to specify if this resource defines a |chef client| completely. When ``true``, any attribute not specified by this resource will be reset to default attribute values.
   * - ``name``
     - The name of the |chef client|.
   * - ``output_key_format``
     - Use to specify the format of a public key. Possible values: ``pem``, ``der``, or ``openssh``. Default value: ``openssh``.
   * - ``output_key_path``
     - Use to specify the path to the location in which a public key will be written.
   * - ``raw_json``
     - The |chef client| as |json| data. For example:
       
       .. code-block:: javascript
       
          {
          "clientname": "client_name",
          "orgname": "org_name",
          "validator": false,
          "certificate": "-----BEGIN CERTIFICATE-----\n
                          ...
                          1234567890abcdefghijklmnopq\n
                          ...
                          -----END CERTIFICATE-----\n",
          "name": "node_name"
          }
   * - ``source_key``
     - Use to copy a public key, but apply a different ``format`` and ``password``. Use in conjunction with ``source_key_pass_phrase``` and ``source_key_path``.
   * - ``source_key_pass_phrase``
     - The pass phrase for the public key. Use in conjunction with ``source_key``` and ``source_key_path``.
   * - ``source_key_path``
     - The path to the public key. Use in conjunction with ``source_key``` and ``source_key_pass_phrase``.
   * - ``validator``
     - Use to specify if the |chef client| is a |chef validator|.
