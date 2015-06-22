.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This |chef provisioning| driver-specific resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``description``
     - Use to specify the description for the network interface.
   * - ``device_index``
     - Use to specify the attachment order position for the network interface.
   * - ``machine``
     - Use to specify the name of the |amazon aws| instance for which this network interface is associated.
   * - ``name``
     - Use to specify the name of the network interface.
   * - ``network_interface_id``
     - Use to specify the identifier for the network interface.
   * - ``private_ip_address``
     - Use to assign a private IP address to the network interface. This IP address will be used as the primary IP address.
   * - ``security_groups``
     - Use to specify one (or more) security group identifiers to be associated with the network interface.
   * - ``subnet``
     - Use to specify the identifier of the subnet to be associated with the network interface.
