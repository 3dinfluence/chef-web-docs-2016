.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for opscode-analytics-ctl.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``start`` subcommand is used to start all services that are enabled in |chef analytics|. This command can also be run for an individual service by specifying the name of the service in the command.

This subcommand has the following syntax:

.. code-block:: bash

   $ opscode-analytics-ctl start name_of_service

where ``name_of_service`` represents the name of any service that is listed after running the ``service-list`` subcommand. When a service is successfully started the output should be similar to:

.. code-block:: bash

   $ ok: run: service_name: (pid 12345) 1s

The |chef server oec| supervisor is configured to wait seven seconds for a service to respond to a command from the supervisor. If you see output that references a timeout, it means that a signal has been sent to the process, but that the process has yet to actually comply. In general, processes that have timed out are not a big concern, unless they are failing to respond to the signals at all. If a process is not responding, use a command like the ``kill`` subcommand to stop the process, investigate the cause (if required), and then use the ``start`` subcommand to re-enable it.



