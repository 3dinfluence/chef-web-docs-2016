=====================================================
Docs for |chef client| 12.0
=====================================================

.. include:: ../../includes_chef/includes_chef_index.rst

View the :doc:`release notes </release_notes>` for |chef client| 12.0.

Getting Started
=====================================================
**From the beginning:** :doc:`Overview (long) </chef_overview>`

.. **Key concepts:** :doc:`Workstations </chef_overview_workstation>` | :doc:`The Server </chef_overview_server>` | :doc:`Nodes </chef_overview_nodes>` | :doc:`Cookbooks </chef_overview_cookbooks>` | :doc:`Attributes </chef_overview_attributes>` | :doc:`Resources and Providers </resource>` | :doc:`LWRPs (Custom Resources) </lwrp_custom>` | :doc:`Knife </knife>`

.. **Using Ruby:** :doc:`Just Enough Ruby for Chef </just_enough_ruby_for_chef>`

.. .. include:: ../../includes_chef/includes_chef_index_getchef.rst

.. .. include:: ../../includes_chef/includes_chef_index_learnchef.rst


.. The Community
.. =====================================================
.. .. include:: ../../includes_chef/includes_chef_index_community.rst

The Workstation
=====================================================

.. **The Basics:** :doc:`About the Workstation </chef_overview_workstation>` | :doc:`The chef-repo </essentials_repository>` | :doc:`Knife </knife>` | :doc:`Debug Recipes </chef_shell>`

.. **Install:** :doc:`Install the chef-client on a Workstation </install_workstation>` | :doc:`Bootstrap a Node </install_bootstrap>` | :doc:`Create and Sync the chef-repo </essentials_repository_create>`

**Knife:** :doc:`About Knife </knife>` | :doc:`Common Options </knife_common_options>` | :doc:`Working with Knife </knife_using>` --- **Commands:** :doc:`bootstrap </knife_bootstrap>` | :doc:`client </knife_client>` | :doc:`configure </knife_configure>` | :doc:`cookbook </knife_cookbook>` | :doc:`cookbook site </knife_cookbook_site>` | :doc:`data bag </knife_data_bag>` | :doc:`delete </knife_delete>` | :doc:`deps </knife_deps>` | :doc:`diff </knife_diff>` | :doc:`download </knife_download>` | :doc:`edit </knife_edit>` | :doc:`environment </knife_environment>` | :doc:`exec </knife_exec>` | :doc:`list </knife_list>` | :doc:`node </knife_node>` | :doc:`raw </knife_raw>` | :doc:`recipe list </knife_recipe_list>` | :doc:`role </knife_role>` | :doc:`search </knife_search>` | :doc:`serve </knife_serve>` | :doc:`show </knife_show>` | :doc:`ssh </knife_ssh>` | :doc:`ssl check </knife_ssl_check>` | :doc:`ssl fetch </knife_ssl_fetch>` | :doc:`status </knife_status>` | :doc:`tag </knife_tag>` | :doc:`upload </knife_upload>` | :doc:`user </knife_user>` | :doc:`xargs </knife_xargs>`

.. **Plugins:** :doc:`About Plugins </plugin_knife>` | :doc:`Custom Knife Plugins </plugin_knife_custom>` | :doc:`Authenticated Requests </plugin_knife_authenticated_requests>`

**Settings:** :doc:`knife.rb </config_rb_knife>`

.. | :doc:`metadata.rb </config_rb_metadata>`

.. **Tools:** :doc:`chef-shell (executable) </ctl_chef_shell>` | :doc:`chef-apply (executable) </ctl_chef_apply>`


.. The Nodes
.. =====================================================
.. **The Basics:** :doc:`About Nodes </essentials_nodes>` | :doc:`chef-client (agent) </essentials_chef_client>` | :doc:`The chef-client Run </essentials_nodes_chef_run>` | :doc:`Chef Solo </chef_solo>` | :doc:`Debug Recipes </chef_shell>`

