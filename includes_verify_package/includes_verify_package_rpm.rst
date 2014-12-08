.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |company_name| package built for |rpm| can be verified using the key located at http://downloads.chef.io/chef.gpg.key.

To verify any |company_name| package built for RPM:

#. Import the key

   .. code-block:: bash
      
      $ rpm --import http://downloads.chef.io/chef.gpg.key

#. Verify the signature. For example, the |chef dk|:

   .. code-block:: bash
      
      $ rpm -K chefdk-0.2.2-1.x86_64.rpm
   
   which will return something similar to:
   
   .. code-block:: bash
      
      $ chefdk-0.2.2-1.x86_64.rpm: (sha1) dsa sha1 md5 gpg OK
