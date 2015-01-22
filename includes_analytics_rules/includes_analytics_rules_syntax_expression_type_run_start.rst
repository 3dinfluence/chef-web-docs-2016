.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following fields are available for the ``run_start`` message type:

.. list-table::
   :widths: 120 60 320
   :header-rows: 1

   * - Field
     - Type
     - Description
   * - ``chef_server_fqdn``
     - string
     - The |fqdn| for the |chef server| against which the instance is running. For example: ``"api.chef.io"``.
   * - ``id``
     - string
     - The internal message identifier for the |chef client| run. For example: ``"12345678-9012-3456-7890-12345678901211"``.
   * - ``message_type``
     - string
     - The message type. For example: ``"run_start"``.
   * - ``message_version``
     - string
     - The message version. For example: ``"0.1.0"``.
   * - ``node_name``
     - string
     - The name of the node on which the |chef client| run occurred. For example: ``"grantmc01-abc"``.
   * - ``organization_name``
     - string
     - The short name of the organization to which the node belongs. For example: ``"chef"``.
   * - ``run_id``
     - string
     - The identifier for the |chef client| run. For example: ``"67890123-4567-8901-2345-67890123456789"``.
   * - ``start_time``
     - string
     - The ISO timestamp at which the |chef client| run started. For example: ``"2014-06-05T10:34:35Z"``.

