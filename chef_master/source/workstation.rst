=====================================================
Workstations
=====================================================

.. include:: ../../includes_workstation/includes_workstation.rst

Some important components of workstations include:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Feature
     - Description
   * - :doc:`Knife </knife>`
     - .. include:: ../../includes_knife/includes_knife.rst
   * - :doc:`The chef-repo </chef_repo>`
     - .. include:: ../../includes_chef_repo/includes_chef_repo.rst

       .. include:: ../../includes_chef_repo/includes_chef_repo_structure.rst
   * - :doc:`knife.rb </config_rb_knife>`
     - The |knife rb| file is used to specify the repository-specific configuration details for |knife|.
   * - :doc:`metadata.rb </config_rb_metadata>`
     - Metadata is stored in a file called |metadata rb| that lives at the top of each cookbook’s directory.

|chef dk_title|
=====================================================

.. include:: ../../includes_chef/includes_chef_index.rst

.. include:: ../../includes_chef_dk/includes_chef_dk.rst

After :doc:`installing the ChefDK </install_dk>`, learn more about the tools that are packaged with the |chef dk|:

* :doc:`chef (executable) </ctl_chef>`
* :doc:`Berkshelf </berkshelf>`
* :doc:`chef-vault </chef_vault>`
* :doc:`ChefSpec </chefspec>`
* :doc:`Foodcritic </foodcritic>`
* :doc:`test-kitchen </kitchen>`
