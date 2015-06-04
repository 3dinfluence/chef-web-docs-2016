.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Guidelines for |openstack chef|:

* Cookbooks are developed and tested with the latest release of the |chef client|
* Most users will install the full-stack client using the |omnibus installer|: http://www.chef.io/chef/install/
* |ruby| 2.1 or later is assumed
* A |chef server| is being used; |chef solo| may not work (patches welcome)
* Cookbooks expose their configuration via attributes
* Attributes are typically overridden by environment attributes
* Roles do not provide attributes
* Search may be short-circuited by attributes that provide a value, such as the IP addresses of services
* Data bags are used for passwords and the like
* `Berkshelf <http://berkshelf.com/>`_ is used to manage cookbook versions in the |openstack chef_repo|
* `Foodcritic <http://acrmp.github.io/foodcritic/>`_ is used for lint-checking the cookbooks
* `ChefSpec <https://github.com/acrmp/chefspec>`_ is used for basic unit acceptance tests
