.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use following |client rb| settings to manage |ssl| certificate preferences:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``local_key_generation``
     - |generate local_keys| Default value: ``true``.
   * - ``ssl_ca_file``
     - |ssl_ca_file|
   * - ``ssl_ca_path``
     - |ssl_ca_path|
   * - ``ssl_client_cert``
     - |ssl_client_cert| Default value: ``nil``.
   * - ``ssl_client_key``
     - |ssl_client_key| Default value: ``nil``.
   * - ``ssl_verify_mode``
     - |ssl_verify_mode|
       
       * |ssl_verify_mode_verify_none|
       * |ssl_verify_mode_verify_peer| This is the recommended setting.
       
       Depending on how |open ssl| is configured, the ``ssl_ca_path`` may need to be specified.
   * - ``verify_api_cert``
     - |ssl_verify_mode_verify_api_cert| Default value: ``true``.

