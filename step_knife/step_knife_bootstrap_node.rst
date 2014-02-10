.. This is an included how-to. 


.. To bootstrap a node:

.. code-block:: bash

   $ knife bootstrap 12.34.56.789 -P vanilla -x root -r 'recipe[apt],recipe[xfs],recipe[vim]'

which shows something similar to:

.. code-block:: bash

   ...
   12.34.56.789 Chef Client finished, 12/12 resources updated in 78.942455583 seconds

Use ``knife node show`` to verify:

.. code-block:: bash

   $ knife node show debian-wheezy.int.domain.org

which returns something similar to:

.. code-block:: bash

   Node Name:   debian-wheezy.int.domain.org
   Environment: _default
   FQDN:        debian-wheezy.int.domain.org
   IP:          12.34.56.789
   Run List:    recipe[apt], recipe[xfs], recipe[vim]
   Roles:
   Recipes:     apt, xfs, vim, apt::default, xfs::default, vim::default
   Platform:    debian 7.4
   Tags:
