.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Knife.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following ``knife bootstrap`` settings can be added to the |knife rb| file:

``knife[:bootstrap_curl_options]``
   Adds the ``--bootstrap-curl-options`` option.

``knife[:bootstrap_install_command]``
   Adds the ``--bootstrap-install-command`` option.

``knife[:bootstrap_no_proxy]``
   Adds the ``--bootstrap-no-proxy`` option.

``knife[:bootstrap_proxy]``
   Adds the ``--bootstrap-proxy`` option.

``knife[:bootstrap_template]``
   Adds the the ``--bootstrap-template`` option.

``knife[:bootstrap_url]``
   Adds the the ``--bootstrap-url`` option.

``knife[:bootstrap_vault_item]``
   Adds the the ``--bootstrap-vault-item`` option.

``knife[:bootstrap_version]``
   Adds the the ``--bootstrap-version`` option.

``knife[:bootstrap_wget_options]``
   Adds the the ``--bootstrap-wget-options`` option.

``knife[:run_list]``
   Adds the the ``--run-list`` option.

``knife[:template_file]``
   Adds the the ``--bootstrap-template`` option.

``knife[:use_sudo]``
   Adds the the ``--sudo`` option.

.. note:: The ``knife bootstrap`` subcommand relies on a number of |ssh|-related settings that are handled by the ``knife ssh`` subcommand.
