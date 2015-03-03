=====================================================
About the Recipe DSL
=====================================================

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe.rst

Because the |dsl recipe| is a |ruby| DSL, then anything that can be done using |ruby| can also be done in a recipe, including ``if`` and ``case`` statements, using the ``include?`` |ruby| method, including recipes in recipes, and checking for dependencies.

Use Ruby
=====================================================
Common |ruby| techniques can be used with the |dsl recipe| methods.

if Statements
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_style_basics_statement_if.rst

case Statements
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_style_basics_statement_case.rst

include? Method
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_style_basics_parameter_include.rst

Array Syntax Shortcut
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_style_basics_array_shortcut.rst

Include Recipes
=====================================================
.. include:: ../../includes_cookbooks/includes_cookbooks_recipe_include_in_recipe.rst

Reload Attributes
-----------------------------------------------------
.. include:: ../../includes_cookbooks/includes_cookbooks_attribute_file_reload_from_recipe.rst

Accessor Methods
-----------------------------------------------------
.. include:: ../../includes_cookbooks/includes_cookbooks_attribute_file_methods_accessor.rst

|dsl recipe| Methods
=====================================================
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method.rst

attribute?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_attribute.rst

control
-----------------------------------------------------
.. include:: ../../includes_analytics/includes_analytics_controls.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_syntax.rst

directory Matcher
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_matcher_directory.rst

file Matcher
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_matcher_file.rst

package Matcher
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_matcher_package.rst

port Matcher
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_matcher_port.rst

service Matcher
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_matcher_service.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++

**A package is installed**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_package_installed.rst

**A package version is installed**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_package_installed_version.rst

**A package is not installed**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_package_not_installed.rst

**A service is enabled**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_service_enabled.rst

**A configuration file contains specific settings**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_file_sshd_configuration.rst

**A file contains desired permissions and contents**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_matcher_file_permissions.rst

control_group
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_group.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_control_group_syntax.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++

**control_group block with multiple control blocks**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_group_many_controls.rst

**Duplicate control_group names**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_control_group_duplicate_names.rst

cookbook_name
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_cookbook_name.rst

data_bag
-----------------------------------------------------
.. include:: ../../includes_data_bag/includes_data_bag.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_data_bag.rst

**Examples**

The following example shows how the ``data_bag`` method can be used in a recipe.

**Get a data bag, and then iterate through each data bag item**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_data_bag.rst

data_bag_item
-----------------------------------------------------
.. include:: ../../includes_data_bag/includes_data_bag.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_data_bag_item.rst

**Examples**

The following examples show how the ``data_bag_item`` method can be used in a recipe.

**Get a data bag, and then iterate through each data bag item**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_data_bag.rst

**Use the contents of a data bag in a recipe**

.. include:: ../../step_dsl_recipe/step_dsl_recipe_data_bag_use_data_bag_methods.rst

platform?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_platform.rst

**Examples**

The following example shows how the ``platform?`` method can be used in a recipe.

**Use an if statement with the platform recipe DSL method**

.. include:: ../../step_resource/step_resource_ruby_block_if_statement_use_with_platform.rst

platform_family?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_platform_family.rst

Parameters
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_platform_family_parameters.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following examples show how the ``platform_family?`` method can be used in a recipe.

**Use a specific binary for a specific platform**

.. include:: ../../step_resource/step_resource_remote_file_use_platform_family.rst

reboot_pending?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_reboot_pending.rst

recipe_name
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_recipe_name.rst

resources
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_resources.rst

search
-----------------------------------------------------
.. include:: ../../includes_search/includes_search.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_search.rst

:filter_result
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_search_filter_result.rst

Query Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_query_syntax.rst

Keys
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_key.rst

**Nested Fields**

.. include:: ../../includes_search/includes_search_key_nested.rst

Patterns
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_pattern.rst

**Exact Match**

.. include:: ../../includes_search/includes_search_pattern_exact.rst

**Wildcard Match**

.. include:: ../../includes_search/includes_search_pattern_wildcard.rst

**Range Match**

.. include:: ../../includes_search/includes_search_pattern_range.rst

**Fuzzy Match**

.. include:: ../../includes_search/includes_search_pattern_fuzzy.rst

Operators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_boolean_operators.rst

Special Characters
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_special_characters.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following examples show how the ``search`` method can be used in a recipe.

**Use the search recipe DSL method to find users**

.. include:: ../../step_resource/step_resource_execute_use_search_dsl_method.rst

shell_out
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_shell_out.rst

shell_out!
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_shell_out_bang.rst

shell_out_with_systems_locale
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_shell_out_with_systems_locale.rst

tag, tagged?, untag
-----------------------------------------------------
.. include:: ../../includes_chef/includes_chef_tags.rst

.. include:: ../../includes_cookbooks/includes_cookbooks_recipe_tags.rst

value_for_platform
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_value_for_platform.rst

Operators
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_cookbooks/includes_cookbooks_version_constraints_operators.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_value_for_platform_examples.rst

value_for_platform_family
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_value_for_platform_family.rst


Windows Platform
=====================================================
The following methods and helpers may be used on the |windows| platform:

.. note:: The recommended order in which registry key-specific methods should be used within a recipe is: ``key_exists?``, ``value_exists?``, ``data_exists?``, ``get_values``, ``has_subkeys?``, and then ``get_subkeys``.

registry_data_exists?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_data_exists.rst

registry_get_subkeys
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_get_subkeys.rst

registry_get_values
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_get_values.rst

registry_has_subkeys?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_has_subkeys.rst

registry_key_exists?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_key_exists.rst

registry_value_exists?
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method_registry_value_exists.rst

Helpers
-----------------------------------------------------
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_helper_windows_platform.rst

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_helper_windows_platform_helpers.rst

.. include:: ../../step_dsl_recipe/step_dsl_recipe_helper_windows_platform.rst