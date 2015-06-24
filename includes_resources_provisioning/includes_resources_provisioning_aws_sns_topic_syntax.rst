.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the ``aws_sns_topic`` driver-specific resource is as follows:

.. code-block:: ruby

   aws_sns_topic 'name' do
     arn                           'string'
   end

where

* ``aws_sns_topic`` is the resource
* ``name`` is the name of the resource block and also the name of a topic in |amazon sns|
* ``arn`` and ``name`` are attributes of this resource, with example values shown. |see attributes|

**Example**

.. code-block:: ruby

   aws_sns_topic 'seapower' do
     arn 'arn:aws:sns:us-west-1:5060091557628:seapower'
   end