.. **Install:** :doc:`Install the chef-client on a Node (Bootstrap) </install_bootstrap>` and :doc:`knife bootstrap </knife_bootstrap>` | :doc:`Install the chef-client on Windows </install_windows>` | :doc:`Download the chef-client with Omnitruck API </api_omnitruck>`

.. .. include:: ../../includes_chef/includes_chef_index_ohai.rst

.. **Settings:** :doc:`client.rb </config_rb_client>` | :doc:`solo.rb </config_rb_solo>`

.. **Command-line Tools:** :doc:`chef-client (executable) </ctl_chef_client>` | :doc:`chef-shell (executable) </ctl_chef_shell>` | :doc:`chef-solo (executable) </ctl_chef_solo>`


Cookbooks
=====================================================
.. **The Basics:** :doc:`About Cookbooks </essentials_cookbooks>` | :doc:`About Recipes </essentials_cookbook_recipes>` | :doc:`About Attribute Files </essentials_cookbook_attribute_files>` |  :doc:`Handlers </handlers>` | `Popular Cookbooks <https://github.com/opscode-cookbooks>`_

.. **LWRPs:** :doc:`About Custom LWRPs </lwrp_custom>` | :doc:`Lightweight Resources </lwrp_custom_resource>` | :doc:`Lightweight Providers w/Chef Resources </lwrp_custom_provider>` | :doc:`Lightweight Providers w/Custom Ruby </lwrp_custom_provider_ruby>`

.. **Other Cookbook Components:** :doc:`About Definitions </essentials_cookbook_definitions>` | :doc:`About Files </essentials_cookbook_files>` | :doc:`About Libraries </essentials_cookbook_libraries>` | :doc:`About Cookbook Metadata </essentials_cookbook_metadata>` | :doc:`About Templates </essentials_cookbook_templates>` | :doc:`About Versions </essentials_cookbook_versions>`

**The Recipe DSL:** :doc:`About the Recipe DSL </dsl_recipe>` --- **Methods:** :doc:`attribute? </dsl_recipe_method_attribute>` | :doc:`cookbook_name </dsl_recipe_method_cookbook_name>` | :doc:`data_bag </dsl_recipe_method_data_bag>` | :doc:`data_bag_item </dsl_recipe_method_data_bag>` | :doc:`platform? </dsl_recipe_method_platform>` | :doc:`platform_family? </dsl_recipe_method_platform_family>` | :doc:`recipe_name </dsl_recipe_method_recipe_name>` |  :doc:`registry_data_exists? </dsl_recipe_method_registry_data_exists>` | :doc:`registry_get_subkeys </dsl_recipe_method_registry_get_subkeys>` | :doc:`registry_get_values </dsl_recipe_method_registry_get_values>` | :doc:`registry_has_subkeys? </dsl_recipe_method_registry_has_subkeys>` | :doc:`registry_key_exists? </dsl_recipe_method_registry_key_exists>` | :doc:`registry_value_exists? </dsl_recipe_method_registry_value_exists>` | :doc:`resources </dsl_recipe_method_resources>` | :doc:`search </dsl_recipe_method_search>` | :doc:`tag </dsl_recipe_method_tag>` | :doc:`tagged? </dsl_recipe_method_tag>` | :doc:`untag </dsl_recipe_method_tag>` | :doc:`value_for_platform </dsl_recipe_method_value_for_platform>` | :doc:`value_for_platform_family </dsl_recipe_method_value_for_platform_family>` | :doc:`Windows Platform Helper Methods </dsl_recipe_helper_windows_platform>`

