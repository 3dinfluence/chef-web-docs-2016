.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``append``
     - **Ruby Types:** TrueClass, FalseClass

       |append_group| Default value: ``false``.
   * - ``excluded_members``
     - **Ruby Type:** Array

       |excluded_members|
   * - ``gid``
     - **Ruby Types:** String, Integer

       |id group|
   * - ``group_name``
     - **Ruby Type:** String

       |name group| |resource_block_default| |see syntax|
   * - ``ignore_failure``
     - **Ruby Types:** TrueClass, FalseClass

       |ignore_failure| Default value: ``false``.
   * - ``members``
     - **Ruby Type:** Array

       |members_group| When more than one group member is identified, the list of members should be an array: ``members ['user1', 'user2']``.
   * - ``non_unique``
     - **Ruby Types:** TrueClass, FalseClass

       |non_unique_members| Default value: ``false``.
   * - ``notifies``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |notifies|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter| |see providers|
   * - ``retries``
     - **Ruby Type:** Integer

       |retries| Default value: ``0``.
   * - ``retry_delay``
     - **Ruby Type:** Integer

       |retry_delay| Default value: ``2``.
   * - ``subscribes``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |subscribes|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

       |subscribes timers|
   * - ``system``
     - **Ruby Types:** TrueClass, FalseClass

       |system group|
