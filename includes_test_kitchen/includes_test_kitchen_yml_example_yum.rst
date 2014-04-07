.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following |kitchen yml| file is part of the |cookbook yum| cookbook and is used for |digital ocean|- and |amazon aws|-based providers.

.. code-block:: yaml

   ---
   driver_config:
     digitalocean_client_id: <%= ENV['DIGITAL_OCEAN_CLIENT_ID'] %>
     digitalocean_api_key: <%= ENV['DIGITAL_OCEAN_API_KEY'] %>
     aws_access_key_id: <%= ENV['AWS_ACCESS_KEY_ID'] %> 
     aws_secret_access_key: <%= ENV['AWS_SECRET_ACCESS_KEY'] %>
     aws_ssh_key_id: <%= ENV['AWS_KEYPAIR_NAME'] %>
   
   provisioner:
     name: chef_zero
     require_chef_omnibus: latest
   
   platforms:
   - name: centos-5.8
     driver_plugin: digitalocean
     driver_config:
       image_id: 1601
       flavor_id: 63
       region_id: 4
       ssh_key_ids: <%= ENV['DIGITAL_OCEAN_SSH_KEY_IDS'] %>
       ssh_key: <%= ENV['DIGITAL_OCEAN_SSH_KEY_PATH'] %>
   
   - name: centos-6.4
     driver_plugin: digitalocean
     driver_config:
       image_id: 562354
       flavor_id: 63
       region_id: 4
       ssh_key_ids: <%= ENV['DIGITAL_OCEAN_SSH_KEY_IDS'] %>
       ssh_key: <%= ENV['DIGITAL_OCEAN_SSH_KEY_PATH'] %>
   
   - name: amazon-2013.09
     driver_plugin: ec2
     driver_config:
       image_id: ami-3be4bc52
       username: ec2-user
       ssh_key: <%= ENV['EC2_SSH_KEY_PATH'] %>
   
   - name: fedora-19
     driver_plugin: digitalocean
     driver_config:
       image_id: 696598
       flavor_id: 63
       region_id: 4
       ssh_key_ids: <%= ENV['DIGITAL_OCEAN_SSH_KEY_IDS'] %>
       ssh_key: <%= ENV['DIGITAL_OCEAN_SSH_KEY_PATH'] %>
   
   suites:
   - name: default
     run_list:
     - recipe[yum::default]
     attributes: {}
