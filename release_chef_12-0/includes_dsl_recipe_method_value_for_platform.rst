.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the ``value_for_platform`` method in a recipe to select a value based on the ``node['platform']`` and ``node['platform_version']`` attributes. These values are detected by |ohai| during every |chef client| run.

The syntax for the ``value_for_platform`` method is as follows:

.. code-block:: ruby

   value_for_platform( ["platform", ...] => { "version" => value } )

where:

* ``"platform", ...`` is a comma-separated list of platforms, such as |redhat|, |suse|, or |fedora|
* ``version`` specifies the version of that platform
* Version constraints---``>``, ``<``, ``>=``, ``<=``, ``~>``---may be used with ``version``; an exception is raised if two version constraints match and an exact match will always take precedence
* ``value`` specifies the value that will be used if the node's platform matches the ``value_for_platform`` method

When each value only has a single platform, use the following syntax:

.. code-block:: ruby

   value_for_platform(
     "platform" => { "version" => "value" },
     "platform" => { "version" => "value" },
     "platform" => "value"
   )

When each value has more than one platform, the syntax changes to:

.. code-block:: ruby

   value_for_platform(
     ["platform", "platform", ... ] => {
      "version" => "value"
     },
   )

The following example will set ``package_name`` to "httpd" for the |redhat| platform and to "apache2" for the |debian| platform:

.. code-block:: ruby

   package_name = value_for_platform(
     ["centos", "redhat", "suse", "fedora" ] => {
      "default" => "httpd"
     },
     ["ubuntu", "debian"] => {
      "default" => "apache2"
     }
   )

The following example will set ``package`` to "apache-couchdb" for |open bsd| platforms, "dev-db/couchdb" for |gentoo| platforms, and "couchdb" for all other platforms:

.. code-block:: ruby

   package = value_for_platform(
     "openbsd" => { "default" => "apache-couchdb" },
     "gentoo" => { "default" => "dev-db/couchdb" },
     "default" => "couchdb"
   )

The following example shows using version constraints to specify a value based on the version:

.. code-block:: ruby

   value_for_platform(
     "os1" => { "< 1.0" => "less than 1.0",
                "~> 2.0" => "version 2.x",
                ">= 3.0" => "version 3.0",
                "3.0.1" => "3.0.1 will always use this value" }
   )


