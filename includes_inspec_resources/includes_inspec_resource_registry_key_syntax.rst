.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A ``registry_key`` |inspec resource| block declares the item in the |windows| registry, the path to a setting under that item, and then one (or more) name/value pairs to be tested:

.. code-block:: ruby

   describe registry_key('registry_item', 'path\to\key') do
     its('name') { should eq 'value' }
   end

or:

.. code-block:: ruby

   describe registry_key('path\to\key') do
     its('name') { should eq 'value' }
   end

where

* ``'registry_item'`` is a key in the |windows| registry (optional)
* ``'path\to\key'`` is the path in the |windows| registry
* ``('name')`` and ``'value'`` represent the name of the key and the value assigned to that key
