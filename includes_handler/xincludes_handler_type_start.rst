.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A start handler is a newer feature within the larger set of handler functionality. They became necessary when |company_name| started building add-ons for |chef server oec|. The |reporting| add-on is designed to create reporting data based on a |chef client| run. And since |reporting| needs to be able to collect data for the entire |chef client| run, |reporting| needs to be enabled before anything else happens.

A start handler is not loaded into the |chef client| run from a recipe, but is instead listed in the |client rb| file using the ``start_handlers`` attribute. The start handler must be installed on the node and be available to the |chef client| prior to the start of the |chef client| run. Use the |cookbook chef_client| cookbook to install the start handler.

Start handlers are made available to the |chef client| run in one of the following ways:

* By adding a start handler to the |cookbook chef_client| cookbook, which installs the handler on the node so that it is available to the |chef client| at the start of the |chef client| run
* By adding the handler to one of the following settings in the node's client.rb file: ``start_handlers``


