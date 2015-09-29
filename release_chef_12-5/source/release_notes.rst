=====================================================
Release Notes: |chef client| 12.5
=====================================================

.. include:: ../../includes_chef/includes_chef.rst

What's New
=====================================================
The following items are new for |chef client| 12.5 and/or are changes from previous versions. The short version:

* **New way to build custom resources** The process for extending the collection of resources that are built into |chef| has been simplified. It is defined only in the ``/resources`` directory using a simplified syntax that easily leverages the built-in collection of resources. (All of the ways you used to build custom resources still work.)
* **"resource attributes" are now known as "resource properties"** In previous releases of |chef|, resource properties are referred to as attributes, but this is confusing for users because nodes also have attributes. Starting with |chef client| 12.5 release---and retroactively updated for all previous releases of the documentation---"resource attributes" are now referred to as "resource properties" and the word "attribute" now refers specifically to "node attributes".
* **ps_credential helper to embed usernames and passwords** Use the ``ps_credential`` helper on |windows| to create a ``PSCredential`` object---security credentials, such as a user name or password---that can be used in the |resource dsc_script| resource.
* **The -j / --json-attributes option may be used to specify environments** The |json| file used by the ``--json-attributes`` option for the |chef client| may now contain the name of the environment to which the node is associated.
* **verify property now uses path, not file** The ``verify`` property, used by file-based resources such as |resource remote_file| and |resource file|, runs user-defined correctness checks against the proposed new file before making the change. For versions of the |chef client| prior to 12.5, the name of the temporary file was stored as ``file``; starting with |chef client| 12.5, use ``path``. This change is documented as a warning across all versions in any topic in which the ``version`` attribute is documented.
* **depth property added to deploy resource** The ``depth`` property allows the depth of a |git| repository to be truncated to the specified number of versions.
* **The knife ssl check subcommand supports SNI*** Support for Server Name Indication (SNI) is added to the |subcommand knife ssl_check| subcommand.
* **Chef Policy group and name can now be part of the node object** |chef| policy is a beta feature of the |chef client| that will eventually replace roles, environments or manually specifying the run_list. Policy group and name can now be stored as part of the node object rather than in the |client rb| file. A recent version of the |chef server|, such as 12.2.0 or higher, is needed to fully utilize this feature.
* **New Handler DSL** A new DSL exists to make it easier to use events that occur during the |chef client| run from recipes. The ``on`` method is easily associated with events. The action the |chef client| takes as a result of that event (when it occurs) is up to you.


Custom Resources
-----------------------------------------------------
.. include:: ../../includes_custom_resources/includes_custom_resources.rst

.. note:: See https://docs.chef.io/custom_resources.html for more information about custom resources, including a scenario that shows how to build a ``website`` resource. Read this scenario as an HTML presentation at https://docs.chef.io/decks/custom_resources.html.

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_custom_resources/includes_custom_resources_syntax.rst

.. include:: ../../includes_custom_resources/includes_custom_resources_syntax_example.rst


Definition vs. Resource
-----------------------------------------------------
.. include:: ../../includes_definition/includes_definition_example.rst

As a Definition
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_definition/includes_definition_example_as_definition.rst

As a Resource
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_definition/includes_definition_example_as_resource.rst

Common Properties
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_definition/includes_definition_example_as_resource_with_common_properties.rst


|dsl handler|
-----------------------------------------------------
.. include:: ../../includes_dsl_handler/includes_dsl_handler.rst

on Method
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_handler/includes_dsl_handler_method_on.rst

Example: Send Email
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_handler/includes_dsl_handler_example_email.rst


ps_credential Helper
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_dsc_script_helper_ps_credential.rst

--json-attributes, Environments
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_client/includes_ctl_chef_client_environment.rst


|dsl custom_resource|
-----------------------------------------------------
.. include:: ../../includes_dsl_custom_resource/includes_dsl_custom_resource.rst

converge_if_changed
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_custom_resource/includes_dsl_custom_resource_method_converge_if_changed.rst

**Multiple Properties**

.. include:: ../../includes_dsl_custom_resource/includes_dsl_custom_resource_method_converge_if_changed_multiple.rst

load_current_value
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_dsl_custom_resource/includes_dsl_custom_resource_method_converge_if_changed.rst


|resource deploy| Property
-----------------------------------------------------
The following property is new for the |resource deploy| resource:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Property
     - Description
   * - ``depth``
     - **Ruby Type:** Integer

       |depth git_truncated|

Specify Policy Revision
-----------------------------------------------------
Use the following command to specify a policy revision:

.. code-block:: bash

   $ chef client -j JSON

where the |json| file is similar to:

.. code-block:: javascript

   {
     "policy_name": "appserver",
     "policy_group": "staging"
   }

Or use the following settings to specify a policy revision in the |client rb| file:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``policy_group``
     - |name policy_name|
   * - ``policy_name``
     - |name policy_group|



Changelog
=====================================================
https://github.com/chef/chef/blob/master/CHANGELOG.md
