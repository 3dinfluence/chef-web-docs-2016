=====================================================
About the Recipe DSL
=====================================================

.. warning:: |note doc_version_11-4|

.. include:: ../../includes_dsl_recipe/includes_dsl_recipe.rst

Because the |dsl recipe| is a |ruby| DSL, then anything that can be done using |ruby| can also be done in a recipe, including ``if`` and ``case`` statements, using the ``include?`` |ruby| method, including recipes in recipes, and checking for dependencies.

Use Ruby
=====================================================
Common |ruby| techniques can be used with the |dsl recipe| methods.

if Statements
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_statement_if.rst

case Statements
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_statement_case.rst

include? Method
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_method_include.rst

Array Syntax Shortcut
-----------------------------------------------------
.. include:: ../../includes_ruby/includes_ruby_shortcut_array.rst

.. include:: ../../step_lwrp/step_lwrp_windows_feature_disable.rst

Include Recipes
=====================================================
.. include:: ../../includes_cookbooks/includes_cookbooks_recipe_include_in_recipe.rst

Reload Attributes
-----------------------------------------------------
.. include:: ../../includes_cookbooks/includes_cookbooks_attribute_file_reload_from_recipe.rst

Accessor Methods
-----------------------------------------------------
.. include:: ../../includes_cookbooks/includes_cookbooks_attribute_file_methods_accessor.rst

Recipe DSL Methods
=====================================================
.. include:: ../../includes_dsl_recipe/includes_dsl_recipe_method.rst

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Methods
     - Description
   * - :doc:`attribute? </dsl_recipe_method_attribute>`
     - Use in a recipe to include an attribute.
   * - :doc:`data_bag, data_bag_item </dsl_recipe_method_data_bag>`
     - Use in a recipe to include a data bag or data bag item.
   * - :doc:`cookbook_name </dsl_recipe_method_cookbook_name>`
     - Use in a recipe to get the name of the cookbook in which a recipe is located.
   * - :doc:`platform? </dsl_recipe_method_platform>`
     - Use in a recipe to check for the platform.
   * - :doc:`platform_family? </dsl_recipe_method_platform_family>`
     - Use in a recipe to check for the platform family.
   * - :doc:`recipe_name </dsl_recipe_method_recipe_name>`
     - Use in a recipe to get the name of a recipe.
   * - :doc:`resources </dsl_recipe_method_resources>`
     - Use in a recipe to include a resource.
   * - :doc:`search </dsl_recipe_method_search>`
     - Use in a recipe to include search results.
   * - :doc:`tag, tagged?, untag </dsl_recipe_method_tag>`
     - Use in a recipe to use and apply tags.
   * - :doc:`value_for_platform </dsl_recipe_method_value_for_platform>`
     - Use in a recipe to check for a value for a platform.
   * - :doc:`value_for_platform_family </dsl_recipe_method_value_for_platform_family>`
     - Use in a recipe to check for a value for a platform family.

The following recipe DSL methods can be used to interact with |windows| registry keys.

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Methods
     - Description
   * -  :doc:`registry_data_exists? </dsl_recipe_method_registry_data_exists>`
     - Find out if a registry key contains data.
   * - :doc:`registry_get_subkeys </dsl_recipe_method_registry_get_subkeys>`
     - Get a list of sub-keys for a registry setting.
   * - :doc:`registry_get_values </dsl_recipe_method_registry_get_values>`
     - Get values (name, type, and data) for a given registry key.
   * - :doc:`registry_has_subkeys? </dsl_recipe_method_registry_has_subkeys>`
     - Find out if a registry key has one (or more) sub-keys.
   * - :doc:`registry_key_exists? </dsl_recipe_method_registry_key_exists>`
     - Find out if a registry key exists.
   * - :doc:`registry_value_exists? </dsl_recipe_method_registry_value_exists>`
     - Find out if a registry key has values set (name, type, and data).

.. note:: The recommended order in which registry key-specific methods should be used within a recipe is: ``key_exists?``, ``value_exists?``, ``data_exists?``, ``get_values``, ``has_subkeys?``, and then ``get_subkeys``.

.. toctree::
   :hidden:

   dsl_recipe_method_attribute
   dsl_recipe_method_cookbook_name
   dsl_recipe_method_data_bag
   dsl_recipe_method_platform
   dsl_recipe_method_platform_family
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



