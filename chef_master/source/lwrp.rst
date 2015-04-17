=====================================================
About LWRPs
=====================================================

.. include:: ../../includes_lwrp/includes_lwrp.rst

Custom Resources
=====================================================

.. include:: ../../includes_resources_common/includes_resources_common.rst

.. include:: ../../includes_lwrp/includes_lwrp_custom_resource.rst

Syntax
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_resource_syntax.rst

|dsl resource| Methods
-----------------------------------------------------
.. include:: ../../includes_dsl_resource/includes_dsl_resource.rst

actions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_action.rst

attribute
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_attribute.rst

attr_accessor
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_attr_accessor.rst

default_action
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_default_action.rst

provides
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_provides.rst

state_attrs
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_state_attrs.rst

Validation Parameters
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_attribute_validation_parameter.rst

Guards
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_resources_common/includes_resources_common_guards.rst

Guard Attributes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_resources_common/includes_resources_common_guards_attributes.rst

Guard Arguments
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_resources_common/includes_resources_common_guards_arguments.rst

Notifications
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_resources_common/includes_resources_common_notifications.rst

Syntax
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

.. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

Timers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst

Examples
-----------------------------------------------------
The following examples show various lightweight providers that use platform resources or how to use certain parts of the |dsl resource|.

:callbacks
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_resource_example_callbacks.rst



Custom Providers w/Platform Resources
=====================================================

.. include:: ../../includes_resources_common/includes_resources_common_provider.rst

.. include:: ../../includes_lwrp/includes_lwrp_custom_provider.rst

Syntax
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_syntax.rst

|dsl provider| Methods
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider.rst

action
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_action.rst

.. note:: The ``converge_by`` method is not included in the previous syntax example because when |whyrun| mode is enabled in a lightweight provider that leverages platform resources, the ``converge_by`` blocks are already defined by the platform resources.

current_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_current_resource.rst

load_current_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_load_current_resource.rst

new_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_new_resource.rst

provides
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_resource/includes_dsl_resource_method_provides.rst

updated_by_last_action
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_updated_by_last_action.rst

.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_updated_by_last_action_example.rst

use_inline_resources
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_use_inline_resources_about.rst

.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_use_inline_resources.rst

Background
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_use_inline_resources_background.rst

Disable
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_use_inline_resources_default_behavior.rst

whyrun_supported?
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode.rst

.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode_assumptions.rst

.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_whyrun_supported.rst

.. note:: When a lightweight provider contains only platform resources, the ``converge_by`` method is not required because it is already built into all of the platform `resources <http://docs.chef.io/resource.html>`_.

Condition Statements
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_conditions.rst

Log Entries
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs.rst

rescue
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs_rescue.rst

Examples
-----------------------------------------------------
The following examples show various lightweight providers that use platform resources.

aws_ebs_volume
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_aws_ebs_volume.rst

cron_d
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_cron_d.rst

rabbitmq_plugin
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_rabbitmq_plugin.rst

ssh_known_hosts_entry
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_ssh_known_hosts_entry.rst



Custom Providers w/Ruby
=====================================================

.. include:: ../../includes_resources_common/includes_resources_common_provider.rst

.. include:: ../../includes_lwrp/includes_lwrp_custom_provider.rst

Syntax
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_syntax_ruby.rst

|dsl provider| Methods
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider.rst

action
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_action_with_converge_by.rst

converge_by
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_converge_by.rst

current_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_current_resource.rst

load_current_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_load_current_resource.rst

new_resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_new_resource.rst

require
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_require.rst

updated_by_last_action
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_updated_by_last_action_ruby.rst

whyrun_supported?
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode.rst

.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode_assumptions.rst

.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_whyrun_supported.rst

Condition Statements
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_conditions.rst

Log Entries
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs.rst

rescue
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs_rescue.rst

Libraries
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_library.rst

Examples
-----------------------------------------------------
The following examples show various lightweight providers that rely on custom |ruby| code.

rbenv_global
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_rbenv_global.rst
