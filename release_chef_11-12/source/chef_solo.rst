.. THIS PAGE DOCUMENTS chef-client version 11.12

=====================================================
|chef solo|
=====================================================

.. warning:: The |chef client| now `includes an option called local mode <http://docs.chef.io/ctl_chef_client.html#run-in-local-mode>`_ (``--local-mode`` or ``-z``), which runs the |chef client| against the |chef repo| on the local machine as if it were running against a |chef server|. Local mode was added to the |chef client| in the 11.8 release. If you are running that version of the |chef client| (or later), you should consider using local mode instead of using |chef solo|.

.. include:: ../../includes_chef_solo/includes_chef_solo.rst

.. note:: |chef solo| is configured using the :doc:`chef-solo (executable) </ctl_chef_solo>`.

Cookbooks
-----------------------------------------------------
.. include:: ../../includes_chef_solo/includes_chef_solo_cookbooks.rst

Attributes
-----------------------------------------------------
.. include:: ../../includes_chef_solo/includes_chef_solo_attributes.rst

Data Bags
-----------------------------------------------------
.. include:: ../../includes_chef_solo/includes_chef_solo_data_bags.rst

Roles
-----------------------------------------------------
.. include:: ../../includes_chef_solo/includes_chef_solo_roles.rst

Environments
-----------------------------------------------------
.. include:: ../../includes_chef_solo/includes_chef_solo_environments.rst

|chef solo| (executable)
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_solo/includes_ctl_chef_solo.rst

Options
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_ctl_chef_solo/includes_ctl_chef_solo_11-12_options.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
**Run chef-solo using solo.rb settings**

.. code-block:: bash

   $ chef-solo -c ~/chef/solo.rb

**Use a URL**

.. include:: ../../step_ctl_chef_solo/step_ctl_chef_solo_use_url.rst

**Use a directory**

.. include:: ../../step_ctl_chef_solo/step_ctl_chef_solo_use_directory.rst

**Use a URL for cookbook and JSON data**

.. include:: ../../step_ctl_chef_solo/step_ctl_chef_solo_url_for_cookbook_and_json.rst

