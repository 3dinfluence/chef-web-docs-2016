=====================================================
|chef manage_title|
=====================================================

.. include:: ../../includes_manage/includes_manage.rst

.. note:: .. include:: ../../includes_chef/includes_chef_subscriptions.rst

Nodes
=====================================================
.. include:: ../../includes_node/includes_node.rst

The |chef manage| provides ways for users to `delete nodes and reset their private keys <http://docs.chef.io/server_manage_nodes.html#manage>`_, `edit node attributes <http://docs.chef.io/server_manage_nodes.html#node-attributes>`_, `manage the run-lists <http://docs.chef.io/server_manage_nodes.html#run-lists>`_, `configure user and group permissions <http://docs.chef.io/server_manage_nodes.html#permissions>`_, and `manage tags <http://docs.chef.io/server_manage_nodes.html#manage-tags>`_.

.. image:: ../../images/step_manage_webui_nodes.png

Search
-----------------------------------------------------
.. include:: ../../includes_search/includes_search.rst

.. note:: The syntax for search queries in the |chef manage| is identical to the syntax for search queries used with |knife|, the command line tool used to manage objects on the |chef server|.

Query Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_query_syntax.rst

Keys
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_key.rst

Nested Fields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_key_nested.rst

About Patterns
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_pattern.rst

Exact Matching
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_pattern_exact.rst

Wildcard Matching
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_pattern_wildcard.rst

Range Matching
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_pattern_range.rst

Fuzzy Matching
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_search/includes_search_pattern_fuzzy.rst

About Operators
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_boolean_operators.rst

.. include:: ../../includes_search/includes_search_boolean_operators_andnot.rst

Special Characters
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_search/includes_search_special_characters.rst



Reports
=====================================================
.. include:: ../../includes_reporting/includes_reporting.rst

The |chef manage| provides ways for users to `configure the timeframe <http://docs.chef.io/server_manage_reports.html#configure-reports>`_ around which a report is built, and then to `review the reports <http://docs.chef.io/server_manage_reports.html#view-reports>`_ that are available for that timeframe.

.. image:: ../../images/step_manage_webui_reports.png

Policy
=====================================================
.. include:: ../../includes_chef/includes_chef_policy.rst

The |chef manage| provides ways for users to manage `data bags <http://docs.chef.io/server_manage_data_bags.html>`_, `environments <http://docs.chef.io/server_manage_environments.html>`_, `roles <http://docs.chef.io/server_manage_roles.html>`_, `cookbooks <http://docs.chef.io/server_manage_cookbooks.html>`_, `clients <http://docs.chef.io/server_manage_clients.html>`_, and `managing tags <http://docs.chef.io/server_manage_nodes.html#manage-tags>`_.

.. image:: ../../images/step_manage_webui_policy.png

Admin
=====================================================
.. include:: ../../includes_manage/includes_manage_admin.rst

.. include:: ../../includes_server_rbac/includes_server_rbac.rst

.. image:: ../../images/step_manage_webui_admin.png

