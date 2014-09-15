.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``cipher``
     - Use to specify the cipher for a .pem file. Default value: ``DES-EDE3-CBC``.
   * - ``exponent``
     - Use to specify the exponent for an RSA private key. This is always an odd integer value, often a prime Fermat number, and typically ``5``, ``17``, ``257``, or ``65537``.
   * - ``format``
     - Use to specify the format of a private key. Possible values: ``pem`` and ``der``. Default value: ``pem``.
   * - ``pass_phrase``
     - Use to specify the pass phrase for a .pem file.
   * - ``path``
     - Use to specify the path to a private key. Set to ``none`` to create a private key in-memory and not on-disk. Default value: the ``name`` of the resource block. (See "Syntax" section above.)
   * - ``public_key_format``
     - Use to specify the format of a public key. Possible values: ``der``, ``openssh``, and ``pem``. Default value: ``openssh``.
   * - ``public_key_path``
     - The path to a public key.
   * - ``regenerate_if_different``
     - Use to regenerate a private key if it does not have the desired size, type, and so on. Default value: ``false``.
   * - ``size``
     - Use to specify the size of an RSA or DSA private key. Default value: ``2048``.
   * - ``source_key``
     - Use to copy a private key, but apply a different ``format`` and ``password``. Use in conjunction with ``source_key_pass_phrase``` and ``source_key_path``.
   * - ``source_key_pass_phrase``
     - The pass phrase for the private key. Use in conjunction with ``source_key``` and ``source_key_path``.
   * - ``source_key_path``
     - The path to the private key. Use in conjunction with ``source_key``` and ``source_key_pass_phrase``.
   * - ``type``
     - Use to specify the type of private key. Possible values: ``dsa`` and ``rsa``. Default value: ``rsa``.




