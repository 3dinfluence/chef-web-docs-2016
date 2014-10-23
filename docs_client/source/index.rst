.. THIS PAGE IS LOCATED AT THE /client/ PATH.

=====================================================
All about the |chef client_title| ... 
=====================================================

.. include:: ../../includes_chef/includes_chef_index.rst

Getting Started
=====================================================
If you are new to the |chef client|, familiarize yourself with :doc:`all of the components the chef-client will interact with </chef_overview>` as it configures your infrastructure.

Cookbooks are the fundamental unit of configuration and policy distribution. Cookbooks are authored using a programming language called |ruby|. Being an expert in |ruby| is not a requirement, but knowing some basic |ruby| will help you a lot. If you're new to |ruby|, :doc:`familiarize yourself with the basics </just_enough_ruby_for_chef>`.

If you want to try out |chef server osc|, use the hosted |chef server|. After you have access to a |chef server|, then :doc:`install the chef-client on a workstation </install_workstation>`, and then :doc:`bootstrap your first node </install_bootstrap>`.

A good way to learn how to use |chef server osc| is the |learnchef| website. It contains a `series of hands-on tutorials <https://learnchef.getchef.com/>`_ that can walk you through the process of setting up a hosted server, a workstation, using the |chef repo|, and then converging your first node.


The Workstation
=====================================================
The workstation is the location from which most users will do most of their work. This work includes:

* Developing `cookbooks <http://docs.getchef.com/client/essentials_cookbooks.html>`_ and :doc:`recipes </essentials_cookbook_recipes>` (and authoring them using :doc:`using Ruby </just_enough_ruby_for_chef>`), including :doc:`debugging recipes </chef_shell>`
* Synchronizing the :doc:`chef-repo </essentials_repository>` with version source control like |git| or |svn|
* Using |knife| to upload items from the |chef repo| to the |chef server|
* Configuring :doc:`organizational policy </essentials_policy>`
* :doc:`Defining roles </essentials_roles>` and :doc:`environments </essentials_environments>`
* Ensuring that critical data is stored in :doc:`data bags </essentials_data_bags>`
* Interacting with nodes, such as performing a :doc:`bootstrap operation </install_bootstrap>` or running the :doc:`chef-client </ctl_chef_client>` remotely

Set up a Workstation
-----------------------------------------------------
A workstation must be configured with a |chef client|, must have access to a |chef repo|, and must be able to issue |knife| commands to the |chef server| to complete certain tasks, such as uploading data to the |chef server| or issuing bootstrap commands to install the |chef client| on nodes.

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_repository_create.html">Create and Sync the chef-repo</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/install_workstation.html">Set up a Workstation</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/install_bootstrap.html">Bootstrap a Node</a> </br>

|knife_title|
-----------------------------------------------------
|knife| is a command-line tool that provides an interface between a local |chef repo| and the |chef server|. All |knife| subcommands share a set of :doc:`common options </knife_common_options>` and :doc:`usage patterns </knife_using>`. 

The following |knife| subcommands are built-in:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_bootstrap.html">knife bootstrap</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_client.html">knife client</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_configure.html">knife configure</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_cookbook.html">knife cookbook</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_cookbook_site.html">knife cookbook site</a> (<a href="http://docs.getchef.com/client/api_cookbooks_site.html">which uses the Cookbooks Site API</a>)</br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_data_bag.html">knife data bag</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_delete.html">knife delete</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_deps.html">knife deps</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_diff.html">knife diff</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_download.html">knife download</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_edit.html">knife edit</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_environment.html">knife environment</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_exec.html">knife exec</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_index_rebuild.html">knife index rebuild</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_list.html">knife list</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_node.html">knife node</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_raw.html">knife raw</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_recipe_list.html">knife recipe list</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_role.html">knife role</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_search.html">knife search</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_show.html">knife show</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_ssh.html">knife ssh</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_ssl_check.html">knife ssl check</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_ssl_fetch.html">knife ssl fetch</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_status.html">knife status</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_tag.html">knife tag</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_upload.html">knife upload</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_user.html">knife user</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/knife_xargs.html">knife xargs</a> </br>

