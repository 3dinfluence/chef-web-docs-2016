=====================================================
Create the Organization
=====================================================

.. warning:: This documentation is about |chef private|, an older version of the |chef server|. For documentation about the current version of the |chef server|, see http://docs.opscode.com/server/.

In order to begin managing your infrastructure with |chef private|, you will need to create an organization. An organization is completely multi-tenant |chef| infrastructure that shares nothing with other organizations on your |chef private| server.

.. image:: ../../images_private_chef/private_chef_1x_click_to_create_org.png

Complete the form that contains the following fields:

* **Organization Full Name**: Should be the name of your company or department
* **Organization Short Name**: Should be a lowercase word describing the organization---used in the web UI and API URLs.

After the form is completed, click **Create Organization** to create your organization.

.. image:: ../../images_private_chef/private_chef_1x_create_org_button.png

After the organization is created:

* **Download the validation key:** This key will enable you to attach clients to this |chef private| organization
* **Generate a Knife configuration file:** |knife| is the command line API to |chef|, and this link will provide you with a pre-generated configuration for this organization, and customized for your |chef private| installation.

.. image:: ../../images_private_chef/private_chef_1x_download_key_and_knife.png



