.. This is an included how-to. 

.. To delete a registry key:

.. code-block:: ruby

   registry_key "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU" do
     values [{
       :name => "NoAutoRebootWithLoggedOnUsers",
       :type => :dword
       }]
     action :delete
   end





