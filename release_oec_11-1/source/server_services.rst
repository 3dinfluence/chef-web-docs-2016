.. THIS PAGE DOCUMENTS Enterprise Chef server version 11.1

=====================================================
Services
=====================================================

.. include:: ../../includes_server_services/includes_server_services.rst

Service Subcommands
=====================================================
|chef server oec| has a built in process supervisor, which ensures that all of the required services are in the appropriate state at any given time. The supervisor starts two processes per service.

hup
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_hup.rst

int
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_int.rst

kill
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_kill.rst

once
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_once.rst

restart
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_restart.rst

service-list
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_service_list.rst

start
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_start.rst

status
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_status.rst

High Availability
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_status_ha.rst

Log Files
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_status_logs.rst

stop
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_stop.rst

tail
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_tail.rst

term
-----------------------------------------------------
.. include:: ../../includes_ctl_private_chef/includes_ctl_private_chef_term.rst


List of Services
=====================================================
The following services are part of |chef server oec|:

* bifrost
* bookshelf
* couchdb
* keepalived
* nginx
* opscode-account
* opscode-certificate
* opscode-erchef
* opscode-expander
* opscode-expander-reindexer
* opscode-org-creator
* opscode-solr
* opscode-webui
* postgresql
* rabbitmq
* redis

All services have the following options: ``status``, ``start``, ``stop``, ``restart``, ``kill``, ``run once``, and ``tail``.

bifrost
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_bifrost.rst

bookshelf
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_bookshelf.rst

couchdb
-----------------------------------------------------
The |service couchdb| service is used to store key/value data.

keepalived
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_keepalived.rst

nginx
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_nginx.rst

opscode-account
-----------------------------------------------------
The |service account| service is a |ruby|-based service that handles the following types of |api chef server| requests:

* ACLs
* Association requests
* Containers
* Groups
* Organizations
* Clients
* Users

.. note:: This service is deprecated in |chef server| 12.

opscode-certificate
-----------------------------------------------------
The |service certificate| service is used to provide the certificates that are returned when the |chef client| is set up and configured on nodes and workstations.

.. note:: This service is deprecated in |chef server| 12.

opscode-erchef
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_erchef.rst

opscode-expander
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_expander.rst

opscode-expander-reindexer
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_reindexer.rst

opscode-solr
-----------------------------------------------------
The |service solr| service is used to create the search indexes.

opscode-webui
-----------------------------------------------------
The |service webui| service is used to mange the web user interface for the |chef server|.

postgresql
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_postgresql.rst

rabbitmq
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_rabbitmq.rst

redis
-----------------------------------------------------
.. include:: ../../includes_server_services/includes_server_services_redis.rst
