.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``run_status`` object is initialized by the |chef client| before the ``report`` method is run for any handler. The ``run_status`` keeps track of the status of the |chef client| run and will contain some (or all) of the following properties:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Property
     - Description
   * - ``all_resources``
     - |handler method_all_resources|
   * - ``backtrace``
     - |handler method_backtrace|
   * - ``elapsed_time``
     - |handler method_elapsed_time|
   * - ``end_time``
     - |handler method_end_time|
   * - ``exception``
     - |handler method_exception|
   * - ``failed?``
     - |handler method_failed| An exception handler runs when the ``failed?`` indicator is ``true``.
   * - ``node``
     - |handler method_node|
   * - ``run_context``
     - |handler method_run_context|
   * - ``start_time``
     - |handler method_start_time|
   * - ``success?``
     - |handler method_success| A report handler runs when the ``success?`` indicator is ``true``.
   * - ``updated_resources``
     - |handler method_updated_resources|

.. note:: These properties are not always available. For example, a start handler runs at the beginning of the |chef client| run, which means that properties like ``end_time`` and ``elapsed_time`` are still unknown and will be unavailable to the ``run_status`` object.

