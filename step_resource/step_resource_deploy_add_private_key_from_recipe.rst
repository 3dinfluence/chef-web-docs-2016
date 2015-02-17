.. This is an included how-to. 

If there isn't much concern about people being able to view a private key, add it to ``cookbook/COOKBOOK_NAME/files/default/id_deploy`` and add it to the |ssh| file locally on the node using the |resource cookbook_file| resource.

To add a private key to a node:

.. code-block:: ruby

   cookbook_file '/tmp/private_code/.ssh/id_deploy' do
     source 'id_deploy'
     owner 'ubuntu'
     mode 00600
   end


