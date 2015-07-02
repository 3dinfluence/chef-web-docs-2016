.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A |resource remote_file| resource block manages files by using files that exist remotely. For example, to write the home page for an |apache| website:

.. code-block:: ruby

   remote_file '/var/www/customers/public_html/index.php' do
     source 'http://somesite.com/index.php'
     owner 'web_admin'
     group 'web_admin'
     mode '0644'
     action :create
   end

where

* ``'/var/www/customers/public_html/index.php'`` is path to the file to be created
* ``'http://somesite.com/index.php'`` specifies the location of the remote file
* ``owner``, ``group``, and ``mode`` define the permissions

The full syntax for all of the attributes that are available to the |resource cookbook_file| resource is:

.. code-block:: ruby

   remote_file 'name' do
     backup                     FalseClass, Integer
     checksum                   String
     group                      String, Integer
     inherits                   TrueClass, FalseClass
     mode                       String, Integer
     owner                      String, Integer
     path                       String  # defaults to 'name' if not specified
     provider                   Chef::Provider::CookbookFile
     rights                     Hash
     source                     String, Array
     action                     Symbol # defaults to :create if not specified
   end

where 

* ``remote_file`` is the resource
* ``name`` is the name of the resource block
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``backup``, ``checksum``, ``group``, ``inherits``, ``mode``, ``owner``, ``path``, ``provider``, ``rights``, and ``source`` are attributes of this resource, with the |ruby| type shown. |see attributes|
