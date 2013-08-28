.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This configuration file has the following settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``rabbitmq['consumer_id']``
     - Default value: ``hotsauce``.
   * - ``rabbitmq['data_dir']``
     - Default value: ``/var/opt/chef-server/rabbitmq/db``.
   * - ``rabbitmq['dir']``
     - Default value: ``/var/opt/chef-server/rabbitmq``.
   * - ``rabbitmq['enable']``
     - |enable service| Default value: ``true``.
   * - ``rabbitmq['ha']``
     - Indicates that the |chef server| is installed as part of a |ha| topology. Default value: ``false``.
   * - ``rabbitmq['log_directory']``
     - The directory in which log files are located. Default value: ``/var/log/chef-server/rabbitmq``.
   * - ``rabbitmq['node_ip_address']``
     - |ip_address rabbitmq| Default value: ``127.0.0.1``.
   * - ``rabbitmq['node_port']``
     - |port rabbitmq| Default value: ``5672``.
   * - ``rabbitmq['nodename']``
     - |name node|  Default value: ``rabbit@localhost``.
   * - ``rabbitmq['password']``
     - |password rabbitmq| Default value: ``chefrocks``.
   * - ``rabbitmq['user']``
     - The user. Default value: ``chef``.
   * - ``rabbitmq['vhost']``
     - The virtual host. Default value: ``/chef``.
   * - ``rabbitmq['vip']``
     - Default value: ``127.0.0.1``.