|knife| settings are stored in the :doc:`knife.rb </config_rb_knife>` file. There is a default |knife rb| file and there are :doc:`optional settings </config_rb_knife_optional_settings>` that can be added to the |knife rb| file.

|knife_title| Cloud Plugins
-----------------------------------------------------
Plugins allow |knife| to interact with all of the major cloud providers. All |knife| plugins share the same set of :doc:`common options </knife_common_options>` and built-in |knife| subcommands, plus |knife| plugins can make :doc:`authenticated API requests </plugin_knife_authenticated_requests>` to the |chef server|.

.. include:: ../../includes_plugin_knife/includes_plugin_knife_chef_maintained_index_list.rst

A number of |knife| plugins are `built and maintained by the community <http://docs.getchef.com/client/community_plugin_knife.html>`_. In addition, `custom Knife plugins <http://docs.getchef.com/client/plugin_knife_custom.html>`_ can be created.

Settings and Tools
-----------------------------------------------------
The following settings files are used to configure behavior for |knife| and how it interacts with nodes and the |chef server|:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/config_rb_knife.html">knife.rb</a> </br>

The following command-line tools can be run on the workstation to simulate a |chef client| run locally:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ctl_chef_apply.html">chef-apply</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ctl_chef_shell.html">chef-shell</a> </br>


The |chef server_title|
=====================================================
.. include:: ../../includes_chef_server/includes_chef_server.rst

For more information about the |chef server| see docs.getchef.com/server/.

The Nodes
=====================================================
.. include:: ../../includes_node/includes_node.rst

About the |chef client_title|
-----------------------------------------------------
The |chef client| does the actual configuration on :doc:`the nodes </essentials_nodes>`. The |chef client| receives its instructions from cookbooks (:doc:`recipes </essentials_cookbook_recipes>`, mostly). The process of configuring a node is called :doc:`the chef-client run </essentials_nodes_chef_run>`. At the beginning of each run, the |chef client| :doc:`validates to the server </essentials_chef_client>`, :doc:`collects important data about that node </ohai>`, and then configures the node. At the end of each run, the |chef client| :doc:`reports the successes and failures that may have occurred </handlers>`.

Be sure to :doc:`test and debug your recipes </chef_shell>` before running them in production! Run the |chef client| in :doc:`why-run mode </essentials_nodes_why_run>` to simulate what should happen during the |chef client| run, but without configuring anything.

Install the |chef client_title|
-----------------------------------------------------
The |chef client| is typically installed using a :doc:`bootstrap operation </essentials_nodes_bootstrap>`. This is done by running the :doc:`knife bootstrap </knife_bootstrap>` subcommand from a workstation. Alternately, the |chef client| can be downloaded to a node directly using the |api omnitruck|.

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/install_bootstrap.html">Install the chef-client with a bootstrap</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/api_omnitruck.html">Download the chef-client using the Omnitruck API</a> </br>


Settings and Tools
-----------------------------------------------------
The following settings files are used to configure behavior for the |chef client|:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/config_rb_client.html">client.rb</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/config_rb_solo.html">solo.rb</a> </br>

|ohai| collects important data about every node:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ohai.html">About Ohai</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ohai_custom.html">Build Custom Ohai Plugins</a> </br>

The following command-line tools can be run on any node:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ctl_chef_client.html">chef-client</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ctl_chef_solo.html">chef-solo</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/ctl_ohai.html">ohai</a> </br>


Cookbooks
=====================================================
A cookbook is the fundamental unit of configuration and policy distribution. A cookbook defines a scenario and contains all of the components that are required to support that scenario.

.. :doc:`metadata.rb </config_rb_metadata>`

Cookbook Essentials
-----------------------------------------------------
A cookbook is made up of the following components: attribute files, definitions, files, libraries, metadata, recipes, resources and providers, templates, and versions.

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_attribute_files.html">Attribute Files</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_definitions.html">Definitions</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_files.html">Files</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/handlers.html">Handlers</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_libraries.html">Libraries</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_metadata.html">Metadata</a> (and <a href="http://docs.getchef.com/client/config_rb_metadata.html">/cookbook directory settings</a>)</br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_recipes.html">Recipes</a> (and the <a href="http://docs.getchef.com/client/dsl_recipe.html">Recipe DSL</a>)</br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_resources.html">Resources and Providers</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_templates.html">Templates</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/essentials_cookbook_versions.html">Versions</a> </br>

