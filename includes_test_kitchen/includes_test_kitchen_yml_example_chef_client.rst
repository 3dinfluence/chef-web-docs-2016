.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following |kitchen yml| file is part of the |cookbook chef_client| cookbook and ensures the |chef client| is configured correctly.

.. code-block:: yaml

   driver:
     name: vagrant
   
   provisioner:
     name: chef_zero
   
   platforms:
     - name: centos-5.10
     - name: centos-6.5
     - name: fedora-19
     - name: ubuntu-1004
     - name: ubuntu-1204
     - name: ubuntu-1310

   suites:
   
   - name: service_init
     run_list:
     - recipe[minitest-handler]
     - recipe[chef-client::config]
     - recipe[chef-client_test::service_init]
     - recipe[chef-client::init_service]
     attributes: {}
   
   - name: service_runit
     run_list:
     - recipe[minitest-handler]
     - recipe[runit]
     - recipe[chef-client_test::service_runit]
     - recipe[chef-client::runit_service]
     attributes: {}
   
   - name: service_upstart
     run_list:
     - recipe[minitest-handler]
     - recipe[chef-client_test::service_upstart]
     - recipe[chef-client::upstart_service]
     excludes: ["centos-5.9"]
     attributes: {}
   
   - name: cron
     run_list:
     - recipe[minitest-handler]
     - recipe[chef-client::cron]
     attributes: {}
   
   - name: delete_validation
     run_list:
     - recipe[chef-client::delete_validation]
     attributes: {}
