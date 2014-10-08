.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef (the executable).
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``chef install`` subcommand is used to evaluate a policy file and find a compatible set of cookbooks, build a run-list, cache it locally, and then emit a ``Policyfile.lock.json`` that describes the locked policy set. The ``Policyfile.lock.json`` may be used to install the locked policy set to other machines and may be pushed to a policy group on the |chef server| to apply that policy to a group of nodes that are under management by |chef|.

.. warning:: This feature is new and expiremental. Some aspects of the design have not yet been finalized. If you are new to |chef|, please don't use it. If you are an experienced user, please try it out and provide feedback. If you do use it, please do so in a location that is isolated from production code.

For more information about policy and the configuration file used to manage and maintain policy---policyfile.rb---please see this topic on Github: https://gist.github.com/danielsdeleo/52c90c9e3c9c76b80316.

