.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``easy_install_binary``
     - **Ruby Type:** String

       The location of the |python easy_install| binary.
   * - ``module_name``
     - **Ruby Type:** String

       The name of the module.
   * - ``options``
     - **Ruby Type:** String

       |command options|
   * - ``package_name``
     - **Ruby Types:** String, Array

       |name package| Default value: the ``name`` of the resource block. |see syntax|
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter| |see providers|
   * - ``python_binary``
     - **Ruby Type:** String

       The location of the |python| binary.
   * - ``source``
     - **Ruby Type:** String

       Optional. |source resource package|
   * - ``timeout``
     - **Ruby Types:** String, Integer

       |timeout|
   * - ``version``
     - **Ruby Types:** String, Array

       |version package|
