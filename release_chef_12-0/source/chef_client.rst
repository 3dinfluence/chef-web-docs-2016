.. THIS PAGE IS IDENTICAL TO docs.getchef.com/essentials_chef_client.html BY DESIGN
.. THIS PAGE DOCUMENTS chef-client version 12.0

=====================================================
|chef client_title|
=====================================================

.. include:: ../../includes_chef_client/includes_chef_client.rst

.. note:: |daemonize chef_client|

Node Types
=====================================================

.. include:: ../../includes_node/includes_node.rst

There following types of nodes can be managed by the |chef client|:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Feature
     - Description
   * - .. image:: ../../images/icon_node_cloud.png
     - .. include:: ../../includes_node/includes_node_type_cloud.rst
   * - .. image:: ../../images/icon_node_physical.png
     - .. include:: ../../includes_node/includes_node_type_physical.rst
   * - .. image:: ../../images/icon_node_virtual.png
     - .. include:: ../../includes_node/includes_node_type_virtual.rst
   * - .. image:: ../../images/icon_node_networking.png
     - .. include:: ../../includes_node/includes_node_type_network.rst

Some important components of nodes include:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Feature
     - Description
   * - .. image:: ../../images/icon_chef_client.png
     - .. include:: ../../includes_chef_client/includes_chef_client.rst
   * - .. image:: ../../images/icon_ohai.png
     - .. include:: ../../includes_ohai/includes_ohai.rst

The |chef client_title| Run
=====================================================
.. include:: ../../includes_chef_client/includes_chef_client_11-14_run.rst

|chef validator|
-----------------------------------------------------
.. include:: ../../includes_security/includes_security_chef_validator.rst

SSL Certificates
-----------------------------------------------------
.. include:: ../../includes_node/includes_node_certificate.rst

Signed Header Authentication
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_security/includes_security_signed_header_authentication.rst
