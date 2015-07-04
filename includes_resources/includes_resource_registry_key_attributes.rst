.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``architecture``
     - **Ruby Type:** Symbol

       |architecture registry_key| Default value: ``:machine``.

       |architecture registry_key machine|

       .. note:: |note registry_key architecture|
   * - ``key``
     - **Ruby Type:** String

       |key_name resource registry_key| Default value: the ``name`` of the resource block. |see syntax|
       |key_name resource registry_key hives|
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter|
   * - ``recursive``
     - **Ruby Types:** TrueClass, FalseClass

       |recursive registry_key|

       .. note:: |note registry_key resource recursive|
   * - ``values``
     - **Ruby Types:** Hash, Array

       |values resource registry_key|
       
       |values resource registry_key types|

       .. warning:: |values resource registry_key multi_string|

