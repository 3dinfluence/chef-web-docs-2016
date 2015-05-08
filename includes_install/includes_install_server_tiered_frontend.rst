.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

For each frontend server, use the following steps to set up the |chef server|:

#. Install the |chef server| package. For |redhat| and |centos| 6:

   .. code-block:: bash
      
      $ rpm -Uvh /tmp/chef-server-core-<version>.rpm

   For |ubuntu|:

   .. code-block:: bash
      
      $ dpkg -i /tmp/chef-server-core-<version>.deb

   After a few minutes, the |chef server| will be installed.

#. Create the ``/etc/opscode/`` directory, and then copy the entire contents of the ``/etc/opscode`` directory from the primary backend server, including all certificates and the |chef server rb| file.

#. Run the following command:

   .. code-block:: bash
      
      $ sudo chef-server-ctl reconfigure

#. Run the following command:

   .. code-block:: bash
      
      $ sudo chef-server-ctl start

#. .. include:: ../../step_ctl_chef_server/step_ctl_chef_server_user_create_admin.rst

#. .. include:: ../../step_ctl_chef_server/step_ctl_chef_server_org_create.rst

#. Run the following command:

   .. code-block:: bash
      
      $ sudo chef-server-ctl reconfigure
