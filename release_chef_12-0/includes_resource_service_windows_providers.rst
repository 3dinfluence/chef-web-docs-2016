.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The |resource service| resource does not have service-specific short names. This is because the |chef client| identifies the platform at the start of every |chef client| run based on data collected by |ohai|. The |chef client| looks up the platform in the `provider_mapping.rb <https://github.com/opscode/chef/blob/master/lib/chef/platform/provider_mapping.rb>`_ file, and then determines the correct provider for that platform. In certain situations, such as when more than one init system is available on a node, a specific provider may need to be identified by using the ``provider`` attribute and the long name for that provider.

This resource has the following providers:

.. list-table::
   :widths: 150 80 320
   :header-rows: 1

   * - Long name
     - Short name
     - Notes
   * - ``Chef::Provider::Service::Windows``
     - ``windows_service``
     - The provider that is used with the |windows| platform.

