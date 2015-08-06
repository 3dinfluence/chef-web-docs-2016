.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``Ohai::Config[:directory]``
     - |path plugin_ohai|
   * - ``Ohai::Config[:disabled_plugins]``
     - |disable plugin_ohai|  The list of plugins included in |ohai| can be found in the ``ohai/lib/ohai/plugins`` directory. For example:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = 'my_plugin'

       or:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = 'windows::my_plugin'

       or:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = ['my_plugin', 'my_plugin', 'my_plugin']

       When a plugin is disabled, the |chef client| log file will contain entries similar to:

       .. code-block:: ruby

          [2014-06-13T23:49:12+00:00] DEBUG: Skipping disabled plugin my_plugin 

   * - ``Ohai::Config[:hints_path]``
     - |path hint_ohai|
   * - ``Ohai::Config[:log_level]``
     - |log_level|
   * - ``Ohai::Config[:log_location]``
     - |log_location|
   * - ``Ohai::Config[:version]``
     - |version ohai|

.. note:: The |ohai| executable ignores settings in the |client rb| file when |ohai| is run independently of the |chef client|.
