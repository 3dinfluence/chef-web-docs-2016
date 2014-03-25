.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``automatic_attributes``
     - |attribute_type automatic| Default value: ``{}``.
   * - ``chef_environment``
     - The |chef server| environment in which this node should exist (or does exist).
   * - ``chef_server``
     - |chef_server_url|
   * - ``complete``
     - Use to specify if this resource defines a node completely. When ``true``, any attribute not specified by this resource will be reset to default attribute values.
   * - ``default_attributes``
     - |attribute_type default| Default value: ``{}``.
   * - ``name``
     - The name of the node.
   * - ``normal_attributes``
     - |attribute_type normal| Default value: ``{}``.
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
   * - ``run_list``
     - |run-list| Default value: ``[]``. For example: ``["recipe[default]","recipe[apache2]"]``

