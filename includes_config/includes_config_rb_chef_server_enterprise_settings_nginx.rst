.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.
 
This configuration file has the following settings for |nginx|:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``nginx['cache_max_size']``
     - Default value: ``5000m``.
   * - ``nginx['client_max_body_size']``
     - Default value: ``250m``.
   * - ``nginx['dir']``
     - |directory generic| |default_value_recommended| Default value: ``/var/opt/chef-server/nginx``.
   * - ``nginx['enable']``
     - |enable service| Default value: ``true``.
   * - ``nginx['enable_ipv6']``
     - |enable ipv6| Default value: ``false``.
   * - ``nginx['enable_non_ssl']``
     - |enable non_ssl| Default value: ``false``.
   * - ``nginx['gzip']``
     - |enable gzip| Default value: ``on``.
   * - ``nginx['gzip_comp_level']``
     - |gzip compression_level| Default value: ``2``.
   * - ``nginx['gzip_http_version']``
     - |gzip http_version| Default value: ``1.0``.
   * - ``nginx['gzip_proxied']``
     - |gzip proxied| Default value: ``any``.
   * - ``nginx['gzip_types']``
     - |gzip types| Default value: ``[ "text/plain", "text/css", "application/x-javascript", "text/xml", "application/xml", "application/xml+rss", "text/javascript", "application/json" ]``.
   * - ``nginx['ha']``
     - |use ha| Default value: ``false``.
   * - ``nginx['keepalive_timeout']``
     - |worker_max_keepalive| Default value: ``65``.
   * - ``nginx['log_directory']``
     - |directory logs| The default value is the recommended value. Default value: ``/var/log/chef-server/nginx``.
   * - ``nginx['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``nginx['non_ssl_port']``
     - |port non_ssl_nginx| Default value: ``80``. Use ``nginx['enable_non_ssl']`` to enable or disable |ssl| redirects on this port number. Set to ``false`` to disable non-SSL connections.
   * - ``nginx['sendfile']``
     - |use sendfile| Default value: ``on``.
   * - ``nginx['server_name']``
     - |server_fqdn| Default value: ``node['fqdn']``.
   * - ``nginx['ssl_certificate']``
     - |ssl_certificate| Default value: ``nil``.
   * - ``nginx['ssl_certificate_key']``
     - |ssl_certificate key| Default value: ``nil``.
   * - ``nginx['ssl_ciphers']``
     - |ssl_ciphers| To favor AES256 with ECDHE forward security, use ``HIGH:MEDIUM:!LOW:!kEDH:!aNULL:!ADH:!eNULL:!EXP:!SSLv2:!SEED:!CAMELLIA:!PSK``. Default value: varies.
   * - ``nginx['ssl_company_name']``
     - Default value: ``YouCorp``.
   * - ``nginx['ssl_country_name']``
     - Default value: ``US``.
   * - ``nginx['ssl_email_address']``
     - Default value: ``you@example.com``.
   * - ``nginx['ssl_locality_name']``
     - Default value: ``Seattle``.
   * - ``nginx['ssl_organizational_unit_name']``
     - Default value: ``Operations``.
   * - ``nginx['ssl_port']``
     - Default value: ``443``.
   * - ``nginx['ssl_protocols']``
     - |version protocols_ssl| For the highest possible security, disable |ssl| 3.0 and allow only TLS: ``nginx['ssl_protocols'] "TLSv1 TLSv1.1 TLSv1.2"``. Default value: varies, depending on the configuration of the |chef server| topology.
   * - ``nginx['ssl_state_name']``
     - Default value: ``WA``.
   * - ``nginx['tcp_nodelay']``
     - |use nagle| Default value: ``on``.
   * - ``nginx['tcp_nopush']``
     - |use tcpip| Default value: ``on``.
   * - ``nginx['url']``
     - Default value: ``https://#{node['fqdn']}``.
   * - ``nginx['worker_connections']``
     - |worker_connections| Use with ``nginx['worker_processes']`` to determine the maximum number of allowed clients. Default value: ``10240``.
   * - ``nginx['worker_processes']``
     - |worker_processes| Use with ``nginx['worker_connections']`` to determine the maximum number of allowed clients. Default value: ``node['cpu']['total'].to_i``.
   * - ``nginx['x_forwarded_proto']``
     - |x_forwarded_proto| This is the protocol used to connect to |chef server oec| by a |chef client| or a workstation. Default value: ``"https"``.
