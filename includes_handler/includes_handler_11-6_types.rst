.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

There are two types of handlers:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Handler
     - Description
   * - exception
     - An exception handler is used to identify situations that have caused a |chef client| run to fail. An exception handler can be loaded at the start of a |chef client| run by adding a recipe that contains the ``chef_handler`` resource to a node's run-list. An exception handler runs when the ``failed?`` property for the ``run_status`` object returns ``true``.
   * - report
     - A report handler is used when a |chef client| run succeeds and reports back on certain details about that |chef client| run. A report handler can be loaded at the start of a |chef client| run by adding a recipe that contains the |resource chef_handler| resource to a node's run-list. A report handler runs when the ``success?`` property for the ``run_status`` object returns ``true``.
