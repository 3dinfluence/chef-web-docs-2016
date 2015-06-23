.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This |chef provisioning| driver-specific resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``cidr_block``
     - Required. Use to specify the |cidr| block of IP address that are associated with a defined virtual network. For example, ``'10.0.0.0/24'`` will give 256 addresses and ``'10.0.0.0/16'`` will give 65536.
   * - ``dhcp_options``
     - Use to specify the DHCP options for the defined virtual network.
   * - ``enable_dns_hostnames``
     - Use to specify if instances launched in a defined virtual network are assigned DNS hostnames. Possible values: ``true`` or ``false``. When ``true``, ``enable_dns_support`` must also be set to ``true``.
   * - ``enable_dns_support``
     - Use to specify if DNS resolution is supported for a defined virtual network. When ``false``, resolution of public DNS hostnames to IP addresses is disabled. When ``true``, queries made to either the DNS server provided by |amazon aws| (and located at the 169.254.169.253 IP address) or the reserved IP address at the base of the defined virtual network range (plus two) will be resolved successfully. For example, a reserved IP address of ``10.0.0.0/16`` is located at ``10.0.0.2``.
   * - ``instance_tenancy``
     - Use to specify if an instance that runs in the defined virtual network instance will run on hardware that is dedicated to a single customer and is physically isolated at the host hardware level from non-dedicated instances. Set to ``:default`` when the instance runs on shared hardware. Set to ``:dedicated`` when the instance runs on dedicated hardware. Default value: ``:default``.
   * - ``internet_gateway``
     - Use to specify if a defined virtual network has an internet gateway. Possible values: ``true`` or ``false``. When ``true``, an internet gateway is created and attached to the defined virtual network. When ``false``, an internet gateway is deleted when the ``Owned`` tag on the internet gateway is ``true`` and is detached if the tag is ``false``.
   * - ``main_route_table``
     - Use to specify the main route table. This may be the name of an ``aws_route_table`` resource block that exists elsewhere in a cookbook, an actual ``aws_route_table`` resource block that exists in this recipe, or the name of the main route table in |amazon vpc|.

       Use ``main_route_table`` by itself (without specifying ``main_routes``) to update the main route association to point to the specified route table. In this situation, use the ``aws_route_table`` resource to manage the route table itself.
   * - ``main_routes``
     - Use to specify a |ruby hash| that defines the routes for the main route table. The destination (on the left side of the ``=>``) must be a |cidr| block. The target (on the right side of the ``=>``) may be the identifier for an internet gateway, an instance name, the identifier for network interface, a |chef provisioning| machine name, or a |chef provisioning| resource.

       For example:

       .. code-block:: ruby

          main_routes {
          '10.0.0.0/8' => 'internal_vpn',
          '0.0.0.0/0' => :internet_gateway
          }

       Use ``main_routes`` by itself (without specifying ``main_route_table``) to update the default route table that is created when |amazon aws| creates |amazon vpc|.
   * - ``name``
     - Use to specify the name of the defined virtual network. Because the name of a |amazon vpc| instance is not guaranteed to be unique for an account at |amazon aws|, |chef provisioning| will store the associated identifier on the |chef server| using the ``data/aws_vpc/<name>`` data bag.
   * - ``vpc_id``
     - Use to specify the identifier for the |amazon vpc|.
