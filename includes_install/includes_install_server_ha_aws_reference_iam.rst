.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following example shows |amazon iam| access management settings that are required for |chef ha|:

.. code-block:: javascript

   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Action": [
           "ec2:DescribeInstances",
           "ec2:DescribeVolumes",
           "ec2:AttachVolume",
           "ec2:DetachVolume",
           "ec2:AssignPrivateIpAddresses"
         ],
         "Resource": [
           "*"
         ]
       }
     ]
   }

It is possible to further restrict access using a more sophisticated policy document. For example, administrators may choose to permit the |amazon iam| user only to attach/detach the volume ID associated with the |chef server| data volume, and not all volumes.
