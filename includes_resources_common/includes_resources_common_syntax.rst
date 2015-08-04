.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A resource is a |ruby| block with four components: a type, a name, one (or more) properties (with values), and one (or more) actions. The syntax for a resource is like this:

.. code-block:: ruby

   type 'name' do
      attribute 'value'
      action :type_of_action
   end

Every resource has its own set of actions and properties. Most properties have default values. Some properties are available to all resources, for example those used to send notifications to other resources and guards that help ensure that some resources are idempotent. 

For example, a resource that is used to install a |tar gz| package for version 1.16.1 may look something like this:

.. code-block:: ruby

   package 'tar' do
     version '1.16.1'
     action :install
   end

All actions have a default value. Only non-default behaviors of actions and properties need to be specified. For example, the |resource package| resource's default action is ``:install`` and the name of the package defaults to the ``name`` of the resource. Therefore, it is possible to write a resource block that installs the latest |tar gz| package like this:

.. code-block:: ruby

   package 'tar'

and a resource block that installs a |tar gz| package for version 1.6.1 like this:

.. code-block:: ruby

   package 'tar' do
     version '1.16.1'
   end
   
In both cases, the |chef client| will use the default action (``:install``) to install the ``tar`` package.
