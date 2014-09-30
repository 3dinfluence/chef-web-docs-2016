.. THIS PAGE DOCUMENTS chef-client version 10.latest

=====================================================
Lightweight Providers w/Platform Resources
=====================================================

.. include:: ../../includes_resources_common/includes_resources_common_provider.rst

.. include:: ../../includes_lwrp/includes_lwrp_custom_provider.rst

Syntax
=====================================================
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_syntax.rst

|dsl provider| Methods
=====================================================
.. include:: ../../includes_dsl_provider/includes_dsl_provider.rst

action
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_action.rst

.. note:: The ``converge_by`` method is not included in the previous syntax example because when |whyrun| mode is enabled in a lightweight provider that leverages platform resources, the ``converge_by`` blocks are already defined by the platform resources.

current_resource
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_current_resource.rst

load_current_resource
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_load_current_resource.rst

new_resource
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_new_resource.rst

updated_by_last_action
-----------------------------------------------------
.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_updated_by_last_action.rst

whyrun_supported?
-----------------------------------------------------
.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode.rst

.. include:: ../../includes_chef_client/includes_chef_client_whyrun_mode_assumptions.rst

.. include:: ../../includes_dsl_provider/includes_dsl_provider_method_whyrun_supported.rst

.. note:: When a lightweight provider contains only platform resources, the ``converge_by`` method is not required because it is already built into all of the platform `resources <http://docs.getchef.com/resource.html>`_.

Condition Statements
=====================================================
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_conditions.rst

Log Entries
=====================================================
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs.rst

rescue
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_logs_rescue.rst

Examples
=====================================================
The following examples show various lightweight providers that use platform resources.

aws_ebs_volume
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_aws_ebs_volume.rst

cron_d
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_cron_d.rst

rabbitmq_plugin
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_rabbitmq_plugin.rst

ssh_known_hosts_entry
-----------------------------------------------------
.. include:: ../../includes_lwrp/includes_lwrp_custom_provider_example_ssh_known_hosts_entry.rst
