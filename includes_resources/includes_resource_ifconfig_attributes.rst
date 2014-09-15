.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``bcast``
     - |broadcast_address|
   * - ``bootproto``
     - |boot_protocol|
   * - ``device``
     - |device ifconfig|
   * - ``hwaddr``
     - |hardware_address|
   * - ``inet_addr``
     - |internet_host_address|
   * - ``mask``
     - |netmask| For example: ``255.255.255.0``.
   * - ``metric``
     - |routing_metric|
   * - ``mtu``
     - |maximum_transmission_unit|
   * - ``network``
     - |network_address|
   * - ``onboot``
     - |onboot ifconfig|
   * - ``onparent``
     - |onparent ifconfig|
   * - ``provider``
     - Optional. |provider resource_parameter| (See "Providers" section below for more information.)
   * - ``target``
     - |target_interface| Default value: the ``name`` of the resource block. (See "Syntax" section above for more information.)