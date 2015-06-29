.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Attribute
     - Description
   * - ``allow_downgrade``
     - **Ruby Types:** TrueClass, FalseClass

       |resource yum_package| resource only. |allow_downgrade| Default value: ``false``.
   * - ``arch``
     - **Ruby Types:** String, Array

       |resource yum_package| resource only. |architecture package|
   * - ``default_release``
     - **Ruby Type:** String

       |resource package_apt| resource only. |default_release apt| For example: ``stable``.
   * - ``flush_cache``
     - **Ruby Type:** Array

       |resource yum_package| resource only. |flush_cache| Default value: ``{ :before => false, :after => false }``.

       .. note:: |flush_cache yum_cache|
   * - ``gem_binary``
     - **Ruby Type:** String

       |gem_binary resource package|
   * - ``options``
     - **Ruby Type:** String

       |command options|
   * - ``package_name``
     - **Ruby Types:** String, Array

       |name package| Default value: the ``name`` of the resource block. |see syntax|
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter| |see providers|
   * - ``response_file``
     - **Ruby Type:** String

       |resource package_apt| and |resource package_dpkg| resources only. |response_file|
   * - ``response_file_variables``
     - **Ruby Type:** Hash

       |resource package_apt| and |resource package_dpkg| resources only. |response_file variables|
   * - ``source``
     - **Ruby Type:** String

       Optional. |source resource package|
   * - ``timeout``
     - **Ruby Types:** String, Integer

       |timeout|
   * - ``version``
     - **Ruby Types:** String, Array

       |version package|
