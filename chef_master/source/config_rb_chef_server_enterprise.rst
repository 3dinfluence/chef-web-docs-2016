=====================================================
|enterprise rb|
=====================================================

.. warning:: This topic documents the settings for |chef server oec|. The current version of the |chef server| is version 12. All of the documentation at http://docs.getchef.com and http://docs.getchef.com/server/ is about the current version of the |chef server|. The documentation for |chef server oec| has been moved to http://docs.getchef.com/enterprise/ and is archived for specific versions: `Enterprise Chef 11.0 <http://docs.getchef.com/release/oec_11-0/>`__, `Enterprise Chef 11.1 <http://docs.getchef.com/release/oec_11-1/>`__, and `Enterprise Chef 11.2 <http://docs.getchef.com/release/oec_11-1/>`__.

.. include:: ../../includes_config/includes_config_rb_chef_server_enterprise.rst

.. note:: If the |enterprise rb| file does not exist, create a file called ``private-chef.rb`` and put it in the ``/etc/opscode/`` directory.

Use Conditions
=====================================================
.. include:: ../../step_config/step_config_add_condition.rst

Recommended Settings
=====================================================
.. include:: ../../includes_server_tuning/includes_server_tuning_general.rst

Optional Settings
=====================================================
The following settings are often used for performance tuning of |chef server oec| in larger installations.

.. note:: When changes are made to the |enterprise rb| file the |chef server oec| must be reconfigured by running the ``private-chef-ctl reconfigure`` command.

bookshelf
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_bookshelf.rst

opscode-account
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_account.rst

opscode-chef
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_chef.rst

opscode-erchef
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_erchef.rst

opscode-expander
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_expander.rst

opscode-solr
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_solr.rst

Update Frequency
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_tuning/includes_server_tuning_solr_update_frequency.rst

opscode-webui
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_webui.rst

postgresql
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_postgresql.rst

rabbitmq
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_rabbitmq.rst

.. warning:: Review the full list of `optional settings <http://docs.opscode.com/config_rb_chef_server_enterprise_optional_settings.html>`_ that can be added to the |enterprise rb| file. Many of these optional settings should not be added without first consulting with |company_name| support.




