.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef-shell.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This command has the following syntax::

   chef-shell OPTION VALUE OPTION VALUE ...

This command has the following options:

``-a``, ``--standalone``
   |chef_shell mode standalone|

``-c CONFIG``, ``--config CONFIG``
   |config chef-client|

``-h``, ``--help``
   |help subcommand|

``-j PATH``, ``--json-attributes PATH``
   |json attributes|

   .. include:: ../../includes_node/includes_node_ctl_run_list.rst

   .. include:: ../../includes_node/includes_node_ctl_attribute.rst

``-l LEVEL``, ``--log-level LEVEL``
   |log_level|

``-s``, ``--solo``
   |chef_shell mode solo|

``-S CHEF_SERVER_URL``, ``--server CHEF_SERVER_URL``
   |chef_server_url|

``-v``, ``--version``
   |version chef|

``-z``, ``--client``
   |chef_shell mode client|

