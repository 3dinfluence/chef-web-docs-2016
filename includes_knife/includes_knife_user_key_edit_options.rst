.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Knife.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This argument has the following options:

``-c``, ``--create-key``
   |key create_public| To replace the public key with an existing public key, use ``--public-key`` instead.

``-e DATE``, ``--expiration-date DATE``
   |key expiration_date| If this option is not specified, the public key will not have an expiration date. For example: ``2013-12-24T21:00:00Z``.

``-f FILE``, ``--file FILE``
   |file public_key| If the ``--key-name`` and ``public-key`` options are not specified the |chef server| will generate a private key.

``-k NAME``, ``--key-name NAME``
   |name key_public| 

``-p FILE_NAME``, ``--public-key FILE_NAME``
   |path key_public| If this option is not specified, and only if ``--key-name`` is specified, the |chef server| will generate a public/private key pair.
