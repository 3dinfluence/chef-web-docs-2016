.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef (the executable).
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``chef push`` subcommand is used to upload an existing ``Policyfile.lock.json`` file to the |chef server|, along with all of the cookbooks that are contained in the policy lock. The policy lock will be applied to the specified policy group, which is a set of nodes that share the same run-list and cookbooks. 

.. warning:: This feature is new and experimental. Some aspects of the design have not yet been finalized. If you are new to |chef|, please don't use it. If you are an experienced user, please try it out and provide feedback. If you do use it, please do so in a location that is isolated from production code.

For more information about policy and the configuration file used to manage and maintain policy---policyfile.rb---please see this topic on Github: https://gist.github.com/danielsdeleo/52c90c9e3c9c76b80316.


