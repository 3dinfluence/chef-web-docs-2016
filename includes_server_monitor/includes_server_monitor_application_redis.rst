.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The |service redis_lb| service located on the back end machine handles requests that are made from the |nginx| service that is located on all front end machines in a |chef server| cluster.

In the event of a disk full condition for the |redis| data store, the ``dump.rdb`` (the primary data store ``.rdb`` used by |redis|) can become corrupt and saved as a zero byte file.

When this occurs, after the |service redis_lb| service started, it's logs will show a statement similar to the following:

.. code-block:: bash

   2015-03-23_16:11:31.44256 [11529] 23 Mar 16:10:09.624 # Server started, Redis version 2.8.2
   2015-03-23_16:11:31.44256 [11529] 23 Mar 16:10:09.624 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.
   2015-03-23_16:11:31.44257 [11529] 23 Mar 16:11:31.438 # Short read or OOM loading DB. Unrecoverable error, aborting now.

The ``dump.rdb`` file will be empty:

.. code-block:: bash

   ls -al /var/opt/opscode/redis_lb/data/
   total 20
   drwxr-x--- 2 opscode opscode 4096 Mar 23 15:58 .
   drwxr-x--- 4 opscode opscode 4096 Dec 22 18:59 ..
   -rw-r--r-- 1 opscode opscode    0 Mar 23 15:58 dump.rdb

This situation is caused by a bug in |redis| where saves are allowed to succeed even when the disk has been full for some time, and not just on edge cases where the disk becomes full as |redis| is writing. To fix this issue, do the following:

1. Stop the |service redis_lb| service:

   .. code-block:: bash

      chef-server-ctl stop redis_lb

2. Remove the corrupt files:

   .. code-block:: bash

      cd /var/opt/opscode/redis_lb/data
      rm -fr *rdb

3. Start the |service redis_lb| service:

   .. code-block:: bash

      chef-server-ctl start redis_lb

      less /var/log/opscode/redis_lb/current
      2015-03-23_17:05:18.82516 [28676] 23 Mar 17:05:18.825 * The server is now ready to accept connections on port 16379

4. Reconfigure the |chef server| to re-populate |redis|:

   .. code-block:: bash

      chef-server-ctl reconfigure

5. Verify that |redis| is re-populated, as indicated by the key ``dl_default``:

   .. code-block:: bash

      /opt/opscode/embedded/bin/redis-cli -p 16379 keys \*
      1) "dl_default"
