.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``backup``
     - |backups_kept| Default value: ``5``.
   * - ``checksum``
     - Optional. |checksum remote_file|
   * - ``group``
     - |windows group_identifier|
   * - ``inherits``
     - |windows| only. |inherits windows security| Default value: ``true``.
   * - ``mode``
     - |mode resource_file_11-4|
       
       The behavior is different depending on the platform.
       
       |unix|- and |linux|-based systems: |mode *nix|
       
       |windows|: |mode windows security|
   * - ``owner``
     - |owner windows security|
   * - ``path``
     - |path file| |path_fully_qualified| Default value: ``name``.
   * - ``provider``
     - Optional. |provider resource_parameter| |see providers|
   * - ``rights``
     - |windows| only. |rights windows security|
   * - ``source``
     - Required. |source file_location chef_11-4|
