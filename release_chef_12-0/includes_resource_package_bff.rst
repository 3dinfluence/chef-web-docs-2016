.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the |resource package_bff| resource to manage packages for the |ibm aix| platform using the |ibm installp| utility. When a package is installed from a local file, it must be added to the node using the |resource remote_file| or |resource cookbook_file| resources.

.. note:: A |ibm aix_bff| package may not have a ``.bff`` file extension. The |chef client| will still identify the correct provider to use based on the platform, regardless of the file extension.