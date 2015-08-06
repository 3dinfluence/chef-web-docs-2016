.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This configuration file has the following settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``add_formatter``
     - |add_formatter| For example:

       .. code-block:: ruby

          add_formatter [ 
            '/path/to/formatter', 
            '/path/to/formatter' 
          ]
   * - ``authorized_openid_identifiers``
     - |authorized_openid_identifiers| For example:

       .. code-block:: ruby

          username.myopenid.com

       or:

       .. code-block:: ruby

          http://username.myopenid.com
   * - ``authorized_openid_providers``
     - |authorized_openid_providers| For example:

       .. code-block:: ruby

          myopenid.com
   * - ``checksum_path``
     - |checksum_path| For example:

       .. code-block:: ruby

          checksum_path 'path_to_folder'
   * - ``cookbook_path``
     - |cookbook_path subdirectory| For example:

       .. code-block:: ruby

          cookbook_path [ 
            '/var/chef/cookbooks', 
            '/var/chef/site-cookbooks' 
          ]
   * - ``data_bag_path``
     - |data_bag_path| Default value: ``/var/chef/databags``. For example:

       .. code-block:: ruby

          data_bag_path '/var/chef/databags'
   * - ``file_backup_path``
     - |path file_backup| Default value: ``/var/chef/backup``. For example:

       .. code-block:: ruby

          file_backup_path '/var/chef/backup'
   * - ``file_cache_path``
     - |file cache_path| For example:

       .. code-block:: ruby

          file_cache_path '/var/chef/cache'
   * - ``json_attribs``
     - |json attributes| For example:

       .. code-block:: ruby

          json_attribs nil
   * - ``lockfile``
     - |lockfile| For example:

       .. code-block:: ruby

          lockfile nil
   * - ``log_level``
     - |log_level| Possible levels: ``debug``, ``info``, ``warn``, ``error``, or ``fatal``. For example:

       .. code-block:: ruby

          log_level :info
   * - ``log_location``
     - |log_location| Default value: ``STDOUT``. For example:

       .. code-block:: ruby

          log_location STDOUT
   * - ``node_name``
     - |name node| For example:

       .. code-block:: ruby

          node_name 'mynode.example.com'
   * - ``openid_cstore_couchdb``
     - |openid_cstore_couchdb| Default value: ``false``. For example:

       .. code-block:: ruby

          openid_cstore_couchdb false
   * - ``openid_cstore_path``
     - |openid_cstore_path| Default value: ``/var/chef/openid/cstore``. For example:

       .. code-block:: ruby

          openid_cstore_path '/var/chef/openid/cstore'
   * - ``recipe_url``
     - |recipe_url| For example:

       .. code-block:: ruby

          recipe_url 'http://path/to/remote/cookbook'
   * - ``rest_timeout``
     - |timeout rest| Default value: ``300``. For example:

       .. code-block:: ruby

          rest_timeout 300
   * - ``role_path``
     - |path roles_chef| Default value: ``/var/chef/roles``. For example:

       .. code-block:: ruby

          role_path '/var/chef/roles'
   * - ``sandbox_path``
     - |sandbox_path| For example:

       .. code-block:: ruby

          sandbox_path 'path_to_folder'
   * - ``solo``
     - |solo mode| Default value: ``false``. For example:

       .. code-block:: ruby

          solo false
   * - ``syntax_check_cache_path``
     - |syntax_check_cache_path|
   * - ``umask``
     - |umask| Default value: ``0022``. For example:

       .. code-block:: ruby

          umask 0022
   * - ``verbose_logging``
     - |verbose_logging| Default value: ``nil``. For example, when ``verbose_logging`` is set to ``true`` or ``nil``:

       .. code-block:: bash

          [date] INFO: *** Chef 0.10.6.rc.1 ***
          [date] INFO: Setting the run_list 
                       to ["recipe[a-verbose-logging]"] from JSON
          [date] INFO: Run List is [recipe[a-verbose-logging]]
          [date] INFO: Run List expands to [a-verbose-logging]
          [date] INFO: Starting Chef Run for some_node
          [date] INFO: Running start handlers
          [date] INFO: Start handlers complete.
          [date] INFO: Loading cookbooks [test-verbose-logging]
          [date] INFO: Processing file[/tmp/a1] action create  
                       (a-verbose-logging::default line 20)
          [date] INFO: Processing file[/tmp/a2] action create  
                       (a-verbose-logging::default line 21)
          [date] INFO: Processing file[/tmp/a3] action create  
                       (a-verbose-logging::default line 22)
          [date] INFO: Processing file[/tmp/a4] action create  
                       (a-verbose-logging::default line 23)
          [date] INFO: Chef Run complete in 1.802127 seconds
          [date] INFO: Running report handlers
          [date] INFO: Report handlers complete

       When ``verbose_logging`` is set to ``false`` (for the same output):

       .. code-block:: bash

          [date] INFO: *** Chef 0.10.6.rc.1 ***
          [date] INFO: Setting the run_list 
                       to ["recipe[a-verbose-logging]"] from JSON
          [date] INFO: Run List is [recipe[a-verbose-logging]]
          [date] INFO: Run List expands to [a-verbose-logging]
          [date] INFO: Starting Chef Run for some_node
          [date] INFO: Running start handlers
          [date] INFO: Start handlers complete.
          [date] INFO: Loading cookbooks [a-verbose-logging]
          [date] INFO: Chef Run complete in 1.565369 seconds
          [date] INFO: Running report handlers
          [date] INFO: Report handlers complete

       Where in the examples above, ``[date]`` represents the date and time the long entry was created. For example: ``[Mon, 21 Nov 2011 09:37:39 -0800]``.
