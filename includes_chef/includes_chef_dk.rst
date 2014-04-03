.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The |chef dk| defines a common workflow for cookbook development:

#. Create a skeleton cookbook. This is a cookbook with the standard files already included. The package manager is often |berkshelf| (included as part of the |chef dk|) and the revision control system is typically |git|. |berkshelf| helps manage cookbooks and cookbook dependencies.

#. Create a virtual machine environment. This is the environment that will be used to develop the cookbook, including the location in which automated testing and debugging of that cookbook will be done as it is being developed.

#. Write the recipes for the cookbook and debug those recipes as they are being written. This is typically an iterative process, where cookbook are tested as they are developed, bugs are fixed quickly, and then cookbooks are tested again. A text editor---|sublime|, |vim|, TextMate, EditPad, or any other preferred text editor---is used to author the files in the cookbook. 

#. Perform acceptance tests. These tests are not done in a development environment, but rather are done against a full |chef server| using an environment that matches the production environment as closely as possible.

#. When the cookbooks pass all the acceptance tests and have been verified to work in the desired manner, deploy the cookbooks to the production environment.
