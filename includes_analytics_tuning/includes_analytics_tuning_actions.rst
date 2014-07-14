.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following settings are often modified from the default as part of the tuning effort for the |service actions| service:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``actions['manage_endpoint']``
     - |manage_endpoint| If your |chef server oec| has a |chef manage| installation which is on a different port or host from the |api chef server|, specify the full URL to the root of the |chef manage| installation here, e.g. ``"http://manage.example.com:8080"``.
   * - ``actions['session_expiry']``
     - |session_expiry| If web clients are timing out too quickly, increase this setting. Default value: ``30``.


