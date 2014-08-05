.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following settings for ``opscode-chef-mover``:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_chef_mover['bulk_fetch_batch_size']``
     - Default value: ``'5'``.
   * - ``opscode_chef_mover['cache_ttl']``
     - Default value: ``'3600'``.
   * - ``opscode_chef_mover['db_pool_size']``
     - **TYPO INTENTIONAL, PENDING REVIEW/SYNC** |db_pool_size| Default value: ``'5'``.
   * - ``opscode_chef_mover['data_dir']``
     - |directory generic_data| |default_value_recommended| Default value: ``"/var/opt/opscode/opscode-chef-mover/data"``.
   * - ``opscode_chef_mover['dir']``
     - |directory generic| |default_value_recommended| Default value: ``"/var/opt/opscode/opscode-chef-mover"``.
   * - ``opscode_chef_mover['enable']``
     - |enable service| Default value: ``true``.
   * - ``opscode_chef_mover['ha']``
     - |use ha| Default value: ``false``.
   * - ``opscode_chef_mover['ibrowse_max_pipeline_size']``
     - Default value: ``1``.
   * - ``opscode_chef_mover['ibrowse_max_sessions']``
     - Default value: ``256``.
   * - ``opscode_chef_mover['log_directory']``
     - |directory logs| |default_value_recommended| Default value: ``"/var/log/opscode/opscode-chef-mover"``.
   * - ``opscode_chef_mover['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``opscode_chef_mover['max_cache_size']``
     - Default value: ``'10000'``.
   * - ``opscode_chef_mover['solr_http_cull_interval']``
     - Default value: ``"{1, min}"``.
   * - ``opscode_chef_mover['solr_http_init_count']``
     - Default value: ``25``.
   * - ``opscode_chef_mover['solr_http_max_age']``
     - Default value: ``"{70, sec}"``.
   * - ``opscode_chef_mover['solr_http_max_connection_duration']``
     - Default value: ``"{70,sec}"``.
   * - ``opscode_chef_mover['solr_http_max_count']``
     - Default value: ``100``.
   * - ``opscode_chef_mover['solr_ibrowse_options']``
     - Default value: ``"[{connect_timeout, 10000}]"``.
   * - ``opscode_chef_mover['solr_timeout']``
     - Default value: ``30000``.
