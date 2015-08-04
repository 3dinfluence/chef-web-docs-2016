.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |resource scm_git| resource block manages source control resources that exist in a |git| repository:

.. code-block:: ruby

   git '#{Chef::Config[:file_cache_path]}/app_name' do
     repository 'node[:app_name][:git_repository]'
     revision 'node[:app_name][:git_revision]'
     action :sync
   end

The full syntax for all of the properties that are available to the |resource scm_git| resource is:

.. code-block:: ruby

   git 'name' do
     additional_remotes         Hash
     checkout_branch            String
     depth                      Integer
     destination                String # defaults to 'name' if not specified
     enable_checkout            TrueClass, FalseClass
     enable_submodules          TrueClass, FalseClass
     environment                Hash
     group                      String, Integer
     notifies                   # see description
     provider                   Chef::Provider::Scm::Git
     reference                  String
     remote                     String
     repository                 String
     revision                   String
     ssh_wrapper                String
     subscribes                 # see description
     timeout                    Integer
     user                       String, Integer
     action                     Symbol # defaults to :sync if not specified
   end

where 

* ``git`` is the resource
* ``name`` is the name of the resource block and also (when the ``destination`` property is not specified) the location in which the source files will be placed and/or synchronized with the files under source control management
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``additional_remotes``, ``checkout_branch``, ``depth``, ``destination``, ``enable_checkout``, ``enable_submodules``, ``environment``, ``group``, ``provider``, ``reference``, ``remote``, ``repository``, ``revision``, ``ssh_wrapper``, ``timeout``, and ``user`` are properties of this resource, with the |ruby| type shown. |see attributes|
