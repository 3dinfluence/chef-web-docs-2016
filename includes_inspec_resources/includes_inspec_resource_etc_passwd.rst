.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the ``passwd`` |inspec resource| to test the contents of ``/etc/passwd``, which contains the following information for users that may log into the system and/or as users that own running processes. The format for ``/etc/passwd`` includes:

* A username
* The password for that user (on newer systems passwords should be stored in ``/etc/shadow`` )
* The user identifier (UID) assigned to that user
* The group identifier (GID) assigned to that user
* Additional information about that user
* That user's home directory
* That user's default command shell

defined as a colon-delimited row in the file, one row per user:

.. code-block:: bash

   root:x:1234:5678:additional_info:/home/dir/:/bin/bash
