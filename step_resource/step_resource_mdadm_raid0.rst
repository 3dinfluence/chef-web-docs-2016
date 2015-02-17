.. This is an included how-to. 

The |mdadm| command can be used to create |raid| arrays. For example, a |raid| 0 array named ``/dev/md0`` with 10 devices would have a command similar to the following:

.. code-block:: bash

   $ mdadm --create /dev/md0 --level=0 --raid-devices=10 /dev/s01.../dev/s10

where ``/dev/s01 .. /dev/s10`` represents 10 devices (01, 02, 03, and so on). This same command, when expressed as a recipe using the |resource mdadm| resource, would be similar to:

.. code-block:: ruby

   mdadm "/dev/md0" do
     devices [ "/dev/s01", ... "/dev/s10" ]
     level 0
     action :create
   end

(again, where ``/dev/s01 .. /dev/s10`` represents devices /dev/s01, /dev/s02, /dev/s03, and so on).