.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Property
     - Description
   * - ``after_restart``
     - **Ruby Types:** Proc, String

       |after_restart| Default value: ``deploy/after_restart.rb``.
   * - ``before_migrate``
     - **Ruby Types:** Proc, String

       |before_migrate| Default value: ``deploy/before_migrate.rb``.
   * - ``before_restart``
     - **Ruby Types:** Proc, String

       |before_restart| Default value: ``deploy/before_restart.rb``.
   * - ``before_symlink``
     - **Ruby Types:** Proc, String

       |before_symlink| Default value: ``deploy/before_symlink.rb``.
   * - ``branch``
     - **Ruby Type:** String

       The alias for the revision.
   * - ``create_dirs_before_symlink``
     - **Ruby Type:** Array

       |create_dirs_before_symlink| Default value: ``%w{tmp public config}`` (or the same as ``["tmp", "public", "config"]``).
   * - ``deploy_to``
     - **Ruby Type:** String

       |deploy_to| |resource_block_default| |see syntax|
   * - ``environment``
     - **Ruby Type:** Hash

       |environment variables|
   * - ``group``
     - **Ruby Type:** String

       |group deploy|
   * - ``ignore_failure``
     - **Ruby Types:** TrueClass, FalseClass

       |ignore_failure| Default value: ``false``.
   * - ``keep_releases``
     - **Ruby Type:** Integer

       |keep_releases| Default value: ``5``.
   * - ``migrate``
     - **Ruby Types:** TrueClass, FalseClass

       |migrate command_run| Default value: ``false``.
   * - ``migration_command``
     - **Ruby Type:** String

       |migration command_string|
   * - ``notifies``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |notifies|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter| |see providers|
   * - ``purge_before_symlink``
     - **Ruby Type:** Array

       |purge_before_symlink| Default value: ``%w{log tmp/pids public/system}`` (or the same as ``["log", "tmp/pids", "public/system"]``.
   * - ``repo``
     - **Ruby Type:** String

       |repository git_or_svn|
   * - ``repository``
     - **Ruby Type:** String

       |uri repository|
   * - ``repository_cache``
     - **Ruby Type:** String

       |repository_cache| Default value: ``cached-copy``.
   * - ``restart_command``
     - **Ruby Types:** String, Proc

       |restart shell_command|
   * - ``retries``
     - **Ruby Type:** Integer

       |retries| Default value: ``0``.
   * - ``retry_delay``
     - **Ruby Type:** Integer

       |retry_delay| Default value: ``2``.
   * - ``revision``
     - **Ruby Type:** String

       |revision| Default value: ``HEAD``.
   * - ``rollback_on_error``
     - **Ruby Types:** TrueClass, FalseClass

       |rollback_on_error| Default value: ``false``.
   * - ``scm_provider``
     - **Ruby Type:** Chef Class

       |name scm_provider| Default value: ``Chef::Provider::Git``. Optional values: ``Chef::Provider::Subversion``.
   * - ``subscribes``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |subscribes|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

       |subscribes timers|
   * - ``symlinks``
     - **Ruby Type:** Hash

       |symlinks| Default value: ``{"system" => "public/system", "pids" => "tmp/pids", "log" => "log"}``.
   * - ``symlink_before_migrate``
     - **Ruby Type:** Hash

       |symlink_before_migrate| Default value: ``{"config/database.yml" => "config/database.yml"}``.
   * - ``user``
     - **Ruby Type:** String

       |user checked_out_code|

The following properties are for use with |git| only:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Property
     - Description
   * - ``enable_submodules``
     - **Ruby Types:** TrueClass, FalseClass

       |enable_submodules| Default value: ``false``.
   * - ``git_ssh_wrapper``
     - **Ruby Type:** String

       |git_ssh_wrapper|
   * - ``remote``
     - **Ruby Type:** String

       |remote resource| Default value: ``origin``.
   * - ``shallow_clone``
     - **Ruby Types:** TrueClass, FalseClass

       |shallow_clone| Default value: ``false``.
   * - ``ssh_wrapper``
     - **Ruby Type:** String

       |ssh_wrapper resource|

The following properties are for use with |svn| only:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Property
     - Description
   * - ``svn_arguments``
     - **Ruby Type:** String

       |svn_arguments resource|
   * - ``svn_password``
     - **Ruby Type:** String

       |svn_password resource|
   * - ``svn_username``
     - **Ruby Type:** String

       |svn_username resource|
