.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the ``aws_ebs_volume`` driver-specific resource is as follows:

.. code-block:: ruby

   aws_ebs_volume 'name' do
     availability_zone             'string'
     device                        'string'
     encrypted                     true
     iops                          integer
     machine                       'string'
     size                          integer
     snapshot                      'string'
     volume_id                     'string'
     volume_type                   'string'
   end

where 

* ``aws_ebs_volume`` is the resource
* ``name`` is the name of the resource block and also the name of a block-level storage device that is attached to an |amazon ec2| instance
* ``availability_zone``, ``device``, ``encrypted``, ``iops``, ``machine``, ``size``, and ``volume_type`` are attributes of this resource, with example values shown. |see attributes|

**Example**

.. code-block:: ruby

   aws_ebs_volume 'name' do
     machine 'ref-machine1'
     availability_zone 'a'
     size 100
     iops 3000
     volume_type 'io1'
     encrypted true
     device '/dev/sda2'
     aws_tags :chef_type => "aws_ebs_volume"
   end
