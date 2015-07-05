.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |resource batch| resource block executes a batch script using the |windows cmd exe| interpreter:

.. code-block:: ruby

   batch 'echo some env vars' do
     code <<-EOH
       echo %TEMP%
       echo %SYSTEMDRIVE%
       echo %PATH%
       echo %WINDIR%
       EOH
   end

The full syntax for all of the attributes that are available to the |resource batch| resource is:

.. code-block:: ruby

   batch 'name' do
     architecture               Symbol
     code                       String
     command                    String, Array # defaults to 'name' if not specified
     creates                    String
     cwd                        String
     flags                      String
     group                      String, Integer
     notifies                   # see description
     provider                   Chef::Provider::Batch
     returns                    Integer, Array
     subscribes                 # see description
     timeout                    Integer, Float
     user                       String, Integer
     action                     Symbol # defaults to :run if not specified
   end

where 

* ``batch`` is the resource
* ``name`` is the name of the resource block
* ``command`` is the command to be run and ``cwd`` is the location from which the command is run
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``architecture``, ``code``, ``command``, ``creates``, ``cwd``, ``flags``, ``group``, ``provider``, ``returns``, ``timeout``, and ``user`` are attributes of this resource, with the |ruby| type shown. |see attributes|
