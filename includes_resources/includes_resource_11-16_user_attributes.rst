.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``comment``
     - |comment user|
   * - ``gid``
     - |id group|
   * - ``home``
     - |home_directory|
   * - ``password``
     - |password shadow_hash|
   * - ``provider``
     - Optional. |provider resource_parameter| (See "Providers" section below for more information.)
   * - ``shell``
     - |shell|
   * - ``supports``
     - |supports user| Default value: ``:manage_home => false, :non_unique => false``.
   * - ``system``
     - |system user|
   * - ``uid``
     - |user uid|
   * - ``username``
     - |name user| Default value: the ``name`` of the resource block. (See "Syntax" section above for more information.)