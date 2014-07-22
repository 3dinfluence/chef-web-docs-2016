.. This is an included how-to. 


To install the |chef client| on a workstation, you must run the |omnibus installer|.

To run the |omnibus installer|:

#. Run the command that appears (for |unix| and |linux| environments) or download the |omnibus installer| (for |windows| environments). For example, for the |mac os x|:

   .. code-block:: bash

      curl -L https://www.getchef.com/chef/install.sh | sudo bash

   and then enter the password for the local machine.
#. As the |chef client| is being installed, the command window will show something like the following:

   .. code-block:: bash

      Downloading Chef for mac_os_x...
        % Total    % Received  % Xferd   Average  Speed    Time     Time      Time   Current
                                         Dload   Upload    Total    Spent     Left   Speed
      100 23.9M  100 23.9M     0     0    944k       0   0:00:26  0:00:26  --:--:--   838k
      Installing Chef

#. When the installation is finished enter the following to verify that the |chef client| was installed:

   .. code-block:: bash

      chef-client -v

   When the |chef client| is installed correctly, the command shell will return a note that says the version of that was installed. For example:

   .. code-block:: bash

      Chef: 11.4.0

#. After the |chef client| has been installed, the following folder structure will be present on the local machine::

      /opt
         /chef
            /bin
            /embedded
               /bin
               /include
               /lib
               /share
               /ssl
