.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``cookbook``
     - |cookbook file_location| The default value is the current cookbook.
   * - ``files_backup``
     - |files_backup| Default value: ``5``.
   * - ``files_group``
     - |files_group| |windows group_identifier|
   * - ``files_mode``
     - The octal mode for a file.
       
       |unix|- and |linux|-based systems: |mode *nix|
       
       |windows|: |mode windows security|
   * - ``files_owner``
     - |files_owner| |owner windows security|
   * - ``group``
     - Use to configure permissions for directories. |windows group_identifier|
   * - ``inherits``
     - |windows| only. |inherits windows security| Default value: ``true``.
   * - ``mode``
     - |mode resource_directory|
       
       The behavior is different depending on the platform.
       
       |unix|- and |linux|-based systems: |mode *nix|
       
       |windows|: |mode windows security|
   * - ``overwrite``
     - |use file_overwrite| Default value: ``true``.
   * - ``owner``
     - Use to configure permissions for directories. |owner windows security|
   * - ``path``
     - |path directory| |path_fully_qualified| Default value: the ``name`` of the resource block. |see syntax|
   * - ``provider``
     - Optional. |provider resource_parameter| |see providers|
   * - ``purge``
     - |purge target_directory| Default value: ``false``.
   * - ``recursive``
     - |recursive remote_directory| Default value: ``true``; the |chef client| must be able to create the directory structure, including parent directories (if missing), as defined in ``COOKBOOK_NAME/files/default/REMOTE_DIRECTORY``.
   * - ``rights``
     - |windows| only. |rights windows security|
   * - ``source``
     - |source remote_directory|
