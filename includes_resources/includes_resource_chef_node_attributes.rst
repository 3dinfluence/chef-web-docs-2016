.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following properties:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Property
     - Description
   * - ``automatic_attributes``
     - |attribute_type automatic| Default value: ``{}``.
   * - ``chef_environment``
     - The |chef server| environment in which this node should exist (or does exist).
   * - ``chef_server``
     - |chef_server_url|
   * - ``complete``
     - Use to specify if this resource defines a node completely. When ``true``, any property not specified by this resource will be reset to default property values.
   * - ``default_attributes``
     - |attribute_type default| Default value: ``{}``.
   * - ``ignore_failure``
     - **Ruby Types:** TrueClass, FalseClass

       |ignore_failure| Default value: ``false``.
   * - ``name``
     - The name of the node.
   * - ``normal_attributes``
     - |attribute_type normal| Default value: ``{}``.
   * - ``notifies``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |notifies|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_notifies.rst

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_timers.rst
   * - ``override_attributes``
     - |attribute_type override| Default value: ``{}``.
   * - ``raw_json``
     - The node as |json| data. For example:
       
       .. code-block:: javascript
       
          {
            "overrides": {},
            "name": "latte",
            "chef_type": "node",
            "json_class": "Chef::Node",
            "attributes": {
              "hardware_type": "laptop"
            },
            "run_list": [
              "recipe[apache2]"
            ],
            "defaults": {}
          }
   * - ``retries``
     - **Ruby Type:** Integer

       |retries| Default value: ``0``.
   * - ``retry_delay``
     - **Ruby Type:** Integer

       |retry_delay| Default value: ``2``.
   * - ``run_list``
     - |run-list| Default value: ``[]``. For example: ``["recipe[default]","recipe[apache2]"]``
   * - ``subscribes``
     - **Ruby Type:** Symbol, 'Chef::Resource[String]', Symbol

       |subscribes|

       .. include:: ../../includes_resources_common/includes_resources_common_notifications_syntax_subscribes.rst

       |subscribes timers|
