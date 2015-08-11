.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A ``aws_key_pair`` resource block manages key pairs. For example:

.. code-block:: ruby

   aws_key_pair 'name' do
     private_key_options({
       :format => :pem,
       :type => :rsa,
       :regenerate_if_different => true
     })
     allow_overwrite true
   end

The full syntax for all of the properties that are available to the ``aws_key_pair`` resource is:

.. code-block:: ruby

   aws_key_pair 'name' do
     allow_overwrite               TrueClass, FalseClass
     private_key_options()         Hash
     private_key_path              String
     public_key_path               String      
   end

where 

* ``aws_key_pair`` is the resource
* ``name`` is the name of the resource block
* ``allow_overwrite`` and ``private_key_options`` are properties of this resource, with the |ruby| type shown. |see attributes|
