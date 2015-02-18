.. This is an included how-to. 


The |resource service| resource does not support using the ``:enable`` and ``:disable`` actions with resources that are managed using |ibm aix_src|. This is because |ibm aix_src| does not have a standard mechanism for enabling and disabling services on system boot.

One approach for enabling or disabling services that are managed by |ibm aix_src| is to use the |resource execute| resource to invoke ``mkitab``, and then use that command to enable or disable the service.

The following example shows how to install a service:

.. code-block:: ruby

   execute "install #{node['chef_client']['svc_name']} in SRC" do
     command "mkssys -s #{node['chef_client']['svc_name']} 
                     -p #{node['chef_client']['bin']} 
                     -u root 
                     -S 
                     -n 15 
                     -f 9 
                     -o #{node['chef_client']['log_dir']}/client.log 
                     -e #{node['chef_client']['log_dir']}/client.log -a '
                     -i #{node['chef_client']['interval']} 
                     -s #{node['chef_client']['splay']}'"
     not_if "lssrc -s #{node['chef_client']['svc_name']}"
     action :run
   end

and then enable it using the ``mkitab`` command:

.. code-block:: ruby

   execute "enable #{node['chef_client']['svc_name']}" do
     command "mkitab '#{node['chef_client']['svc_name']}:2:once:/usr/bin/startsrc 
                     -s #{node['chef_client']['svc_name']} > /dev/console 2>&1'"
     not_if "lsitab #{node['chef_client']['svc_name']}"
   end
