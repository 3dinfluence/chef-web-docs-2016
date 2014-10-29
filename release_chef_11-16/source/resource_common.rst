.. THIS PAGE DOCUMENTS chef-client version 11.16

=====================================================
Common Functionality 
=====================================================

All resources (and lightweight resources) share a set of common actions, attributes, conditional executions, notifications, and relative path options.

Actions
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_actions.rst

Examples
-----------------------------------------------------
The following examples show how to use common actions in a recipe.

**Use the :nothing action**

.. include:: ../../step_resource/step_resource_service_use_nothing_action.rst

Attributes
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_attributes.rst

Examples
-----------------------------------------------------
The following examples show how to use common attributes in a recipe.

**Use the ignore_failure common attribute**

.. include:: ../../step_resource/step_resource_package_use_ignore_failure_attribute.rst

**Use the provider common attribute**

.. include:: ../../step_resource/step_resource_package_use_provider_attribute.rst

**Use the supports common attribute**

.. include:: ../../step_resource/step_resource_service_use_supports_attribute.rst

**Use the supports and providers common attributes**

.. include:: ../../step_resource/step_resource_service_use_provider_and_supports_attributes.rst

Guards
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_guards.rst

.. note:: .. include:: ../../includes_resources_common/includes_resources_common_guards_execute_resource.rst

Attributes
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_guards_attributes.rst

Arguments
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_guards_arguments.rst

not_if Examples
-----------------------------------------------------

**Update if not already updated**

.. include:: ../../step_recipe/step_recipe_guard_notif_do_not_update_if_already_updated.rst

**Ensure a node can resolve a host**

.. include:: ../../step_recipe/step_recipe_guard_notif_ensure_node_can_resolve_host.rst

**Prevent installs on older versions**

.. include:: ../../step_recipe/step_recipe_guard_notif_prevent_install_on_older_versions.rst

**Set the administrator if not already set**

.. include:: ../../step_recipe/step_recipe_guard_notif_set_administrator_unless_already_set.rst

only_if Examples
-----------------------------------------------------

**Install packages only when necessary**

.. include:: ../../step_recipe/step_recipe_guard_onlyif_certain_packages.rst

**Remove a recipe if it belongs to a specific run-list**

.. include:: ../../step_recipe/step_recipe_guard_onlyif_remove_recipe.rst

**Re-register ASP.Net if it's already installed**

.. include:: ../../step_recipe/step_recipe_guard_onlyif_reregister_aspdotnet.rst

Guard Interpreters
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_guard_interpreter.rst

Attributes
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_11-16_guard_interpreter_attributes.rst

Inheritance
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_11-16_guard_interpreter_attributes_inherit.rst

Examples
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_guard_interpreter_example_default.rst

Lazy Attribute Evaluation
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_lazy_evaluation.rst

Notifications
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_notifications.rst

Notifications Timers
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst

Notifies Syntax
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following examples show how to use the ``notifies`` notification in a recipe.

**Delay notifications**

.. include:: ../../step_resource/step_resource_template_notifies_delay.rst

**Notify immediately**

.. include:: ../../step_resource/step_resource_template_notifies_run_immediately.rst

**Enable a service after a restart or reload**

.. include:: ../../step_resource/step_resource_service_notifies_enable_after_restart_or_reload.rst

**Notify multiple resources**

.. include:: ../../step_resource/step_resource_template_notifies_multiple_resources.rst

**Notify in a specific order**

.. include:: ../../step_resource/step_resource_execute_notifies_specific_order.rst

**Reload a service**

.. include:: ../../step_resource/step_resource_template_notifies_reload_service.rst

**Restart a service when a template is modified**

.. include:: ../../step_resource/step_resource_template_notifies_restart_service_when_template_modified.rst

**Send notifications to multiple resources**

.. include:: ../../step_resource/step_resource_template_notifies_send_notifications_to_multiple_resources.rst

**Execute a command using a template**

.. include:: ../../step_resource/step_resource_execute_command_from_template.rst

**Restart a service, and then notify a different service**

.. include:: ../../step_resource/step_resource_service_restart_and_notify.rst

**Notify when a remote source changes**

.. include:: ../../step_resource/step_resource_remote_file_transfer_remote_source_changes.rst

Subscribes Syntax
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following examples show how to use the ``subscribes`` notification in a recipe.

**Prevent restart and reconfigure if configuration is broken**

.. include:: ../../step_resource/step_resource_execute_subscribes_prevent_restart_and_reconfigure.rst

**Reload a service using a template**

.. include:: ../../step_resource/step_resource_service_subscribes_reload_using_template.rst

**Stash a file in a data bag**

.. include:: ../../step_resource/step_resource_ruby_block_stash_file_in_data_bag.rst

Relative Paths
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_relative_paths.rst

Examples
-----------------------------------------------------
.. include:: ../../step_resource/step_resource_template_use_relative_paths.rst


Run from Resource Collection 
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_compile.rst

Before other Resources
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_compile_begin.rst

After Collection is Built
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_compile_end.rst


Windows File Security
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_windows_security.rst

Access Control Lists (ACLs)
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_windows_security_acl.rst

Inheritance
-----------------------------------------------------
.. include:: ../../includes_resources_common/includes_resources_common_windows_security_inherits.rst

