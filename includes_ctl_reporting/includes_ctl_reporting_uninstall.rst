.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Chef Reporting.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``uninstall`` subcommand is used to remove the |reporting| add-on to |chef server oec|, but without removing any of the data. This subcommand will shut down all services (including the ``runit`` process supervisor).

This subcommand has the following syntax:

.. code-block:: bash

   $ opscode-reporting-ctl uninstall

.. note:: To revert the ``uninstall`` subcommand, run the ``reconfigure`` subcommand (because the ``start`` subcommand is disabled by the ``uninstall`` command). 





