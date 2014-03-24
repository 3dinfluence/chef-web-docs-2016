.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``admin``
     - |admin client|
   * - ``chef_server``
     - |chef_server_url|
   * - ``complete``
     - Use to specify if this resource defines a user completely. When ``true``, any attribute not specified by this resource will be reset to default attribute values.
   * - ``email``
     - The email address for the user.
   * - ``external_authentication_uid``
     - xxxxx
   * - ``name``
     - The name of the user.
   * - ``output_key_format``
     - Use to specify the format of a public key. Possible values: ``pem``, ``der``, or ``openssh``. Default value: ``openssh``.
   * - ``output_key_path``
     - Use to specify the path to the location in which a public key will be written.
   * - ``raw_json``
     - The |chef client| as |json| data. For example:
       
       .. code-block:: javascript
       
          {
            "name": "Robert Forster"
          }
   * - ``recovery_authentication_enabled``
     - xxxxx
   * - ``source_key``
     - Use to copy a public or private key, but apply a different ``format`` and ``password``. Use in conjunction with ``source_key_pass_phrase``` and ``source_key_path``.
   * - ``source_key_pass_phrase``
     - The pass phrase for the public key. Use in conjunction with ``source_key``` and ``source_key_path``.
   * - ``source_key_path``
     - The path to the public key. Use in conjunction with ``source_key``` and ``source_key_pass_phrase``.
