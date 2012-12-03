.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The |resource deploy| resource expects an application to be structured like a |ruby on rails| application, but the layout can be modified to meet custom requirements as needed. Use the following attributes within a recipe to modify the layout of a recipe that is using the |resource deploy| resource:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Layout Modifiers
     - Description
   * - ``create_dirs_before_symlink``
     - |create_dirs_before_symlink|
   * - ``purge_before_symlink``
     - |purge_before_symlink| 
   * - ``symlink_before_migrate``
     - |symlink_before_migrate|
   * - ``symlinks``
     - |symlinks| 

