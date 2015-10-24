.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Custom resources are designed to use core resources that are built into |chef|. In some cases, it may be necessary to specify a property in the custom resource that is the same as a property in a core resource, for the purpose of overriding that property when used with the custom resource. For example:

.. code-block:: ruby

   class Chef
     class Resource::NodeExecute < ChefCompat::Resource
       resource_name :node_execute
   
       property :command, kind_of: String, name_property: true
       property :version, kind_of: String
   
       # Useful properties from the `execute` resource
       property :cwd, kind_of: String
       property :environment, kind_of: Hash, default: {}
       property :user, kind_of: [String, Integer]
       property :sensitive, kind_of: [TrueClass, FalseClass], default: false
   
       prefix = '/opt/languages/node'
   
       load_current_value do
         current_value_does_not_exist! if node.run_state['nodejs'].nil?
         version node.run_state['nodejs'][:version]
       end
   
       action :run do
         execute 'execute-node' do
           cwd cwd
           environment environment
           user user
           sensitive sensitive
           # gsub replaces 10+ spaces at the beginning of the line with nothing
           command <<-CODE.gsub(/^ {10}/, '')
             #{prefix}/#{version}/#{command}
           CODE
         end
       end
     end
   end

where the ``property :cwd``, ``property :environment``, ``property :user``, and ``property :sensitive`` are identical to properties in the |resource execute| resource, embedded as part of the ``action :run`` action. Because both the custom properties and the |resource execute| properties are identical, this will result in an error message similar to:

.. code-block:: ruby

   ArgumentError
   -------------
   wrong number of arguments (0 for 1)

To prevent this behavior, use ``new_resource.`` to tell the |chef client| to process the properties from the core resource instead of the properties in the custom resource. For example:

.. code-block:: ruby

   class Chef
     class Resource::NodeExecute < ChefCompat::Resource
       resource_name :node_execute
   
       property :command, kind_of: String, name_property: true
       property :version, kind_of: String
   
       # Useful properties from the `execute` resource
       property :cwd, kind_of: String
       property :environment, kind_of: Hash, default: {}
       property :user, kind_of: [String, Integer]
       property :sensitive, kind_of: [TrueClass, FalseClass], default: false
  
       prefix = '/opt/languages/node'
   
       load_current_value do
         current_value_does_not_exist! if node.run_state['nodejs'].nil?
         version node.run_state['nodejs'][:version]
       end
   
       action :run do
         execute 'execute-node' do
           cwd new_resource.cwd
           environment new_resource.environment
           user new_resource.user
           sensitive new_resource.sensitive
           # gsub replaces 10+ spaces at the beginning of the line with nothing
           command <<-CODE.gsub(/^ {10}/, '')
             #{prefix}/#{new_resource.version}/#{new_resouce.command}
           CODE
         end
       end
     end
   end

where ``cwd new_resource.cwd``, ``environment new_resource.environment``, ``user new_resource.user``, and ``sensitive new_resource.sensitive`` correctly use the properties of the |resource execute| resource and not the identically-named override properties of the custom resource.
