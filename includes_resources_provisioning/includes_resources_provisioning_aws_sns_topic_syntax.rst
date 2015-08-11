.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A ``aws_sns_topic`` resource block manages topics in |amazon sns|. For example:

.. code-block:: ruby

   aws_sns_topic 'seapower' do
     arn 'arn:aws:sns:us-west-1:5060091557628:seapower'
   end

The full syntax for all of the properties that are available to the ``aws_sns_topic`` resource is:

.. code-block:: ruby

   aws_sns_topic 'name' do
     arn                           String
   end

where

* ``aws_sns_topic`` is the resource
* ``name`` is the name of the resource block and also the name of a topic in |amazon sns|
* ``arn`` and ``name`` are attributes of this resource, with the |ruby| type shown. |see attributes|
