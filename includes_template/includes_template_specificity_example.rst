.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A cookbook may have a ``/templates`` directory structure like this::

   templates/
     windows-6.2
     windows-6.1
     windows-6.0
     windows
     default

and a resource that looks something like the following:

.. code-block:: ruby

   template "C:\path\to\file\text_file.txt" do
     source "text_file.txt"
     mode '0755'
     owner 'root'
     group 'root'
   end

This resource would be matched in the same order as the ``/templates`` directory structure. For a node named "host-node-desktop" that is running |windows 7|, the second item would be the matching item and the location:

.. code-block:: ruby

   /templates
     windows-6.2/text_file.txt
     windows-6.1/text_file.txt
     windows-6.0/text_file.txt
     windows/text_file.txt
     default/text_file.txt


