.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

To set up the |reporting| server for a high availability configuration:

#. Contact |company_name| and get the package that is appropriate for the |chef server| platform and operating system
#. Install the package on every machine that is running |chef server|. Every |chef server| machine must be running |chef server| version 11.0.1 or higher. For example on |ubuntu|:

   .. code-block:: bash

      $ dpkg -i opscode-reporting_1.0.1-1.ubuntu.10.04_amd64.deb

#. Reconfigure the |chef server| on the back end primary server (bootstrap):

   .. code-block:: bash

      $ private-chef-ctl reconfigure

#. Reconfigure the |reporting| server on the back end primary server (bootstrap):

   .. code-block:: bash

      $ opscode-reporting-ctl reconfigure

#. Copy the entire ``/etc/opscode-reporting`` directory from the back end primary machine to all front and back end nodes. For example, from each server run:

   .. code-block:: bash
      
      $ scp -r <Bootstrap server IP>:/etc/opscode-reporting /etc

   or from the back end primary machine:

   .. code-block:: bash
      
      $ scp -r /etc/opscode-reporting <each servers IP>:/etc

#. Reconfigure any |chef server| on which |reporting| services have been installed:

   .. code-block:: bash

      $ private-chef-ctl reconfigure

#. Reconfigure |reporting| services on each server:

   .. code-block:: bash

      $ opscode-reporting-ctl reconfigure

.. #. Restart the |reporting| components:
.. 
..    .. code-block:: bash
.. 
..       $ private-chef-ctl restart opscode-reporting

#. Verify the installation:

   .. code-block:: bash

      $ opscode-reporting-ctl test
