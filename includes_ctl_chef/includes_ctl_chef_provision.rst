.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for chef (the executable).
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The |subcommand chef provision| subcommand is used to invoke an embedded |chef client| run to provision machines using |chef provisioning|. By default, this subcommand expects to find a cookbook named ``provision`` in the current working directory. The |chef client| run will run a recipe in this cookbook that uses |chef provisioning| to create one (or more) machines.

The |subcommand chef provision| subcommand is intended to:

* Provide a provisioning mechamism that supports using |policyfile rb| files
* Supporting naming conventions within |chef provisioning|
* Integreate |chef provisioning| steps with the command-line tools that are packaged with the |chef dk|
* Separate the configuration of provisioned machines from running |chef provisioning|
* Allow provisioing to be managed as code and versioned (via |policyfile rb| files), as opposed to the legacy |subcommand knife bootstrap| behavior, which is primarily driven by command-line options
