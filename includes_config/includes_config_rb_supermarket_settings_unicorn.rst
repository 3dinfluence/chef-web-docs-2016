.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.
 
This configuration file has the following settings for |ruby unicorn|:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``supermarket['unicorn']['after_fork']``
     - 
   * - ``supermarket['unicorn']['copy_on_write']``
     - Default value: ``true``.
   * - ``supermarket['unicorn']['before_exec']``
     - 
   * - ``supermarket['unicorn']['before_fork']``
     - 
   * - ``supermarket['unicorn']['enable_stats']``
     - Default value: ``false``.
   * - ``supermarket['unicorn']['forked_group']``
     - Default value: ``node['supermarket']['group']``.
   * - ``supermarket['unicorn']['forked_user']``
     - Default value: ``node['supermarket']['user']``.
   * - ``supermarket['unicorn']['listen']``
     - |ip_address service| Default value: ``["127.0.0.1:#{node['supermarket']['rails']['port']}"]``.
   * - ``supermarket['unicorn']['name']``
     - Default value: ``'supermarket'``.
   * - ``supermarket['unicorn']['pid']``
     - Default value: ``"#{node['supermarket']['var_directory']}/rails/run/unicorn.pid"``.
   * - ``supermarket['unicorn']['preload_app']``
     - Default value: ``true``.
   * - ``supermarket['unicorn']['stderr_path']``
     - 
   * - ``supermarket['unicorn']['stdout_path']``
     - 
   * - ``supermarket['unicorn']['unicorn_command_line']``
     - 
   * - ``supermarket['unicorn']['worker_processes']``
     - |worker_processes| Default value: ``node['nginx']['worker_processes']``.
   * - ``supermarket['unicorn']['worker_timeout']``
     - |timeout worker_process| Default value: ``15``.
   * - ``supermarket['unicorn']['working_directory']``
     - 
