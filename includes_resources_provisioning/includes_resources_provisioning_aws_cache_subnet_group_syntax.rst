.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the ``aws_cache_subnet_group`` driver-specific resource is as follows:

.. code-block:: ruby

   aws_cache_subnet_group 'name' do
     description 'Description of cache subnet group.'
     subnets [ 'subnet', 'subnet' ]
   end

where 

* ``aws_cache_subnet_group`` is the resource
* ``name`` is the name of the resource block (and is the same as the ``group_name`` attribute if ``group_name`` is not specified in the resource block)
* ``description`` and ``subnets`` are attributes of this resource, with example values shown. |see attributes|
