.. This is an included how-to. 


The following example shows how to use the ``not_if`` condition to create a file based on a template and using a string to specify the condition:

.. code-block:: ruby

   template "/tmp/somefile" do
     mode 00644
     source "somefile.erb"
     not_if "test -f /etc/passwd"
   end

