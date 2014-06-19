.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A sample |client rb| file that contains all possible settings (listed alphabetically):

.. code-block:: ruby

   add_formatter :nyan
   add_formatter :foo
   add_formatter :bar
   checksum_path "/var/chef/checksums"
   cookbook_path [ 
                  "/var/chef/cookbooks", 
                  "/var/chef/site-cookbooks" 
                 ]
   data_bag_path "/var/chef/data_bags"
   environment "production"
   environment_path "/var/chef/environments"
   file_backup_path "/var/chef/backup"
   file_cache_path "/var/chef/cache"
   json_attribs nil
   lockfile nil
   log_level :info
   log_location STDOUT
   node_name "mynode.example.com"
   recipe_url "http://path/to/remote/cookbook"
   rest_timeout 300
   role_path "/var/chef/roles"
   sandbox_path "path_to_folder"
   solo false
   syntax_check_cache_path
   umask 0022
   verbose_logging nil