Resources
-----------------------------------------------------
A :doc:`resource </resource>` is a key part of a recipe that defines the actions that may be taken by the |chef client|. All resources share :doc:`common functionality </resource_common>`: 

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#actions">Actions</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#attributes">Attributes</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#guards">Guards</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#notifications">Notifications</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#relative-paths">Relative Paths</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#windows-file-security">Windows File Security</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_common.html#run-from-resource-collection">Run During Resource Compilation</a> </br>

The following resources are built-in and can be used in any recipe:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_apt_package.html">apt_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_bash.html">bash</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_batch.html">batch</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_breakpoint.html">breakpoint</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_chef_gem.html">chef_gem</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_chef_handler.html">chef_handler</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_cookbook_file.html">cookbook_file</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_cron.html">cron</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_deploy.html">deploy</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_directory.html">directory</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_dpkg_package.html">dpkg_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_easy_install_package.html">easy_install_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_env.html">env</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_erlang_call.html">erl_call</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_execute.html">execute</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_file.html">file</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_gem_package.html">gem_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_git.html">git</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_group.html">group</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_http_request.html">http_request</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_ifconfig.html">ifconfig</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_link.html">link</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_log.html">log</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_mdadm.html">mdadm</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_mount.html">mount</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_ohai.html">ohai</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_package.html">package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_powershell_script.html">powershell_script</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_registry_key.html">registry_key</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_remote_directory.html">remote_directory</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_remote_file.html">remote_file</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_route.html">route</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_rpm_package.html">rpm_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_ruby_block.html">ruby_block</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_script.html">script</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_service.html">service</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_subversion.html">subversion</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_template.html">template</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_user.html">user</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_windows_package.html">windows_package</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/resource_yum.html">yum_package</a> </br>

LWRPs 
-----------------------------------------------------
A :doc:`LWRP </lwrp>` is an extension of the |chef client| that behaves much like a platform resource, including sharing all of the common functionality available to platform resources. A |lwrp| is created by defining a lightweight resource and a lightweight provider:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/lwrp_custom.html">About custom LWRPs</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/lwrp_custom_resource.html">Create a lightweight resource</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/lwrp_custom_provider.html">Create a lightweight provider using platform resources</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/lwrp_custom_provider_ruby.html">Create a lightweight provider using Ruby</a> </br>

.. include:: ../../includes_lwrp/includes_lwrp_chef_maintained_index_list.rst

See the `opscode-cookbooks <https://github.com/opscode-cookbooks>`_ repository for the full list.

The |dsl recipe|
-----------------------------------------------------
The :doc:`Recipe DSL </dsl_recipe>` is used to declare resources in recipes. The |chef client| relies on recipes to know what action(s) to take as it is configuring a node. The |dsl recipe| contains the following methods:

.. raw:: html

   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_attribute.html">attribute?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_cookbook_name.html">cookbook_name</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_data_bag.html">data_bag</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_data_bag_item.html">data_bag_item</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_platform.html">platform?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_platform_family.html">platform_family?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_reboot_pending.html">reboot_pending?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_recipe_name.html">recipe_name</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_data_exists.html">registry_data_exists?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_get_subkeys.html">registry_get_subkeys</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_get_values.html">registry_get_values</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_has_subkeys.html">registry_has_subkeys?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_key_exists.html">registry_key_exists?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_registry_value_exists.html">registry_value_exists?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_resources.html">resources</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_search.html">search</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_tag.html">tag</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_tag.html">tagged?</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_tag.html">untag</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_value_for_platform.html">value_for_platform</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_method_value_for_platform_family.html">value_for_platform_family</a> </br>
   &nbsp;&nbsp;&nbsp;   <a href="http://docs.getchef.com/client/dsl_recipe_helper_windows_platform.html">Microsoft Windows Platform Helpers</a> </br>


.. Hide the TOC from this file.

