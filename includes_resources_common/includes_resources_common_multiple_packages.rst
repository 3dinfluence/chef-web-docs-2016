.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A resource may specify multiple packages and/or versions for platforms that use |yum| or |apt|. Specifing multiple packages and/or versions allows a single transaction to:

* Download the specified packages and versions via a single HTTP transaction
* Update or install multiple packages with a single resource during the |chef client| run

For example, installing multiple packages:

.. code-block:: ruby

   package ['package1', 'package2']

Upgrading multiple packages:

.. code-block:: ruby

   package ['package1', 'package2']  do
     action :upgrade
   do

Removing multiple packages:

.. code-block:: ruby

   package ['package1', 'package2']  do
     action :remove
   do

Purging multiple packages:

.. code-block:: ruby

   package ['package1', 'package2']  do
     action :purge
   do

Notifications, via an implicit name:

.. code-block:: ruby

   package ['package1', 'package2']  do
     action :nothing
   do
   
   log "call a notification" do
     notifies :install, "package[package1, package2]", :immediately
   end

.. note:: Notifications and subscriptions do not need to be updated when packages and versions are added or removed from the ``package_name`` or ``version`` attributes.
