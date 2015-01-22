.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following diagram shows the stages of the |chef client_audit| phase of the |chef client| run, and then the list below the diagram describes in greater detail each of those stages.

.. image:: ../../images/audit_run.png

When the |chef client| is run in |chef client_audit|, the following happens:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Stages
     - Description
   * - **chef-client Run ID**
     - The |chef client| run identifier is associated with each audit.
   * - **Configure the Node**
     - If |chef client_audit| is run as part of the full |chef client| run, |chef client_audit| occurs after the |chef client| has finished converging all resources in the resource collection.
   * - **Audit node based on controls in cookbooks**
     - Each ``control_group`` and ``control`` block found in any recipe that was part of the run-list of for the node is evaluated, with each expression in each ``control`` block verified against the state of the node.
   * - **Upload audit data to the Chef server**
     - When |chef client_audit| mode is complete, the data is uploaded to the |chef server|.
   * - **Send to Chef Analytics**
     - Most of this data is passed to the |chef analytics| platformfor further analysis, such as rules processing (for notification events triggered by expected or unexpected audit outcomes) and visibility from the actions web user interface.