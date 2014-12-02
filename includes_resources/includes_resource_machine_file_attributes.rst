.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``chef_server``
     - |chef_server_url|
   * - ``content``
     - |content file| The default behavior will not modify content.
   * - ``driver``
     - Use to specify the driver to be used for provisioning.
   * - ``group``
     - |windows group_identifier|
   * - ``local_path``
     - The local path to a file.
   * - ``machine``
     - Use to specify the machine type.
   * - ``mode``
     - |mode resource_file|
       
       The behavior is different depending on the platform.
       
       |unix|- and |linux|-based systems: |mode *nix|
       
       |windows|: |mode windows security|

   * - ``owner``
     - |owner windows security|
   * - ``path``
     - |path full_path_to_file| Default value: the ``name`` of the resource block. |see syntax|

       |windows|: A path that begins with a forward slash (``/``) will point to the root of the current working directory of the |chef client| process. This path can vary from system to system. Therefore, using a path that begins with a forward slash (``/``) is not recommended.











