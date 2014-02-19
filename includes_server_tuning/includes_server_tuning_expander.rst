.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following setting is often modified from the default as part of the tuning effort for the |service expander| service:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_expander['nodes']``
     - |worker_processes| The |service expander| service runs on the back-end and feeds data to the |service solr| service, which creates and maintains search data used by the |chef server|. Additional memory may be required by these worker processes depending on the frequency and volume of |chef client| runs across the organization, but only if the back-end machines have available CPU and RAM.. Default value: ``2``.

