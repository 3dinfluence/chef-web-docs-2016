.. THIS PAGE DOCUMENTS chef-client version 10.latest

=====================================================
|ohai|
=====================================================

.. include:: ../../includes_ohai/includes_ohai.rst

.. include:: ../../includes_ohai/includes_ohai_platforms.rst

View the :doc:`release notes </release_notes>` for |ohai 6|.

.. warning:: `Ohai 7 <http://docs.getchef.com/release/ohai-7/>`_ is planned to be fully integrated into the |chef client| starting with the 11.12.0 release (~April 2014).

Automatic Attributes
=====================================================
.. include:: ../../includes_ohai/includes_ohai_automatic_attribute.rst

**Get a list of automatic attributes for a node**

.. include:: ../../includes_ohai/includes_ohai_attribute_list.rst

.. note:: |note see_attributes_overview|

Attribute Persistence
-----------------------------------------------------
.. include:: ../../includes_node/includes_node_attribute_persistence.rst

Attribute Precedence
-----------------------------------------------------
.. include:: ../../includes_node/includes_node_attribute_precedence.rst

Custom |ohai 6| Plugins
=====================================================

.. warning:: Custom plugins change significantly in |ohai 7| (see the `release notes <http://docs.getchef.com/release/ohai-7/release_notes.html>`_). While |company_name| has worked to ensure backwards compatibility for all |ohai| plugins, all plugins that were built for |ohai 6| should be updated, tested, and then verified for |ohai 7|.

.. include:: ../../includes_ohai/includes_ohai_custom_plugin.rst

Syntax
-----------------------------------------------------
.. include:: ../../includes_ohai/includes_ohai_6_custom_plugin_syntax.rst

Use a Mash
-----------------------------------------------------
.. include:: ../../includes_dsl_ohai/includes_dsl_ohai_method_collect_data_mash.rst

|ohai 6| vs. |ohai 7| Plugins
-----------------------------------------------------
.. include:: ../../includes_ohai/includes_ohai_migrate_plugins_6_to_7.rst

ohai Resource
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_generic.rst

.. include:: ../../includes_resources/includes_resource_ohai.rst

Syntax
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_ohai_syntax.rst

Actions
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_ohai_actions.rst

Attributes
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_11-10_ohai_attributes.rst

Providers
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_ohai_providers.rst

Examples
-----------------------------------------------------
|generic resource statement|

**Reload Ohai**

.. include:: ../../step_resource/step_resource_ohai_reload.rst

**Reload Ohai after a new user is created**

.. include:: ../../step_resource/step_resource_11-10_ohai_reload_after_create_user.rst

ohai Cookbook
=====================================================
.. include:: ../../step_ohai/step_ohai_download_cookbook.rst

Default Location
-----------------------------------------------------
.. include:: ../../step_ohai/step_ohai_plugin_change_path.rst

Upload Custom Plugins
-----------------------------------------------------
.. include:: ../../step_ohai/step_ohai_plugin_upload.rst

Add |ohai| to a Run-list
-----------------------------------------------------
.. include:: ../../step_ohai/step_ohai_add_to_run_list.rst



ohai Command Line Tool
=====================================================
.. include:: ../../includes_ctl_ohai/includes_ctl_ohai.rst

Options
-----------------------------------------------------
.. include:: ../../includes_ctl_ohai/includes_ctl_ohai_6_options.rst

Examples
-----------------------------------------------------
The following examples show how to use the |ohai| command-line tool:

**Run a plugin independently of a chef-client run**

.. include:: ../../step_ohai/step_ohai_6_run_plugin.rst


|ohai| Settings in |client rb|
=====================================================
.. include:: ../../includes_config/includes_config_rb_ohai.rst

.. include:: ../../includes_config/includes_config_rb_6_ohai_settings.rst
