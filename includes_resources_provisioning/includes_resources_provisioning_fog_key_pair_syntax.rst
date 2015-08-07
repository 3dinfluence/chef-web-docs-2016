.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the ``fog_key_pair`` driver-specific resource is as follows:

.. code-block:: ruby

   fog_key_pair 'name' do
     allow_overwrite         TrueClass, FalseClass
     driver                  Chef::Provisioning::Driver
     private_key_options     Hash
     private_key_path        String
     public_key_path         String
   end

where 

* ``fog_key_pair`` is the resource
* ``name`` is the name of the resource block and also the name of an instance in |amazon ec2|
* ``allow_overwrite``, ``driver``, ``private_key_options``, ``private_key_path``, and ``public_key_path`` are properties of this resource, with the |ruby| type shown. |see attributes|

**Example**

.. code-block:: ruby

   fog_key_pair 'name' do
     private_key_options({
       :format => :pem,
       :type => :rsa,
       :regenerate_if_different => true
     })
     allow_overwrite true
   end
