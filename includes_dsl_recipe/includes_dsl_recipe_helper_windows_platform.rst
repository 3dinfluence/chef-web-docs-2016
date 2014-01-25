.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A recipe can define specific behaviors for specific |windows| platform versions by using a series of helper methods. To enable these helper methods, add the following to the recipe:

.. code-block:: ruby

   require 'chef/win32/version'

Then declare a variable using the ``Chef::ReservedNames::Win32::Version`` class:

.. code-block:: ruby

   variable_name = Chef::ReservedNames::Win32::Version.new

Then use the variable to define specific behaviors for specific |windows| platform versions. For example:

.. code-block:: ruby

   if variable_name.helper_name?
     # Ruby code goes here, such as
     resource_name do
       # resource block
     end

   elsif variable_name.helper_name?
     # Ruby code goes here
     resource_name do
       # resource block for something else
     end

   else variable_name.helper_name?
     # Ruby code goes here, such as
     log 'log entry' do
       level :level
     end
   
   end

