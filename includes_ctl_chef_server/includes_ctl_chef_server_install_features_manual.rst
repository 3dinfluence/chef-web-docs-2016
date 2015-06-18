.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef-server-ctl.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``install`` subcommand downloads packages from https://packagecloud.io/ by default. For systems that are behind a firewall (and may not have connectivity to |packagecloud|), these packages can be downloaded from https://downloads.chef.io/chef-manage/, and then installed manually. First download the package that is appropriate for the platform, save it to a local path, and then run the ``install`` command using the ``--path`` option to specify the directory in which the package is located:

.. code-block:: bash

   $ chef-server-ctl install PACKAGE_NAME --path /path/to/package/directory

For example:

.. code-block:: bash

   $ chef-server-ctl install opscode-manage --path /root/packages

The ``chef-server-ctl`` command will install the first ``opscode-manage`` package found in the ``/root/packages`` directory.
