.. This is an included how-to. 


To find the uptime of all of your Web servers running |ubuntu| on the |amazon ec2| platform, enter:

.. code-block:: bash

   $ knife ssh "role:web" "uptime" -x ubuntu -a ec2.public_hostname

to return something like:

.. code-block:: bash

   ec2-174-129-127-206.compute-1.amazonaws.com  13:50:47 up 1 day, 23:26,  1 user,  load average: 0.25, 0.18, 0.11
   ec2-67-202-63-102.compute-1.amazonaws.com    13:50:47 up 1 day, 23:33,  1 user,  load average: 0.12, 0.13, 0.10
   ec2-184-73-9-250.compute-1.amazonaws.com     13:50:48 up 16:45,  1 user,  load average: 0.30, 0.22, 0.13
   ec2-75-101-240-230.compute-1.amazonaws.com   13:50:48 up 1 day, 22:59,  1 user,  load average: 0.24, 0.17, 0.11
   ec2-184-73-60-141.compute-1.amazonaws.com    13:50:48 up 1 day, 23:30,  1 user,  load average: 0.32, 0.17, 0.15
