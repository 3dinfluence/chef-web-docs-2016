.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following settings for ``opscode-certificate``:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_certificate['dir']``
     - The directory in which ``opscode-certificate`` is located. The default value is the recommended value. Default value: ``"/var/opt/opscode/opscode-certificate"``.
   * - ``opscode_certificate['enable']``
     - |enable service| Default value: ``true``.
   * - ``opscode_certificate['ha']``
     - |use ha| Default value: ``false``.
   * - ``opscode_certificate['log_directory']``
     - |directory logs| The default value is the recommended value. Default value: ``"/var/log/opscode/opscode-certificate"``.
   * - ``opscode_certificate['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``opscode_certificate['num_certificates_per_worker']``
     - Default value: ``"50"``.
   * - ``opscode_certificate['num_workers']``
     - Default value: ``"2"``.
   * - ``opscode_certificate['port']``
     - |port opscode_certificate| Default value: ``5140``.
   * - ``opscode_certificate['vip']``
     - |ip_address virtual| Default value: ``"127.0.0.1"``.