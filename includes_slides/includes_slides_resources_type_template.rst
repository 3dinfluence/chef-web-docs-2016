.. The contents of this file are included in multiple slide decks.
.. This file should not be changed in a way that hinders its ability to appear in multiple slide decks.


A file to be generated from a template:

.. code-block:: ruby
       
   template "/etc/haproxy/haproxy.cfg" do
     source "haproxy.cfg.erb"
     owner "root"
     group "root"
     mode "0644"
     notifies :restart, "service[haproxy]"
   end
