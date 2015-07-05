.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |resource link| resource block creates symbolic or hard links. For example, to create a hard link from ``/tmp/file`` to ``/etc/file``:

.. code-block:: ruby

   link '/tmp/file' do
     to '/etc/file'
     link_type :hard
   end

Because the default value for ``link_type`` is symbolic, and because attributes that are not specified in the resource block will be assigned their default values, the following example creates a symbolic link:

.. code-block:: ruby

   link '/tmp/file' do
     to '/etc/file'
   end

The full syntax for all of the attributes that are available to the |resource link| resource is:

.. code-block:: ruby

   link 'name' do
     group                      Integer, String
     link_type                  Symbol
     mode                       Integer, String
     notifies                   # see description
     owner                      Integer, String
     provider                   Chef::Provider::Link
     target_file                String # defaults to 'name' if not specified
     to                         String
     action                     Symbol # defaults to :create if not specified
   end

where 

* ``link`` is the resource
* ``name`` is the name of the resource block
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``group``, ``link_type``, ``mode``, ``owner``, ``provider``, ``target_file``, and ``to`` are attributes of this resource, with the |ruby| type shown. |see attributes|
