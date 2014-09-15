.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``arch``
     - |architecture package|
   * - ``options``
     - |command options| For example, common |aptget| directives, such as ``--no-install-recommends``. See the `apt-get man page <http://manpages.debian.net/cgi-bin/man.cgi?query=apt-get>`_ for the full list.
   * - ``package_name``
     - |name package| Default value: the ``name`` of the resource block (see Syntax section above).
   * - ``provider``
     - Optional. |provider resource_parameter| (See "Providers" section below for more information.)
   * - ``response_file``
     - Optional. |response_file|
   * - ``source``
     - Optional. |source resource apt_package|
   * - ``version``
     - |version package|


