.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Some important components of workstations include:

.. list-table::
   :widths: 100 420
   :header-rows: 1

   * - Component
     - Description
   * - .. image:: ../../images/icon_devkit.svg
          :width: 100px
          :align: center

     - .. include:: ../../includes_chef_dk/includes_chef_dk.rst
   * - .. image:: ../../images/icon_ctl_chef.svg
          :width: 100px
          :align: center

       .. image:: ../../images/icon_ctl_knife.svg
          :width: 100px
          :align: center

     - |chef| incudes two important command-line tools:

       * Use the |chef ctl| command-line tool to work with items in a |chef repo|, which is the primary location in which cookbooks are authored, tested, and maintained, and from which policy is uploaded to the |chef server|
       * Use the |knife| command-line tool to interact with nodes or work with objects on the |chef server|

   * - .. image:: ../../images/icon_repository.svg
          :width: 100px
          :align: center

     - .. include:: ../../includes_chef_repo/includes_chef_repo.rst

       .. include:: ../../includes_chef_repo/includes_chef_repo_structure.rst

   * - .. image:: ../../images/icon_kitchen.svg
          :width: 100px
          :align: center

     - .. include:: ../../includes_test_kitchen/includes_test_kitchen.rst
   * - .. image:: ../../images/icon_chefspec.svg
          :width: 100px
          :align: center

     - .. include:: ../../includes_chefspec/includes_chefspec.rst
