.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A |resource execute| resource block typically executes a single command that is unique to the environment in which a recipe will run. Some |resource execute| resource commands are run by themselves, but often they are run in combination with other |chef| resources. For example, a single command:

.. code-block:: ruby

   execute 'apache_configtest' do
     command '/usr/sbin/apachectl configtest'
   end

where ``'/usr/sbin/apachectl configtest'`` is a command that tests if the configuration files for |apache| are valid.

A command that is run in combination with another |chef| resource is often similar to the following, where the |resource template| resource is run along with the previous example to add an entry to the LDAP Directory Interchange Format (LDIF) file:

.. code-block:: ruby

   execute 'slapadd' do
     command 'slapadd < /tmp/something.ldif'
     creates '/var/lib/slapd/uid.bdb'
     action :nothing
   end
   
   template '/tmp/something.ldif' do
     source 'something.ldif'
     notifies :run, 'execute[slapadd]', :immediately
   end

where

* ``'/tmp/something.ldif'`` specifies the location of the file
* ``'something.ldif'`` specifies template file from which ``/tmp/something.ldif`` is created
* ``'slapadd < /tmp/something.ldif'`` is the command that is run
* ``/var/lib/slapd/uid.bdb`` prevents the |resource execute| resource block from running if that file already exists

The full syntax for all of the attributes that are available to the |resource execute| resource is:

.. code-block:: ruby

   execute 'name' do
     command                    String, Array  # defaults to 'name' if not specified
     creates                    String
     cwd                        String
     environment                Hash
     group                      String, Integer
     path                       Array # do not use
     provider                   Chef::Provider::Execute
     returns                    Integer, Array
     timeout                    Integer, Float
     user                       String, Integer
     umask                      String, Integer
     action                     Symbol # defaults to :run if not specified
   end

where 

* ``execute`` is the resource
* ``name`` is the name of the resource block
* ``command`` is the command to be run
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``atomic_update``, ``backup``, ``cookbook``, ``force_unlink``, ``group``, ``helper``, ``helpers``, ``inherits``, ``local``, ``manage_symlink_source``, ``mode``, ``owner``, ``path``, ``provider``, ``rights``, ``source``, ``variables``, and ``verify`` are attributes of this resource, with example values shown. |see attributes|
