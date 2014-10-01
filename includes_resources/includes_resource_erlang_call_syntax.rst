.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource erlang_call| resource in a recipe is as follows:

.. code-block:: ruby

   erl_call "name" do
     attribute "value" # see attributes section below
     ...
     action :action # see actions section below
   end

where 

* ``erl_call`` tells the |chef client| to use the ``Chef::Provider::ErlCall`` provider during the |chef client| run
* ``"name"`` is the name of the call
* ``attribute`` is zero (or more) of the attributes that are available for this resource
* ``:action`` identifies which steps the |chef client| will take to bring the node into the desired state
