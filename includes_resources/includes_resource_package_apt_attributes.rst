.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:
   
``default_release``
   **Ruby Type:** String

   |default_release apt| For example: ``stable``.
   
``ignore_failure``
   **Ruby Types:** TrueClass, FalseClass

   |ignore_failure| Default value: ``false``.
   
``notifies``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   |notifies|

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   
``options``
   **Ruby Type:** String

   |command options| For example, common |aptget| directives, such as ``--no-install-recommends``. See the `apt-get man page <http://manpages.debian.net/cgi-bin/man.cgi?query=apt-get>`_ for the full list.
   
``package_name``
   **Ruby Types:** String, Array

   |name package| |resource_block_default| |see syntax|
   
``provider``
   **Ruby Type:** Chef Class

   Optional. |provider resource_parameter| |see providers|
   
``retries``
   **Ruby Type:** Integer

   |retries| Default value: ``0``.
   
``retry_delay``
   **Ruby Type:** Integer

   |retry_delay| Default value: ``2``.
   
``source``
   **Ruby Type:** String

   Optional. |source resource apt_package|
   
``subscribes``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   |subscribes|

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

   |subscribes timers|
   
``timeout``
   **Ruby Types:** String, Integer

   |timeout|
   
``version``
   **Ruby Types:** String, Array

   |version package|