**Resources:** :doc:`About Resources </resource>` | :doc:`Common Functionality </resource_common>` --- :doc:`apt_package </resource_apt_package>` | :doc:`bash </resource_bash>` | :doc:`batch </resource_batch>` | :doc:`bff_package </resource_bff_package>` | :doc:`breakpoint </resource_breakpoint>` | :doc:`chef_gem </resource_chef_gem>` | :doc:`chef_handler </resource_chef_handler>` | :doc:`cookbook_file </resource_cookbook_file>` | :doc:`cron </resource_cron>` | :doc:`deploy </resource_deploy>` | :doc:`directory </resource_directory>` | :doc:`dpkg_package </resource_dpkg_package>` | :doc:`dsc_script </resource_dsc_script>` | :doc:`easy_install_package </resource_easy_install_package>` | :doc:`env </resource_env>` | :doc:`erl_call </resource_erlang_call>` | :doc:`execute </resource_execute>` | :doc:`file </resource_file>` | :doc:`gem_package </resource_gem_package>` | :doc:`git </resource_git>` | :doc:`group </resource_group>` | :doc:`homebrew_package </resource_homebrew_package>` | :doc:`http_request </resource_http_request>` | :doc:`ifconfig </resource_ifconfig>` | :doc:`link </resource_link>` | :doc:`log </resource_log>` | :doc:`mdadm </resource_mdadm>` | :doc:`mount </resource_mount>` | :doc:`ohai </resource_ohai>` | :doc:`package </resource_package>` | :doc:`powershell_script </resource_powershell_script>` | :doc:`reboot </resource_reboot>` | :doc:`registry_key </resource_registry_key>` | :doc:`remote_directory </resource_remote_directory>` | :doc:`remote_file </resource_remote_file>` | :doc:`route </resource_route>` | :doc:`rpm_package </resource_rpm_package>` | :doc:`ruby_block </resource_ruby_block>` | :doc:`script </resource_script>` | :doc:`service </resource_service>` | :doc:`subversion </resource_subversion>` | :doc:`template </resource_template>` | :doc:`user </resource_user>` | :doc:`windows_package </resource_windows_package>` | :doc:`windows_service </resource_windows_service>` | :doc:`yum_package </resource_yum>`


.. Hide the TOC from this file.  

.. toctree::
   :hidden:

   chef_overview
   config_rb_knife
   config_rb_knife_optional_settings
   dsl_recipe
   dsl_recipe_helper_windows_platform
   dsl_recipe_method_attribute
   dsl_recipe_method_cookbook_name
   dsl_recipe_method_data_bag
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
   knife
   knife_common_options
   knife_bootstrap
   knife_client
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
   knife_list
   knife_node
   knife_raw
   knife_recipe_list
   knife_role
   knife_search
   knife_serve
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
   release_notes
   resource
   resource_apt_package
   resource_bash
   resource_batch
   resource_bff_package
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
   resource_dsc_script
   resource_easy_install_package
   resource_env
   resource_erlang_call
   resource_execute
   resource_file
   resource_freebsd_package
   resource_gem_package
   resource_git
   resource_group
   resource_homebrew_package
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
   resource_reboot
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
   resource_windows_service
   resource_yum

..    api_chef_server
   api_omnitruck
   auth_authentication
   auth_authorization
   chef_client
   chef_cookbooks
   chef_overview
   chef_overview_attributes
   chef_overview_cookbooks
   chef_overview_nodes
   chef_overview_server
   chef_overview_workstation
   chef_private_keys
   chef_quick_overview
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
   essentials_node_object_deep_merge
   essentials_node_object_run_lists
   essentials_nodes
   essentials_nodes_chef_run
   essentials_nodes_why_run
   essentials_policy
   essentials_repository
   essentials_repository_create
   essentials_roles
   essentials_search
   handlers
   install_bootstrap
   install_omnibus
   install_windows
   install_workstation
   just_enough_ruby_for_chef
   lwrp
   lwrp_custom
   lwrp_custom_provider
   lwrp_custom_provider_ruby
   lwrp_custom_resource
   lwrp_custom_resource_library
   plugin_knife
   plugin_knife_authenticated_requests
   plugin_knife_custom



