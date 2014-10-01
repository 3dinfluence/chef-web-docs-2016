.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource link| resource in a recipe is as follows:

.. code-block:: ruby

   link "name" do
     attribute "value" # see attributes section below
     ...
     action :action # see actions section below
   end

where 

* ``link`` tells the |chef client| to use the ``Chef::Provider::Link`` provider during the |chef client| run
* ``name`` is the name of the resource block; when the ``target_file`` attribute is not specified as part of a recipe, ``name`` is also name of the link
* ``attribute`` is zero (or more) of the attributes that are available for this resource
* ``:action`` identifies which steps the |chef client| will take to bring the node into the desired state
