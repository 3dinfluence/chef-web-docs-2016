.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for test-kitchen.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets. 


This subcommand has the following options:

``--auto-init``
   |kitchen_auto_init| Default: ``false``.

``-c NUMBER``, ``--concurrency NUMBER``
   |concurrency| Use this option to limit the number of instances that are tested concurrently. For example, ``--concurrency 6`` will set this limit to six concurrent instances. Default: ``9999`` (all instances, effectively).

``-d``, ``--destroy``
   |kitchen_destroy| Default: ``passing``.

``-l``, ``--log-level``
   |log_level| Options (in order of priority): ``:debug``, ``:info``, ``:warn``, ``:error``, and ``:fatal``. Default: ``info``.

``PLATFORMS``
   |kitchen_platforms| For example, if the |kitchen yml| file contains the following:

   .. code-block:: javascript
   
       - name: centos-5.10
       - name: centos-6.5
       - name: fedora-19
       - name: ubuntu-1004
       - name: ubuntu-1204
       - name: ubuntu-1310
   
   then a regular expression like ``(04|5)`` would run |kitchen| against ``centos-5.10``, ``centos-6.5``, ``ubuntu-1004``, and ``ubuntu-1204``. A regular expression like ``(ubuntu)`` would run |kitchen| against ``ubuntu-1004``, ``ubuntu-1204``, and ``ubuntu-1310``. A regular expression like ``(fedora-19)`` would run |kitchen| against only ``fedora-19``. Default: ``all``.