.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following general settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``addons['install']``
     - Default value: ``false``.
   * - ``addons['path']``
     - Default value: ``nil``.
   * - ``addons['packages']``
     - Default value: ``%w{opscode-reporting opscode-manage opscode-analytics opscode-push-jobs-server}``.
   * - ``api_version``
     - |version chef_server| Default value: ``"12.0.0"``.
   * - ``default_orgname``
     - |default_orgname|
   * - ``flavor``
     - Default value: ``"cs"``.
   * - ``install_path``
     - |directory chef_server| Default value: ``"/opt/opscode"``.
   * - ``from_email``
     - Default value: ``'"Opscode" <donotreply@opscode.com>'``.
   * - ``license['nodes']``
     - |license chef_server| Default value: ``25``.
   * - ``license['upgrade_url']``
     - |license url| Default value: ``"http://www.chef.io/contact/on-premises-simple"``.
   * - ``notification_email``
     - |email chef_server| Default value: ``"pc-default@opscode.com"``.
   * - ``role``
     - |role chef_server| Possible values: ``backend``, ``frontend``, or ``standalone``. Default value: ``"standalone"``.
   * - ``topology``
     - The topology of the |chef server|. Possible values: ``ha``, ``manual``, ``standalone``, and ``tier``. Default value: ``"standalone"``.
