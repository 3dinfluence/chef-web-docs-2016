.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for test-kitchen.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Use the ``list`` subcommand to view the list of instances. Instances are based on the list of platforms in the |kitchen yml| file. |kitchen| will auto-name instances by combining a suite name with a platform name. For example, if a suite is named ``default`` and a platform is named ``ubuntu-10.04``, then the instance would be ``default-ubuntu-10.04``. This ensures that |kitchen| instances have safe |dns| and hostname records.