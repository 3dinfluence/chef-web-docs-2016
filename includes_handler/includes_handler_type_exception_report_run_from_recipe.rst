.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The |resource chef_handler| resource allows exception and report handlers to be enabled from within recipes, which can then added to the run-list for any node on which the exception or report handler should run. The |resource chef_handler| resource is available from the |cookbook chef_handler| cookbook.

To use the |resource chef_handler| resource in a recipe, add code similar to the following:

.. code-block:: ruby

   chef_handler 'name_of_handler' do
     source '/path/to/handler/handler_name'
     action :enable
   end

For example, a handler for |growl| needs to be enabled at the beginning of the |chef client| run:

.. code-block:: ruby

   chef_gem 'chef-handler-growl'

and then is activated in a recipe by using the |resource chef_handler| resource:

.. code-block:: ruby

   chef_handler 'Chef::Handler::Growl' do
     source 'chef/handler/growl'
     action :enable
   end
