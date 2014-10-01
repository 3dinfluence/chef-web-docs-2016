.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource mount| resource in a recipe is as follows:

.. code-block:: ruby

   mount "name" do
     attribute "value" # see attributes section below
     ...
     fstype "type"
     action :action # see actions section below
   end

where 

* ``mount`` tells the |chef client| to use the ``Chef::Provider::Mount`` provider during the |chef client| run for all platforms except for |windows|, which uses the ``Chef::Provider::Mount::Windows`` provider 
* ``name`` is the name of the resource block; when the ``mount_point`` attribute is not specified as part of a recipe, ``name`` is also the directory (or path) in which a device should be mounted
* ``attribute`` is zero (or more) of the attributes that are available for this resource
* ``fstype`` is the file system type; this attribute is required
* ``:action`` is the step that the resource will ask the provider to take during the |chef client| run

For example:

.. code-block:: ruby

   mount node['mysql']['ec2_path'] do
     device ebs_vol_dev
     fstype "xfs"
     action :mount
   end
