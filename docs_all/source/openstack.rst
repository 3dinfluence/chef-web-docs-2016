.. THIS PAGE IS LOCATED AT THE /chef/ PATH.

=====================================================
|openstack chef|
=====================================================

.. include:: ../../includes_openstack/includes_openstack.rst

This page describes how to use the |openstack chef| cookbooks as the basis for managing an |openstack| deployment with |chef|, as well as how to participate in the development and maintenance process of these cookbooks. For more information about |openstack| itself, see http://docs.openstack.org.


Architecture
=====================================================
This section describes the supported deployment scenarios for |openstack chef| and is based on the `OpenStack Grizzly <http://www.solinea.com/2013/06/15/openstack-grizzly-architecture-revisited/>`_ release.

.. image:: ../../images/openstack-arch-grizzly-conceptual-v2.jpg

There are a number of configuration options available, including block storage, hypervisors, databases, message queuing, networking, object storage, source builds, and so on. The current supported deployment scenarios include the following:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Scenario
     - Description
   * - All-in-One Compute
     - A full |openstack compute| deployment on a single host. No object storage.
   * - Single Controller + N Compute
     - A single controller with 1 or more |openstack compute| nodes. No object storage.
   * - |vagrant|
     - A virtual instance on a single host using |vagrant|.

.. note:: |openstack chef| is under very active development for the |openstack grizzly| release. |openstack| is flexible and additional configurations will be supported in the future.

All-in-One
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_architecture_allinone.rst

Roles
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_allinone_roles.rst

Environments
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_allinone_environments.rst

1 Controller, N Compute
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_architecture_1+n.rst

Vagrant
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_architecture_vagrant.rst

Vagrantfile
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_vagrant_vagrantfile.rst

Install
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_vagrant_configure.rst

Environments
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_vagrant_environment.rst

Usage
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_architecture_vagrant_usage.rst

Deployment Prerequisites
=====================================================
.. include:: ../../includes_openstack/includes_openstack_deploy.rst

|chef|
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_deploy_prereq_chef.rst

Hardware
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_deploy_prereq_hardware.rst

Network
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_deploy_prereq_network.rst

Operating Systems
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_deploy_prereq_os.rst

Images
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_deploy_prereq_images.rst


Development
=====================================================
.. include:: ../../includes_openstack/includes_openstack_develop.rst

|irc|
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_develop_irc.rst

|google|
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_develop_google.rst

Issue Tracking
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_develop_issues.rst

Feature Tracking
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_develop_features.rst


Repository
=====================================================
.. include:: ../../includes_openstack/includes_openstack_repo.rst

|berkshelf|
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_repo_berkshelf.rst

|spiceweasel|
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_repo_spiceweasel.rst

Roles
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_repo_roles.rst

Cookbooks
=====================================================
.. include:: ../../includes_openstack/includes_openstack_cookbooks.rst

The canonical upstream cookbooks and example repository are located in the `Stackforge Github organization <https://github.com/stackforge/>`_. Each integrated |openstack| project has a separate cookbook and repository.

|openstack| Cookbooks
-----------------------------------------------------
The following table lists all of the cookbooks that are available for |openstack chef|:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Cookbook
     - Description
   * - block-storage
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_block_storage.rst
   * - common
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_common.rst
   * - compute
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_compute.rst
   * - dashboard
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_dashboard.rst
   * - identity
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_identity.rst
   * - image
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_image.rst
   * - metering
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_metering.rst
   * - network
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_network.rst
   * - object-storage
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_object_storage.rst
   * - ops-database
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_ops_database.rst
   * - ops-messaging
     - .. include:: ../../includes_openstack/includes_openstack_cookbooks_ops_messaging.rst

.. note:: All |openstack| cookbooks are prefaced with ``cookbook-openstack-`` in addition to the name listed in the previous table. For example: ``cookbook-openstack-block-storage`` or ``cookbook-openstack-ops-messaging``.

Contribute
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_cookbooks_contribute.rst

Commit Messages
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_cookbooks_contribute_commit_messages.rst

Code Review
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_cookbooks_contribute_code_review.rst

Test Cookbooks
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_cookbooks_test.rst



Install
=====================================================
.. include:: ../../includes_openstack/includes_openstack_install.rst


knife-openstack
=====================================================
See http://docs.chef.io/plugin_knife_openstack.html.



Example Deployment
=====================================================

.. include:: ../../includes_openstack/includes_openstack_example.rst

.. image:: ../../images/openstack-lab.png

lab-repo
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo.rst

Environment
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_environment.rst

Roles
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_roles.rst

lab-admin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_roles_lab_admin.rst

lab-base
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_roles_lab_base.rst

Data Bags
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_data_bags.rst

pxe_dust
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_data_bags_pxe_dust.rst

users
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_data_bags_users.rst

Cookbooks
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_lab_repo_cookbooks.rst

Network
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_example_network.rst

Admin 10.0.0.0/24
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_network_admin.rst

Public 172.16.100.0/24
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_network_public.rst

Storage 192.160.0.0/24
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_network_storage.rst

Hardware
-----------------------------------------------------
.. include:: ../../includes_openstack/includes_openstack_example_hardware.rst

mom.lab.atx
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_hardware_mom.rst

crushinator.lab.atx
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_hardware_crushinator.rst

ignar.lab.atx/larry.lab.atx
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_hardware_ignar.rst

lrrr.lab.atx
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_openstack/includes_openstack_example_hardware_lrrr.rst


For More Information ...
=====================================================
We are a community of developers, deployers and integrators who make working with |openstack| consistent and automated. Join us!

.. list-table::
   :widths: 150 450
   :header-rows: 0

   * - |irc|
     - ``#openstack-chef`` is our channel on ``irc.freenode.net``. Many useful conversations and debugging sessions happen there. Archives are available at `community.opscode.com/chat/openstack-chef <http://community.opscode.com/chat/openstack-chef>`_
   * - Mailing List
     - `groups.google.com/group/opscode-chef-openstack <http://groups.google.com/group/opscode-chef-openstack>`_ is the mailing list. Traffic is typically a few posts a day, a great place for updates and longer discussions
   * - |openstack chef| Wiki
     - `wiki.openstack.org <https://wiki.openstack.org/wiki/Chef/GettingStarted>`_ most of this information is migrated here
   * - |twitter|
     - `@chefopenstack <http://twitter.com/chefopenstack>`_

If you have questions or concerns outside the mailing list, please email matt@opscode.com.