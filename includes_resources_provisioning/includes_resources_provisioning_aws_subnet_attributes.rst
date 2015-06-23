.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This |chef provisioning| driver-specific resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``availability_zone``
     - Use to specify the availability zone for the subnet. For example: ``us-east-1a`` or ``us-east-1b``. Default value: selected automatically by |amazon aws|.
   * - ``aws_tags``
     - |aws_tag|

       .. include:: ../../includes_resources_provisioning/includes_resources_provisioning_aws_attributes_aws_tag_example.rst
   * - ``chef_server``
     - |provisioning_server|
   * - ``cidr_block``
     - Required. Use to specify the |cidr| block of IP address that are associated with a subnet. This must be a subset of the IP addresses in the defined virtual network and must not overlap with any other IP addresses used by any other subnet within this defined virtual network. For example, ``'10.0.0.0/24'`` will give 256 addresses and ``'10.0.0.0/16'`` will give 65536.
   * - ``driver``
     - |driver_provisioning|
   * - ``managed_entry_store``
     - |managed_entry_store| For example: ``Chef::Provisioning.chef_managed_entry_store(self.chef_server)``.
   * - ``map_public_ip_on_launch``
     - Use to specify if public IP addresses are assigned to new instances in this subnet by default. Default value: ``false``.
   * - ``route_table``
     - Use to specify the route table associated with this subnet. This may be the name of an ``aws_route_table`` resource block that exists elsewhere in a cookbook, an actual ``aws_route_table`` resource block that exists in this recipe, or the name of the main route table in |amazon vpc|. Default value: ``:default_to_main``, which will detach any explicit route table that may be associated with this subnet, and then use the subnet that exists for the defined virtual network in which this subnet exists.
   * - ``subnet_id``
     - Use to specify the identifier for the subnet.
