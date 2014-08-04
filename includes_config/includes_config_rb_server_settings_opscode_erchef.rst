.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following settings for ``opscode-erchef``:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_erchef['auth_skew']``
     - Default value: ``900``.
   * - ``opscode_erchef['authz_fanout']``
     - Default value: ``20``.
   * - ``opscode_erchef['authz_timeout']``
     - Default value: ``1000``.
   * - ``opscode_erchef['base_resource_url']``
     - The base URL to which the service will return links to API resources. Use ``:host_header`` to ensure the URL is derived from the host header of the incoming HTTP request. Default value: ``:host_header``.
   * - ``opscode_erchef['bulk_fetch_batch_size']``
     - Default value: ``5``.
   * - ``opscode_erchef['cache_ttl']``
     - Default value: ``3600``.
   * - ``opscode_erchef['cleanup_batch_size']``
     - Default value: ``0``.
   * - ``opscode_erchef['couchdb_max_conn']``
     - Default value: ``"100"``.
   * - ``opscode_erchef['db_pool_size']``
     - |db_pool_size| Default value: ``20``.
   * - ``opscode_erchef['depsolver_timeout']``
     - The amount of time (in milliseconds) to wait for cookbook dependency problems to be solved. Default value: ``"5000"``.
   * - ``opscode_erchef['depsolver_worker_count']``
     - The number of |ruby| processes for which cookbook dependency problems are unsolved. Use the ``pgrep -fl depselector`` command to verify the number of depsolver workers that are running. Default value: ``"5"``.
   * - ``opscode_erchef['dir']``
     - |directory generic| |default_value_recommended| Default value: ``/var/opt/chef-server/erchef``.
   * - ``opscode_erchef['enable']``
     - |enable service| Default value: ``true``.
   * - ``opscode_erchef['enable_actionlog']``
     - Use to enable |chef actions|, an add-on for |chef server oec|. Default value: ``false``.
   * - ``opscode_erchef['ha']``
     - |use ha| Default value: ``false``.
   * - ``opscode_erchef['ibrowse_max_pipeline_size']``
     - Default value: ``1``.
   * - ``opscode_erchef['ibrowse_max_sessions']``
     - Default value: ``256``.
   * - ``opscode_erchef['listen']``
     - The IP address on which the service will listen. Default value: ``127.0.0.1``.
   * - ``opscode_erchef['log_directory']``
     - |directory logs| |default_value_recommended| Default value: ``/var/log/chef-server/erchef``.
   * - ``opscode_erchef['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``opscode_erchef['max_cache_size']``
     - Default value: ``10000``.
   * - ``opscode_erchef['max_request_size']``
     - Default value: ``2500000``.
   * - ``opscode_erchef['port']``
     - |port service| Default value: ``8000``.
   * - ``opscode_erchef['root_metric_key']``
     - Default value: ``chefAPI``.
   * - ``opscode_erchef['s3_bucket']``
     - The |amazon s3| bucket. (This is configurable and may be pointed at external storage locations, such as |amazon ec2|. Four settings require configuration when pointing at an external cookbook storage location: ``bookshelf['vip']``, for the endpoint; ``bookshelf['access_key_id']``, for user access key; ``bookshelf['secret_access_key']``, for secret key; and ``opscode_erchef['s3_bucket']``, for the bucket name. Run the |chef server| ``reconfigure`` command after changing these settings.) Default value: ``bookshelf``.
   * - ``opscode_erchef['s3_parallel_ops_fanout']``
     - Default value: ``20``.
   * - ``opscode_erchef['s3_parallel_ops_timeout']``
     - Default value: ``5000``.
   * - ``opscode_erchef['s3_url_ttl']``
     - Default value: ``900``.
   * - ``opscode_erchef['udp_socket_pool_size']``
     - Default value: ``20``.
   * - ``opscode_erchef['umask']``
     - Default value: ``0022``.
   * - ``opscode_erchef['validation_client_name']``
     - Default value: ``chef-validator``.
   * - ``opscode_erchef['vip']``
     - |ip_address virtual| Default value: ``127.0.0.1``.

