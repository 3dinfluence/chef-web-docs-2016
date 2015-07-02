.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |resource remote_directory| resource block transfers a directory from a cookbook to a node, and then assigns the permissions needed on that directory. For example:

.. code-block:: ruby

   remote_directory '/etc/apache2' do
     source 'apache2'
     owner 'root'
     group 'root'
     mode '0755'
     action :create
   end

where

* ``'/etc/apache2'`` specifies the directory
* ``source`` specifies a directory in the current cookbook (use the ``cookbook`` attribute to specify a file that is in a different cookbook)
* ``owner``, ``group``, and ``mode`` define the permissions

The full syntax for all of the attributes that are available to the |resource remote_directory| resource is:

.. code-block:: ruby

   remote_directory 'name' do
     cookbook                   String
     files_backup               Integer, FalseClass
     files_group                String
     files_mode                 String
     files_owner                String
     group                      String, Integer
     inherits                   TrueClass, FalseClass
     mode                       String, Integer
     overwrite                  TrueClass, FalseClass
     owner                      String, Integer
     path                       String  # defaults to 'name' if not specified
     provider                   Chef::Provider::Directory::RemoteDirectory
     purge                      TrueClass, FalseClass
     recursive                  TrueClass, FalseClass
     rights                     Hash
     source                     String
     action                     Symbol # defaults to :create if not specified
   end

where 

* ``remote_directory`` is the resource
* ``name`` is the name of the resource block; when the ``path`` attribute is not specified, ``name`` is also the path to the directory, from the root
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``cookbook``, ``files_backup``, ``files_group``, ``files_mode``, ``files_owner``, ``group``, ``inherits``, ``mode``, ``overwrite``, ``owner``, ``path``, ``provider``, ``recursive``, ``rights``, and ``source`` are attributes of this resource, with example values shown. |see attributes|
