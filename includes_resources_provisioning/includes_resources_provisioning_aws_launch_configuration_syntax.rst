.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the ``aws_launch_configuration`` driver-specific resource is as follows:

.. code-block:: ruby

   aws_launch_configuration 'ref-launch-configuration' do
     image                         'string'
     instance_type                 'string'
     options                       Hash
   end

where 

* ``aws_launch_configuration`` is the resource
* ``name`` is the name of the resource block and also the name of an |amazon ami| instance type
* ``image``, ``instance_type``, and ``options`` are attributes of this resource, with example values shown. |see attributes|

**Example**

.. code-block:: ruby

   aws_launch_configuration 'ref-launch-configuration' do
     image 'ref-machine_image1'
     instance_type 't1.micro'
     options security_groups: 'ref-sg1'
   end
