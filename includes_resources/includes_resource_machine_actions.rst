.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This resource has the following actions:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Action
     - Description
   * - ``:allocate``
     - Use to create a machine, return its machine identifier, and then (depending on the provider) boot the machine to an image. This reserves the machine with the provider and subsequent ``:allocate`` actions against this machine no longer need to create the machine, just update it.
   * - ``:converge``
     - Default. Use to create a machine, return its machine identifier, boot the machine to an image with the specified parameters and transport, install the |chef client|, and then converge the machine.
   * - ``:converge_only``
     - Use to converge a machine, but only if the machine is in a ready state.
   * - ``:destroy``
     - Use to destroy a machine.
   * - ``:ready``
     - Use to create a machine, return its machine identifier, and then boot the machine to an image with the specified parameters and transport. This machine is in a ready state and may be connected to (via SSH or other transport).
   * - ``:setup``
     - Use to create a machine, return its machine identifier, boot the machine to an image with the specified parameters and transport, and then install the |chef client|. This machine is in a ready state, has the |chef client| installed, and all of the configuration data required to apply the run-list to the machine. 
   * - ``:stop``
     - Use to stop a machine.
