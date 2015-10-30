.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

An ``apache_conf`` |inspec resource| block declares configuration settings that should be tested:

.. code-block:: ruby

   describe apache_conf('path') do
     its('setting_name') { should eq 'value' }
   end

where

* ``'setting_name'`` is a configuration setting defined in the |apache| configuration file
* ``('path')`` is the non-default path to the |apache| configuration file
* ``{ should eq 'value' }`` is the value that is expected
