.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|ohai| hints are used to tell |ohai| something about the system that it is running on that it would not be able to discover itself. An |ohai| hint exists if a |json| file exists in the hint directory with the same name as the hint. For example, calling ``hint?('antartica')`` in an |ohai| plugin would return an empty hash if the file ``antartica.json`` existed in the hints directory, and return nil if the file does not exist.

If the hint file contains |json| content, it will be returned as a hash from the call to ``hint?``.

.. code-block:: javascript

   {
     "snow": true,
     "penguins": "many"
   }

.. code-block:: ruby

   arctic_hint = hint?('antartica')
   if arctic_hint['snow']
     "There are #{arctic_hint['penguins']} penguins here." 
   else
     "There is no snow here, and penguins like snow."
   end

The default directory in which hint files are located is ``/etc/chef/ohai/hints/``. Use the ``Ohai::Config[:hints_path]`` setting in the |client rb| file to customize this location.
