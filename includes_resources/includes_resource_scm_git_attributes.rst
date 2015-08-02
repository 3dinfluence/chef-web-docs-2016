.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Property
     - Description
   * - ``additional_remotes``
     - **Ruby Type:** Hash

       |additional_remotes|
   * - ``checkout_branch``
     - **Ruby Type:** String

       |checkout_branch git| See ``revision``. Default value: ``deploy``.
   * - ``depth``
     - **Ruby Type:** Integer

       |depth git_shallow_clone| The default behavior will do a full clone.
   * - ``destination``
     - **Ruby Type:** String

       |destination resource scm| |resource_block_default| |see syntax|
   * - ``enable_checkout``
     - **Ruby Types:** TrueClass, FalseClass

       |enable_git_checkout| Set to ``false`` when using the ``checkout_branch`` attribute to prevent the |resource scm_git| resource from attempting to check out master from master. Default value: ``true``.
   * - ``enable_submodules``
     - **Ruby Types:** TrueClass, FalseClass

       |enable_submodules| Default value: ``false``.
   * - ``environment``
     - **Ruby Type:** Hash

       |environment variables|

       .. note:: .. include:: ../../includes_notes/includes_notes_scm_resource_git_env_variables.rst
   * - ``group``
     - **Ruby Types:** String, Integer

       |group deploy|
   * - ``ignore_failure``
     - **Ruby Types:** TrueClass, FalseClass

       |ignore_failure| Default value: ``false``.
   * - ``notifies``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |notifies|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter|
   * - ``reference``
     - **Ruby Type:** String

       |reference resource scm|
   * - ``remote``
     - **Ruby Type:** String

       |remote resource|
   * - ``repository``
     - **Ruby Type:** String

       |uri repository_git|
   * - ``retries``
     - **Ruby Type:** Integer

       |retries| Default value: ``0``.
   * - ``retry_delay``
     - **Ruby Type:** Integer

       |retry_delay| Default value: ``2``.
   * - ``revision``
     - **Ruby Type:** String

       |revision| See ``checkout_branch``. Default value: ``HEAD``.

       .. include:: ../../includes_resources/includes_resource_scm_git_attributes_revision.rst
   * - ``ssh_wrapper``
     - **Ruby Type:** String

       |ssh_wrapper resource|
   * - ``subscribes``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |subscribes|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

       |subscribes timers|
   * - ``timeout``
     - **Ruby Type:** Integer

       |timeout scm| |timeout scm_value_git|
   * - ``user``
     - **Ruby Types:** String, Integer

       |user checked_out_code| Default value: the home directory of this user, as indicated by the ``HOME`` environment variable.
