.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A role is defined using |json| or the |ruby| DSL. |chef solo| will look for roles in ``/var/chef/roles``, but this location can be modified by changing the setting in |solo rb|. For example, the following setting in |solo rb|:

.. code-block:: ruby

   role_path "/var/chef-solo/roles"

Role data looks like the following in |json|:

.. code-block:: javascript

   {
     "name": "test",
     "default_attributes": { },
     "override_attributes": { },
     "json_class": "Chef::Role",
     "description": "This is just a test role, no big deal.",
     "chef_type": "role",
     "run_list": [ "recipe[test]" ]
   }

and like the following in the |ruby| DSL:

.. code-block:: ruby

   name 'test'
   description 'This is just a test role, no big deal.'
   run_list 'recipe[test]'

and finally, |json| data passed to |chef solo|:

.. code-block:: ruby

   { "run_list": "role[test]" }
