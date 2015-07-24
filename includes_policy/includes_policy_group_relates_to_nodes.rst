.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Each node has a 1:many relationship with policy settings stored on the |chef server|. This relationship is based on the policy group to which the node is associated, and then the policy settings assigned to that group:

* A policy is typically named after the functional role ahost performs, such as "application server", "chat server", "load balancer", and so on
* A policy group defines a set of hosts in a deployed units, typically mapped to organizational requirements such as "dev", "test", "staging", and "production", but can also be mapped to more detailed requirements as needed
