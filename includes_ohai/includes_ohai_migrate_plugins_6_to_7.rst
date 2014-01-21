.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|ohai 7| is backwards compatible with existing |ohai 6| plugins; however, none of the new (or future) functionality will be made available to |ohai 6| plugins. It is recommended that all |ohai 6| plugins be updated for new DSL behavior in |ohai 7| as soon as possible. When migrating |ohai| 6 plugins to |ohai 7|, consider the following:

* Pick a name for the existing plugin, and then define it as an |ohai 7| plugin
* Convert the ``required_plugin()`` calls to ``depends`` statements
* Move the |ohai 6| plugin logic into a ``collect_data()`` block

For example, |ohai 7|:

.. code-block:: ruby

   provides 'my_app'
   
   require_plugin("kernel")
   
   my_app Mash.new
   my_app[:version] = shell_out("my_app -v").stdout
   my_app[:message] = "Using #{kernel[:version]}"

and then |ohai 7|:

.. code-block:: ruby

   Ohai.plugin(:MyAPP) do
     provides 'my_app'
     depends 'kernel'
   
     collect_data do
       my_app Mash.new
       my_app[:version] = shell_out("my_app -v").stdout
       my_app[:message] = "Using #{kernel[:version]}"
     end
   end

