.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``destination``
     - **Ruby Type:** String

       |destination resource scm| Default value: the ``name`` of the resource block. |see syntax|
   * - ``group``
     - **Ruby Types:** String, Integer

       |group deploy|
   * - ``provider``
     - **Ruby Type:** Chef Class

       Optional. |provider resource_parameter|
   * - ``repository``
     - **Ruby Type:** String

       |uri repository_svn|
   * - ``revision``
     - **Ruby Type:** String

       |revision| Default value: ``HEAD``.
   * - ``svn_arguments``
     - **Ruby Type:** String

       |svn_arguments resource|
   * - ``svn_info_args``
     - **Ruby Type:** String

       |svn_info_args resource|
   * - ``svn_password``
     - **Ruby Type:** String

       |svn_password resource|
   * - ``svn_username``
     - **Ruby Type:** String

       |svn_username resource|
   * - ``user``
     - **Ruby Types:** String, Integer

       |user checked_out_code|
