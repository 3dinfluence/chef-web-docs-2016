.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:
   
``ignore_failure``
   **Ruby Types:** TrueClass, FalseClass

   |ignore_failure| Default value: ``false``.
   
``init_command``
   **Ruby Type:** String

   |command service_init| This is typically ``/etc/init.d/SERVICE_NAME``. The ``init_command`` property can be used to prevent the need to specify  overrides for the ``start_command``, ``stop_command``, and ``restart_command`` attributes. Default value: ``nil``.
   
``notifies``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   |notifies|

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   
``pattern``
   **Ruby Type:** String

   |pattern process_table| Default value: ``service_name``.
   
``provider``
   **Ruby Type:** Chef Class

   Optional. |provider resource_parameter|
   
``reload_command``
   **Ruby Type:** String

   |command service_reload|
   
``restart_command``
   **Ruby Type:** String

   |command service_restart|
   
``retries``
   **Ruby Type:** Integer

   |retries| Default value: ``0``.
   
``retry_delay``
   **Ruby Type:** Integer

   |retry_delay| Default value: ``2``.
   
``run_as_password``
   **Ruby Type:** String

   |password windows_service_run_as|
   
``run_as_user``
   **Ruby Type:** String

   |user windows_service_run_as|
   
``service_name``
   **Ruby Type:** String

   |name service| |resource_block_default| |see syntax|
   
``start_command``
   **Ruby Type:** String

   |command service_start|
   
``startup_type``
   **Ruby Type:** Symbol

   Use to specify the startup type for a |windows| service. Possible values: ``:automatic``, ``:disabled``, or ``:manual``. Default value: ``:automatic``.
   
``status_command``
   **Ruby Type:** String

   |command service_status|
   
``stop_command``
   **Ruby Type:** String

   |command service_stop|
   
``subscribes``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   |subscribes|

   .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

   |subscribes timers|
   
``supports``
   **Ruby Type:** Hash

   |supports service| Default value: ``{ :restart => false, :reload => false, :status => false }`` for all platforms (except for the |redhat| platform family, which defaults to ``{ :restart => false, :reload => false, :status => true }``.)
   
``timeout``
   **Ruby Type:** Integer

   |timeout|
