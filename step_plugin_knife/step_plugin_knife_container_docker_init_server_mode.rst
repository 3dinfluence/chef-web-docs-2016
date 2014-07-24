.. This is an included how-to.


.. To initialize a |dockerfile| context in server-mode for an image named "example/apache2" that has a ``run_list`` of ``recipe[apache2]``:

.. code-block:: bash

   $ knife container docker init example/apache2 -r 'recipe[apache2]'

will create a directory named ``example`` with a subdirectory named ``demo`` in the ``Chef::Config[:knife][:dockerfiles_path]`` path. In the ``example`` directory, a subdirectory named ``chef`` is created, which contains all of the files and folders that are necessary for the |chef client| to run successfully inside a container.
