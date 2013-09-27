.. This is an included how-to. 

To use the ``netdev_lag`` lightweight resource:

.. code-block:: ruby

   netdev_lag "ae0" do
     links %w{ ge-0/0/1 ge-0/0/2 }
     minimum_links 1
     lacp "disable"
     action :create
   end
