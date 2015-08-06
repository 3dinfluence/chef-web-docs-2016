.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This |chef provisioning| driver-specific resource has the following properties:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Property
     - Description
   * - ``aws_tags``
     - **Ruby Type:** Hash

       |aws_tag|

       .. include:: ../../includes_resources_provisioning/includes_resources_provisioning_aws_attributes_aws_tag_example.rst
   * - ``certificate_body``
     - **Ruby Type:** String

       Use to specify the contents of the public key certificate in PEM-encoded format.
   * - ``chef_server``
     - **Ruby Type:** Hash

       |provisioning_server|
   * - ``driver``
     - **Ruby Type:** Chef::Provisioning::Driver

       |driver_provisioning|
   * - ``managed_entry_store``
     - **Ruby Type:** Chef::Provisioning::ManagedEntryStore

       |managed_entry_store| For example: ``Chef::Provisioning.chef_managed_entry_store(self.chef_server)``.
   * - ``name``
     - **Ruby Type:** String

       Use to specify name of the server certificate.
   * - ``private_key``
     - **Ruby Type:** 

       Use to specify contents of the private key in PEM-encoded format.
