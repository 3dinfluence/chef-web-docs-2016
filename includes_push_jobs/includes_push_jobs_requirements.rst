.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


|push jobs| has the following requirements:

* An on-premise |chef server| version 11.0.1 (or later)
* To use the |cookbook push jobs| cookbook to configure the |push jobs| client, the |chef client| must also be present on the node (because only the |chef client| can use a cookbook to configure a node)
* TCP protocol ports 10000-10003 must be open. This allows the |push jobs| clients to communicate with the |push jobs| server. In a configuration with both front and back ends, these ports only need to be open on the back end servers. The |push jobs| server waits for connections from the |push jobs| client (and never makes a connection to a |push jobs| client).

The |push jobs| client can run on the following platforms:

* |ubuntu| 10.04, 10.10, 12.04, and 12.10
* |centos| 5 and 6
* |windows|