.. toctree::
   :hidden:

   api_chef_server
   api_omnitruck
   auth_authentication
   auth_authorization
   chef_client
   chef_overview
   chef_shell
   chef_solo
   config_rb_client
   config_rb_knife
   config_rb_knife_optional_settings
   config_rb_metadata
   config_rb_solo
   ctl_chef_apply
   ctl_chef_client
   ctl_chef_shell
   ctl_chef_solo
   ctl_ohai
   dsl_recipe
   dsl_recipe_helper_windows_platform
   dsl_recipe_method_attribute
   dsl_recipe_method_cookbook_name
   dsl_recipe_method_data_bag
   dsl_recipe_method_data_bag_item
   dsl_recipe_method_platform
   dsl_recipe_method_platform_family
   dsl_recipe_method_reboot_pending
   dsl_recipe_method_recipe_name
   dsl_recipe_method_registry_data_exists
   dsl_recipe_method_registry_get_subkeys
   dsl_recipe_method_registry_get_values
   dsl_recipe_method_registry_has_subkeys
   dsl_recipe_method_registry_key_exists
   dsl_recipe_method_registry_value_exists
   dsl_recipe_method_resources
   dsl_recipe_method_search
   dsl_recipe_method_tag
   dsl_recipe_method_value_for_platform
   dsl_recipe_method_value_for_platform_family
   essentials_chef_client
   essentials_cookbook_attribute_files
   essentials_cookbook_definitions
   essentials_cookbook_directory
   essentials_cookbook_files
   essentials_cookbook_libraries
   essentials_cookbook_metadata
   essentials_cookbook_recipes
   essentials_cookbook_resources
   essentials_cookbook_templates
   essentials_cookbook_versions
   essentials_cookbooks
   essentials_data_bags
   essentials_environments
   essentials_node_object
   essentials_node_object_run_lists
   essentials_nodes
   essentials_nodes_bootstrap
   essentials_nodes_chef_run
   essentials_nodes_why_run
   essentials_policy
   essentials_repository
   essentials_repository_create
   essentials_roles
   essentials_search
   handlers
   install
   install_bootstrap
   install_windows
   install_workstation
   just_enough_ruby_for_chef
   knife_bootstrap
   knife_client
   knife_common_options
   knife_configure
   knife_cookbook
   knife_cookbook_site
   knife_data_bag
   knife_delete
   knife_deps
   knife_diff
   knife_download
   knife_edit
   knife_environment
   knife_exec
   knife_index_rebuild
   knife_list
   knife_node
   knife_raw
   knife_recipe_list
   knife_role
   knife_search
   knife_show
   knife_ssh
   knife_ssl_check
   knife_ssl_fetch
   knife_status
   knife_tag
   knife_upload
   knife_user
   knife_using
   knife_xargs
   lwrp
   lwrp_custom
   lwrp_custom_provider
   lwrp_custom_provider_ruby
   lwrp_custom_resource
   lwrp_custom_resource_library
   ohai
   plugin_knife_authenticated_requests
   plugin_knife_custom
   resource
   resource_apt_package
   resource_bash
   resource_batch
   resource_breakpoint
   resource_chef_gem
   resource_chef_handler
   resource_common
   resource_cookbook_file
   resource_cron
   resource_csh
   resource_deploy
   resource_directory
   resource_dpkg_package
   resource_easy_install_package
   resource_env
   resource_erlang_call
   resource_execute
   resource_file
   resource_freebsd_package
   resource_gem_package
   resource_git
   resource_group
   resource_http_request
   resource_ifconfig
   resource_ips_package
   resource_link
   resource_log
   resource_macports_package
   resource_mdadm
   resource_mount
   resource_ohai
   resource_package
   resource_pacman_package
   resource_perl
   resource_portage_package
   resource_powershell_script
   resource_python
   resource_registry_key
   resource_remote_directory
   resource_remote_file
   resource_route
   resource_rpm_package
   resource_ruby
   resource_ruby_block
   resource_scm
   resource_script
   resource_service
   resource_smartos_package
   resource_solaris_package
   resource_subversion
   resource_template
   resource_user
   resource_windows_package
   resource_yum

