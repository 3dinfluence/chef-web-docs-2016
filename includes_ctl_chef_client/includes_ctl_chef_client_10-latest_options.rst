.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef-client.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This command has the following syntax::

   chef-client OPTION VALUE OPTION VALUE ...

This command has the following options:

``-A``, ``--fatal-windows-admin-check``
   |fatal_windows_admin_check|

``-c CONFIG``, ``--config CONFIG``
   |config chef-client|

``-d``, ``--daemonize``
   |daemonize| This option is only available on machines that run in |unix| or |linux| environments. For machines that are running |windows| that require similar functionality, use the ``chef-client::service`` recipe in the |cookbook chef_client| cookbook: http://community.opscode.com/cookbooks/chef-client. This will install a |chef client| service under |windows| using the |windows service wrapper|.

``-E ENVIRONMENT_NAME``, ``--environment ENVIRONMENT_NAME``
   |name environment|

``-f``, ``--[no-]fork``
   |fork_chef|

``-F FORMAT``, ``--format FORMAT``
   |format chef_ctls|

``-g GROUP``, ``--group GROUP``
   |name group_process_owner|

``-h``, ``--help``
   |help subcommand|

``-i SECONDS``, ``--interval SECONDS``
   |interval| |chef_client intervals_11-16| Default value: ``1800``.

``-j PATH``, ``--json-attributes PATH``
   |json attributes|

   .. include:: ../../includes_node/includes_node_ctl_run_list.rst

   .. warning:: .. include:: ../../includes_node/includes_node_ctl_attribute.rst

``-k KEY_FILE``, ``--client_key KEY_FILE``
   |client_key| Default value: ``/etc/chef/client.pem``.

``-K KEY_FILE``, ``--validation_key KEY_FILE``
   |validation_key| Default value: ``/etc/chef/validation.pem``.

``-l LEVEL``, ``--log-level LEVEL``
   |log_level| Possible levels: ``:auto`` (default), ``debug``, ``info``, ``warn``, ``error``, or ``fatal``. Default value: ``warn`` (when a terminal is available) or ``info`` (when a terminal is not available).

``-L LOGLOCATION``, ``--logfile LOGLOCATION``
   |log_location| This is recommended when starting any executable as a daemon. Default value: ``STDOUT``.

``--[no-]color``
   |color| Default setting: ``--color``.

``-N NODE_NAME``, ``--node-name NODE_NAME``
   |name node|

``-o RUN_LIST_ITEM``, ``--override-runlist RUN_LIST_ITEM``
   |override_runlist|

``--once``
   |once|

``-P PID_FILE``, ``--pid PID_FILE``
   |path pid_file| Default value: ``/tmp/name-of-executable.pid``.

``-R``, ``--enable-reporting``
   |enable_reporting|

``-s SECONDS``, ``--splay SECONDS``
   |splay| |chef_client intervals_11-16|

``-S CHEF_SERVER_URL``, ``--server CHEF_SERVER_URL``
   |url chef_server|

``-u USER``, ``--user USER``
   |user chef_client|

``-v``, ``--version``
   |version chef|

``-W``, ``--why-run``
   |whyrun_mode|
