=====================================================
|push jobs|
=====================================================

.. include:: ../../includes_push_jobs/includes_push_jobs.rst

.. note:: |push jobs| is an add-on feature for on-premise installations of the |chef server oec| server only.

Install `Push Jobs <http://docs.getchef.com/install_push_jobs.html>`_ using the |cookbook push jobs| cookbook and a |chef client| run on each of the target nodes.

Requirements
=====================================================
.. include:: ../../includes_push_jobs/includes_push_jobs_requirements.rst

Components
=====================================================
.. include:: ../../includes_push_jobs/includes_push_jobs_component.rst

The following diagram shows the various components of |push jobs|:

.. image:: ../../images/overview_push_jobs_states.png


Jobs
-----------------------------------------------------
.. include:: ../../includes_push_jobs/includes_push_jobs_component_jobs.rst

Nodes
-----------------------------------------------------
.. include:: ../../includes_push_jobs/includes_push_jobs_component_nodes.rst

Workstations
-----------------------------------------------------
.. include:: ../../includes_push_jobs/includes_push_jobs_component_workstations.rst


|cookbook push jobs| Cookbook
=====================================================
The |cookbook push jobs| cookbook contains attributes that are used to configure the |push jobs| client. In addition, |push jobs| relies on the ``whitelist`` attribute to manage the list of jobs (and commands) that are available to |push jobs|.

Whitelist
-----------------------------------------------------
.. include:: ../../includes_push_jobs/includes_push_jobs_whitelist.rst

.. 
.. Commented out, probably move to new file(s)
.. 
.. Messages
.. =====================================================
.. xxxxx sends two types of messages: heartbeat and job.
.. 
.. Heartbeat Messages
.. -----------------------------------------------------
.. .. include:: ../../includes_push_jobs/includes_push_jobs_messages_heartbeat.rst
.. 
.. Job Messages
.. -----------------------------------------------------
.. .. include:: ../../includes_push_jobs/includes_push_jobs_messages_jobs.rst

Reference
=====================================================
The following sections describe the |knife| subcommands, the |api push jobs|, and configuration settings used by |push jobs|.


|subcommand knife push jobs|
=====================================================
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs.rst

.. note:: Review the list of `common options <http://docs.opscode.com/knife_common_options.html>`_ available to this (and all) |knife| subcommands and plugins.

.. Install this plugin
.. -----------------------------------------------------
.. .. include:: ../../step_plugin_knife/step_plugin_knife_push_jobs_install_rubygem.rst

job list
-----------------------------------------------------
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_list.rst

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_list_syntax.rst

Options
+++++++++++++++++++++++++++++++++++++++++++++++++++++
|no_options|

job start
-----------------------------------------------------
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_start.rst

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_start_syntax.rst

Options
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_start_options.rst

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
**Run a job**

.. include:: ../../step_plugin_knife/step_plugin_knife_push_jobs_job_start_run_job.rst

**Run a job using quorum percentage**

.. include:: ../../step_plugin_knife/step_plugin_knife_push_jobs_job_start_search_by_quorum.rst

**Run a job using node names**

.. include:: ../../step_plugin_knife/step_plugin_knife_push_jobs_job_start_search_by_nodes.rst

job status
-----------------------------------------------------
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_status.rst

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_job_status_syntax.rst

Options
+++++++++++++++++++++++++++++++++++++++++++++++++++++
|no_options|

Examples
+++++++++++++++++++++++++++++++++++++++++++++++++++++
**View job status by job identifier**

.. include:: ../../step_plugin_knife/step_plugin_knife_push_jobs_job_status_by_id.rst

node status
-----------------------------------------------------
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_node_status.rst

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_plugin_knife/includes_plugin_knife_push_jobs_node_status_syntax.rst

Options
+++++++++++++++++++++++++++++++++++++++++++++++++++++
|no_options|



|api push jobs|
=====================================================
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs.rst

.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint.rst

connect/NODE_NAME
-----------------------------------------------------
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_name.rst

GET
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_name_get.rst

jobs
-----------------------------------------------------
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_jobs.rst

GET
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_jobs_get.rst

POST
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_jobs_post.rst

jobs/ID
-----------------------------------------------------
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_jobs_id.rst

GET
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_jobs_id_get.rst

node_states
-----------------------------------------------------
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_states.rst

GET
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_states_get.rst

node_states/NODE_NAME
-----------------------------------------------------
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_name.rst

GET
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_push_jobs/includes_api_push_jobs_endpoint_node_name_get.rst



|push jobs client|
=====================================================
.. include:: ../../includes_push_jobs/includes_push_jobs.rst

.. include:: ../../includes_ctl_push_jobs_client/includes_ctl_push_jobs_client.rst

Options
-----------------------------------------------------
.. include:: ../../includes_ctl_push_jobs_client/includes_ctl_push_jobs_client_options.rst



|push_jobs_server rb|
=====================================================
.. include:: ../../includes_config/includes_config_rb_push_jobs_server.rst

Settings
-----------------------------------------------------
.. include:: ../../includes_config/includes_config_rb_push_jobs_server_settings.rst