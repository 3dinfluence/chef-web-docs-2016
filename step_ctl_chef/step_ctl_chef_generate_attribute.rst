.. This is an included how-to. 


To generate an attribute, run a command similar to:

.. code-block:: bash

   $ chef generate attribute /path/to/cookbook FOO
   
will return something similar to:

.. code-block:: bash

   Recipe: code_generator::attribute
     * directory[/Users/grantmc/chef-repo/cookbooks/chef-repo/attributes] action create
       - create new directory /Users/grantmc/chef-repo/cookbooks/chef-repo/attributes
   
     * template[/Users/grantmc/chef-repo/cookbooks/chef-repo/attributes/FOO.rb] action create
       - create new file /Users/grantmc/chef-repo/cookbooks/chef-repo/attributes/FOO.rb
