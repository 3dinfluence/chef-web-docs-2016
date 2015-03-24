.. THIS PAGE DOCUMENTS chef-client version 11.4

=====================================================
knife ssh 
=====================================================

.. include:: ../../includes_knife/includes_knife_ssh.rst

Syntax
=====================================================
.. include:: ../../includes_knife/includes_knife_ssh_syntax.rst

Options
=====================================================
.. note:: Review the list of :doc:`common options </knife_common_options>` available to this (and all) |knife| subcommands and plugins.

.. include:: ../../includes_knife/includes_knife_12-1_ssh_options.rst

.. note:: See :doc:`knife.rb </config_rb_knife_optional_settings>` for more information about how to add certain |knife| options as settings in the |knife rb| file.

Examples
=====================================================
The following examples show how to use this |knife| subcommand:

**Find server uptime**

.. include:: ../../step_knife/step_knife_ssh_find_uptime.rst

**Run the chef-client on all nodes**

.. include:: ../../step_knife/step_knife_ssh_run_chef_client_on_all_nodes.rst

**Force a chef-client run**

.. include:: ../../step_knife/step_knife_ssh_force_chef_run.rst

**Run a command based on search query**

.. include:: ../../step_knife/step_knife_ssh_query_for_nodes.rst

**Upgrade all nodes**

.. include:: ../../step_knife/step_knife_ssh_upgrade_nodes.rst

**Specify the shell type**

.. include:: ../../step_knife/step_knife_ssh_shell_type.rst
