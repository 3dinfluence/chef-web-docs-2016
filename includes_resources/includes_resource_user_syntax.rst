.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource user| resource in a recipe is as follows:

.. code-block:: ruby

   user "name" do
     attribute "value" # see attributes section below
     ...
     action :action # see actions section below
   end

where 

* ``user`` tells the |chef client| to use one of the following providers during the |chef client| run: ``Chef::Provider::User::Useradd``, ``Chef::Provider::User::Pw``, ``Chef::Provider::User::Dscl``, or ``Chef::Provider::User::Windows``. The provider that is used by the |chef client| depends on the platform of the machine on which the |chef client| run is taking place
* ``name`` is the name of the resource block; when the ``username`` attribute is not specified as part of a recipe, ``name`` is also the name of the user
* ``attribute`` is zero (or more) of the attributes that are available for this resource
* ``:action`` identifies which steps the |chef client| will take to bring the node into the desired state
