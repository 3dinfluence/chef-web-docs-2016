.. This is an included how-to. 


To use an intermediate certificate, append both the server and intermediate certificates into a single ``.crt`` file. For example:

.. code-block:: bash

   $ cat server.crt intermediate.crt >> /var/opt/opscode/nginx/ca/FQDN.crt
