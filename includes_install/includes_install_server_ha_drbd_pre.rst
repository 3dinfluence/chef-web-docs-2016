.. The contents of this file may be included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Before installing the |chef server| software, perform the following steps:

* Backend machines `should have a dedicated connection <http://www.drbd.org/users-guide/s-prepare-network.html>`_. This is required for replication between the two machines.
* Backend machines will share a virtual IP address that must also be accessible from each frontend server. This virtual IP address is created and managed by the |chef server|, but will also need to be added to the DNS so that all machines in the high availability configuration may access it.
* Persistent data on backend machines of the |chef server| is primarily composed of cookbook files and directories. Separate disks should be dedicated entirely to storing this data prior to installing the |chef server|.
* Load-balancing should be used with frontend machines, along with a DNS entry for the virtual IP address used for load balancing. This virtual IP address is added to the |chef server rb| file as the ``api_fqdn``. 
* All required ports must be open. See the Firewalls section (below) for the list of ports. All connections to and from the |chef server| are accomplished via TCP. Refer to the operating system's manual or your systems administrators for instructions on how to configure to ports, if necessary.
* The hostname for the |chef server| must be an |fqdn|, including the domain suffix, and must be resolvable by the other backend and frontends. See `Hostnames, FQDNs <http://docs.getchef.com/install_server_pre.html#hostnames>`_ for more information.
