.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``name``
     -  Always the same value as the ``name`` of the resource block (see Syntax section above).
   * - ``plugin``
     - Optional. The attribute to be reloaded. The |chef client| will identify the correct plugin.
   * - ``provider``
     - Optional. |provider resource_parameter| (See "Providers" section below for more information.)
