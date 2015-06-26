.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``comment``
     - **Ruby Type:** String

       |comment user|
   * - ``force``
     - **Ruby Types:** TrueClass, FalseClass

       |force_remove_user|

       .. warning:: Using this attribute may leave the system in an inconsistent state. For example, a user account will be removed even if the user is logged in. A user's home directory will be removed, even if that directory is shared by multiple users.
   * - ``gid``
     - **Ruby Types:** String, Integer

       |id group|
   * - ``home``
     - **Ruby Types:** String

       |home_directory|
   * - ``iterations``
     - **Ruby Types:** Integer

       |mac os x| platform only, 10.8 (or higher). |iterations|
   * - ``manage_home``
     - **Ruby Types:** TrueClass, FalseClass

       |user homedir|

       |user homedir_create|

       |user homedir_modify|
   * - ``non_unique``
     - **Ruby Types:** TrueClass, FalseClass

       |non_unique_user|
   * - ``password``
     - **Ruby Types:** String

       |password shadow_hash|
   * - ``provider``
     - **Ruby Types:** Chef Class

       Optional. |provider resource_parameter| |see providers|
   * - ``salt``
     - **Ruby Types:** String

       |mac os x| platform only, 10.7 or higher. |salt| |mac os x| version 10.7 uses SALTED-SHA512 and version 10.8 (and higher) uses SALTED-SHA512-PBKDF2 to calculate password shadow hashes. 
   * - ``shell``
     - **Ruby Types:** String

       |shell|
   * - ``supports``
     - **Ruby Types:** Hash

       |supports user| Default value: ``:manage_home => false, :non_unique => false``.
   * - ``system``
     - **Ruby Types:** TrueClass, FalseClass

       |system user|
   * - ``uid``
     - **Ruby Types:** String, Integer

       |user uid|
   * - ``username``
     - **Ruby Type:** String

       |name user| Default value: the ``name`` of the resource block. |see syntax|