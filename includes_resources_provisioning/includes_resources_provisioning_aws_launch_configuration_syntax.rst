.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A ``aws_launch_configuration`` resource block manages launch configurations. For example:

.. code-block:: ruby

   aws_launch_configuration 'ref-launch-configuration' do
     image 'ref-machine_image1'
     instance_type 't1.micro'
     options security_groups: 'ref-sg1'
   end

The full syntax for all of the properties that are available to the ``aws_launch_configuration`` resource is:

.. code-block:: ruby

   aws_launch_configuration 'ref-launch-configuration' do
     image                         String
     instance_type                 String
     options                       Hash
   end

where 

* ``aws_launch_configuration`` is the resource
* ``name`` is the name of the resource block and also the name of an |amazon ami| instance type
* ``image``, ``instance_type``, and ``options`` are properties of this resource, with the |ruby| type shown. |see attributes|
