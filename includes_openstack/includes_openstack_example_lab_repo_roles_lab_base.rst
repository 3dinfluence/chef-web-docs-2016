.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The base role ensures that the apt repository proxy is used, NTP and SSH are configured and the sysadmins in the users data bag are all installed. After this role is applied, the machines are available for whatever purpose they are needed.

.. code-block:: ruby

   name "lab-base"
   description "Default run_list for lab machines"
   run_list(
     "recipe[apt::cacher-client]",
     "recipe[ntp]",
     "recipe[openssh]",
     "recipe[users::sysadmins]",
     "recipe[sudo]",
     "recipe[chef-client::delete_validation]"
     )


