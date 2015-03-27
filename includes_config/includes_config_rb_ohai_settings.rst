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
     - |disable plugin_ohai| The list of plugins included in |ohai| can be found in the ``ohai/lib/ohai/plugins`` directory. For example, disabling a single plugin:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = [
		       :MyPlugin
			   ]

       or disabling multiple plugins:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = [
		       :MyPlugin, 
			   :MyPlugin, 
			   :MyPlugin
			   ]

       and to disable multiple plugins, including |ohai| 6 plugins:

       .. code-block:: ruby

          Ohai::Config[:disabled_plugins] = [
		       :MyPlugin, 
			   :MyPlugin, 
			   "my_ohai_6_plugin"
			   ]

       When a plugin is disabled, the |chef client| log file will contain entries similar to:

       .. code-block:: ruby

          [2014-06-13T23:49:12+00:00] DEBUG: Skipping disabled plugin MyPlugin 

   * - ``Ohai::Config[:hints_path]``
     - |path hint_ohai|
   * - ``Ohai::Config[:log_level]``
     - |log_level|
   * - ``Ohai::Config[:logfile]``
     - |log_location|
   * - ``Ohai::Config[:plugin_path]``
     - An array of paths at which |ohai| plugins are located. Default value: ``[<CHEF_GEM_PATH>/ohai-9.9.9/lib/ohai/plugins]``. When custom |ohai| plugins are added, the paths must be added to the array. For example, a single plugin:

       .. code-block:: ruby

          Ohai::Config[:plugin_path] << '/etc/chef/ohai_plugins'

       and for multiple plugins:

       .. code-block:: ruby

          Ohai::Config[:plugin_path] += [
            '/etc/chef/ohai_plugins',
            '/path/to/other/plugins'
            ]


   * - ``Ohai::Config[:version]``
     - |version ohai|

.. note:: The |ohai| executable ignores settings in the |client rb| file when |ohai| is run independently of the |chef client|.