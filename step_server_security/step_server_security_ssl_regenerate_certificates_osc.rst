.. This is an included how-to. 


|ssl| certificates should be regenerated periodically. This is an important part of protecting |chef server osc| from vulnerabilities and helps to prevent the information stored on the |chef server osc| server from being compromised.

To regenerate |ssl| certificates:

#. Run the following command:

   .. code-block:: bash
   
      $ chef-server-ctl stop

#. If the |chef server osc| server uses |chef server osc|-generated |ssl| certificates, |chef server osc| can regenerate them. These certificates will be located in ``/var/opt/chef-server/nginx/ca/`` and will be named after the |fqdn| for the |chef server osc| server. To determine the |fqdn| for the server, run the following command:

   .. code-block:: bash

      $ hostname -f

   Please delete the files found in the ca directory with names like this ``$FQDN.crt`` and ``$FQDN.key``.

#. If your organization has provided custom |ssl| certificates to the |chef server osc| server, they are located in ``/etc/chef-server/chef-server.rb`` as values for the ``nginx[‘ssl_certificate’]`` and ``nginx[‘ssl_certificate_key’]`` settings. Delete these files and regenerate new keys using the same authority.

#. Run the following command, |chef server osc|-generated |ssl| certificates will automatically be created if necessary:

   .. code-block:: bash

      $ chef-server-ctl reconfigure

#. Run the following command:

   .. code-block:: bash

      $ chef-server-ctl start


