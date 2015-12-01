.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef-server-ctl.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``backup`` subcommand is used to back up all |chef server| data. This subcommand:

* Requires |rsync| to be installed on the |chef server| prior to running the command
* Requires a ``chef-server-ctl reconfigure`` prior to running the command
* Should not be run in a |chef server| configuration with an external |postgresql| database; `use knife ec backup <https://github.com/chef/knife-ec-backup>`__ instead
* Puts the initial backup in the `` /var/opt/chef-backup`` directory as a |tar gz| file; move this backup to a new location for safe keeping