.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Property
     - Description
   * - ``atomic_update``
     - **Ruby Types:** TrueClass, FalseClass

       |atomic_update| Default value: ``true``.
   * - ``backup``
     - **Ruby Types:** FalseClass, Integer

       |backups_kept| Default value: ``5``.
   * - ``cookbook``
     - **Ruby Type:** String

       |cookbook file_location| The default value is the current cookbook.
   * - ``force_unlink``
     - **Ruby Types:** TrueClass, FalseClass

       |force_unlink| Default value: ``false``.
   * - ``group``
     - **Ruby Types:** Integer, String

       |windows group_identifier|
   * - ``helper``
     - **Ruby Type:** Method

       |helper| Default value: ``{}``.
   * - ``helpers``
     - **Ruby Type:** Module

       |helpers| Default value: ``[]``.
   * - ``ignore_failure``
     - **Ruby Types:** TrueClass, FalseClass

       |ignore_failure| Default value: ``false``.
   * - ``inherits``
     - **Ruby Types:** TrueClass, FalseClass

       |windows| only. |inherits windows security| Default value: ``true``.
   * - ``local``
     - **Ruby Types:** TrueClass, FalseClass

       |local_template| Default value: ``false``.
   * - ``manage_symlink_source``
     - **Ruby Types:** TrueClass, FalseClass, NilClass

       |manage_symlink_source| Possible values: ``nil``, ``true``, or ``false``. When this value is set to ``nil``, the |chef client| will manage a symlink's source file and emit a warning. When this value is set to ``true``, the |chef client| will manage a symlink's source file and not emit a warning. Default value: ``nil``. The default value will be changed to ``false`` in a future version.
   * - ``mode``
     - **Ruby Types:** Integer, String

       |mode resource| |mode resource_file|
       
       The behavior is different depending on the platform.
       
       |unix|- and |linux|-based systems: |mode *nix|
       
       |windows|: |mode windows security|
   * - ``notifies``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |notifies|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   * - ``owner``
     - **Ruby Types:** Integer, String

       |owner windows security|
   * - ``path``
     - **Ruby Type:** String

       |path full_path_to_file|

       |windows|: A path that begins with a forward slash (``/``) will point to the root of the current working directory of the |chef client| process. This path can vary from system to system. Therefore, using a path that begins with a forward slash (``/``) is not recommended.
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter|
   * - ``retries``
     - **Ruby Type:** Integer

       |retries| Default value: ``0``.
   * - ``retry_delay``
     - **Ruby Type:** Integer

       |retry_delay| Default value: ``2``.
   * - ``rights``
     - **Ruby Types:** Integer, String

       |windows| only. |rights windows security|
   * - ``sensitive``
     - **Ruby Types:** TrueClass, FalseClass

       |sensitive| Default value: ``false``.
   * - ``source``
     - **Ruby Types:** String, Array

       |source template| |source template_cookbook| |source template_local| This property may also be used to distribute specific files to specific platforms. |see file_specificity| |resource_block_default| |see syntax|
   * - ``subscribes``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |subscribes|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

       |subscribes timers|
   * - ``variables``
     - **Ruby Type:** Hash

       |variables passed_to_template|
       
       .. include:: ../../includes_template/includes_template_partials_variables_attribute.rst
   * - ``verify``
     - **Ruby Types:** String, Block

       |verify_file|

       .. include:: ../../includes_resources_common/includes_resources_common_attribute_verify.rst
