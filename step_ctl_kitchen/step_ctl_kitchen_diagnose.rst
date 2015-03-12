.. This is an included how-to. 


Use the ``--loader`` option to include diagnostic data in the output:

.. code-block:: yaml

   ---
   loader:
     combined_config:
       filename: 
       raw_data:
         driver:
           name: vagrant
           socket: tcp://192.168.12.34:1234
       provisioner:
        #...

or:

.. code-block:: yaml

   ---
   loader:
     global_config:
       filename: "/Users/username/.kitchen/config.yml"
       raw_data: #...
     project_config:
       filename: "/Users/username/Projects/sandbox/path/to/kitchen.yml"
       raw_data: #...
     local_config:

