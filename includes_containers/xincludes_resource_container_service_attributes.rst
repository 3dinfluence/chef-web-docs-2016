.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``command``
     - Use to specify the command to be run.
   * - ``binary``
     - The binary used by |runit| to manage services in a |linux| container. Default value: ``'/opt/chef/embedded/bin/sv'``.