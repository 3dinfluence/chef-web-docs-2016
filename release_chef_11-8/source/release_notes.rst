=====================================================
Release Notes: |chef client| 11.8
=====================================================

.. include:: ../../includes_chef/includes_chef.rst


What's New
=====================================================
The following items are new for |chef 11-8| and/or are changes from previous versions. The short version:

* **Local mode for the chef-client** The |chef client| can now be run in local mode, which allows the |chef client| to run against the local |chef repo| as if it were running against a |chef server|.
* **New configuration settings** Three configuration settings have been added to support the use of local mode: ``chef_zero[:enabled]``, ``chef_zero[:port]``, and ``local_mode``.
* **New man pages for Knife** The man pages built into |knife|, |chef client|, |chef shell|, |chef solo|, and |ohai| are now synchronized with the same topics from docs.opscode.com and are current as of the |chef client| 11.8.0 release. 

|chef zero|
-----------------------------------------------------
.. include:: ../../includes_chef/includes_chef_zero.rst

|chef client| Local Mode
-----------------------------------------------------
The |chef client| can be run in local mode using the ``--local-mode`` option:

``-z``, ``--local-mode``
   |local_mode|

.. include:: ../../includes_chef_client/includes_chef_client_local_mode.rst


Knife Support for |chef zero|
-----------------------------------------------------
New common options have been added:

``--chef-zero-port PORT``
   |port chef_zero|

``-z``, ``--local-mode``
   |local_mode|


New Config Settings
-----------------------------------------------------
Three new settings are available for the |knife rb| and |client rb| configuration files:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``chef_zero[:enabled]``
     - |chef_zero_enabled| Default value: ``false``. For example:
       ::
 
          chef_zero[:enabled]true
   * - ``chef_zero[:port]``
     - |chef_zero_port| Default value: ``8889``. For example:
       ::
 
          chef_zero[:port] 8889
   * - ``local_mode``
     - |local_mode| For example:
       ::
 
          local_mode true
   * - ``verify_api_cert``
     - |ssl_verify_mode_verify_api_cert| Default value: ``false``.


New Man Pages
-----------------------------------------------------
The man pages built into |knife|, |chef client|, |chef shell|, |chef solo|, and |ohai| are now synchronized with the same topics from docs.opscode.com and are current as of the |chef client| 11.8.0 release. The man pages and online topics are published using the same process, which means that the information published to each format is identical. That said, the docs.opscode.com pages are updated more frequently than man pages will be; changes made to the topics on docs.opscode.com after this release will be included in future updates of the |chef client|.


|resource http_request| resource, |json| messages
-----------------------------------------------------
The approach for using the |resource http_request| resource to send a ``POST`` request that has a |json| message body has changed. Specifically, the ``message`` must be converted to |json| using ``to_json`` and the content-type header must be specified within the header.

For releases prior to |chef 11-8|, ``POST`` requests with a |json| message body looked like:

.. code-block:: ruby

   http_request "posting data" do
     action :post
     url "http://example.com/check_in"
     message :some => "data"
     headers({"AUTHORIZATION" => "Basic #{Base64.encode64("username:password")}"})
   end

And starting with |chef 11-8|, they should be like:

.. code-block:: ruby

   http_request "posting data" do
     action :post
     url "http://example.com/check_in"
     message ({:some => "data"}.to_json)
     headers({"AUTHORIZATION" => "Basic #{Base64.encode64("username:password")}","Content-Type" => "application/data"})
   end



What's Fixed
=====================================================

The following bugs were fixed:

* `CHEF-1559 <http://tickets.opscode.com/browse/CHEF-1559>`_  --- Debian service provider does not modify the priorities of service
* `CHEF-3159 <http://tickets.opscode.com/browse/CHEF-3159>`_  --- Do not silently exit when the daemon isn't executable in init scripts on Debian
* `CHEF-3798 <http://tickets.opscode.com/browse/CHEF-3798>`_  --- user provider on Windows tries to set the password even if not provided
* `CHEF-3881 <http://tickets.opscode.com/browse/CHEF-3881>`_  --- exit 1, not 0, if $DAEMON (chef-client) is not executable
* `CHEF-3982 <http://tickets.opscode.com/browse/CHEF-3982>`_  --- wget/curl dep in chef-full knife bootstrap script fails on Solaris 10
* `CHEF-4014 <http://tickets.opscode.com/browse/CHEF-4014>`_  --- Group provider does not respect group_name on Windows
* `CHEF-4084 <http://tickets.opscode.com/browse/CHEF-4084>`_  --- knife status -r adds incorrect punctuation
* `CHEF-4155 <http://tickets.opscode.com/browse/CHEF-4155>`_  --- remove the chef-apply symlink in postinst/postrm
* `CHEF-4196 <http://tickets.opscode.com/browse/CHEF-4196>`_  --- chef-shell & chef-apply aren't deleted by postinst & postrm scripts
* `CHEF-4197 <http://tickets.opscode.com/browse/CHEF-4197>`_  --- Chef::Provider::Mount device_mount_regex fails to populate capture groups when device is symlink (Ubuntu 12)
* `CHEF-4200 <http://tickets.opscode.com/browse/CHEF-4200>`_  --- When uid is sent into user provider as a string, chef should not update user on each chef run
* `CHEF-4271 <http://tickets.opscode.com/browse/CHEF-4271>`_  --- "--sudo-use-password" option for knife-bootstrap should escape passwords with ' ' to allow for special characters to be passed in via command line
* `CHEF-4335 <http://tickets.opscode.com/browse/CHEF-4335>`_  --- Knife ssh adds annoying extra newlines to output
* `CHEF-4344 <http://tickets.opscode.com/browse/CHEF-4344>`_  --- Fix typo in spec
* `CHEF-4353 <http://tickets.opscode.com/browse/CHEF-4353>`_  --- No way to assign validator property to client.
* `CHEF-4371 <http://tickets.opscode.com/browse/CHEF-4371>`_  --- FreeBSD Package Provider fails when package name contains +'s.
* `CHEF-4375 <http://tickets.opscode.com/browse/CHEF-4375>`_  --- chef-service-manager --version shows "version unknown"
* `CHEF-4394 <http://tickets.opscode.com/browse/CHEF-4394>`_  --- Add an equivalent for --fork on Windows
* `CHEF-4399 <http://tickets.opscode.com/browse/CHEF-4399>`_  --- Line endings for templates are based on the platform the template was written on not on the node platform
* `CHEF-4406 <http://tickets.opscode.com/browse/CHEF-4406>`_  --- response_file fails trying to load preseed templates and falls back to cookbook files.
* `CHEF-4411 <http://tickets.opscode.com/browse/CHEF-4411>`_  --- Fix --copyright and --email typos in knife cookbook create docs
* `CHEF-4422 <http://tickets.opscode.com/browse/CHEF-4422>`_  --- remote_file fails when source becomes too long
* `CHEF-4426 <http://tickets.opscode.com/browse/CHEF-4426>`_  --- knife cookbook upload doesn't work on windows when working with :versioned_cookbooks
* `CHEF-4435 <http://tickets.opscode.com/browse/CHEF-4435>`_  --- Chef::DataBag.save does a PUT getting a 405 from the chef server
* `CHEF-4456 <http://tickets.opscode.com/browse/CHEF-4456>`_  --- Knife cookbook site share fails with Ruby 2
* `CHEF-4457 <http://tickets.opscode.com/browse/CHEF-4457>`_  --- Diffs fail when there are spaces in the path
* `CHEF-4470 <http://tickets.opscode.com/browse/CHEF-4470>`_  --- Running chef-client fails when chef is running as a service on windows
* `CHEF-4482 <http://tickets.opscode.com/browse/CHEF-4482>`_  --- user resource allows defining uid as a string but results in re-applying the change with each run
* `CHEF-4493 <http://tickets.opscode.com/browse/CHEF-4493>`_  --- Merge unmerged knife-essentials code into chef
* `CHEF-4499 <http://tickets.opscode.com/browse/CHEF-4499>`_  --- knife upload subcommand does not support any options
* `CHEF-4507 <http://tickets.opscode.com/browse/CHEF-4507>`_  --- smartos package provider matches package names too loosely in candidate_version
* `CHEF-4509 <http://tickets.opscode.com/browse/CHEF-4509>`_  --- After CHEF-4011 - Double encryption problem
* `CHEF-4513 <http://tickets.opscode.com/browse/CHEF-4513>`_  --- HTTPS proxy not set (wget only) using HTTPS to download the Omnibus installer
* `CHEF-4515 <http://tickets.opscode.com/browse/CHEF-4515>`_  --- Wrong puzzling/confusing message "Unsupported `json_class` type 'Chef::WebUIUser' (JSON::ParserError)" while users upload
* `CHEF-4526 <http://tickets.opscode.com/browse/CHEF-4526>`_  --- knife environment edit still is .js temp files
* `CHEF-4534 <http://tickets.opscode.com/browse/CHEF-4534>`_  --- Upstart provider's restart_service if..else has a syntax bug
* `CHEF-4554 <http://tickets.opscode.com/browse/CHEF-4554>`_  --- Typo in chef solo config file option default
* `CHEF-4556 <http://tickets.opscode.com/browse/CHEF-4556>`_  --- chef-client service starts at every run of chef-client::service recipe
* `CHEF-4561 <http://tickets.opscode.com/browse/CHEF-4561>`_  --- :write is not a valid action for log resource
* `CHEF-4567 <http://tickets.opscode.com/browse/CHEF-4567>`_  --- SmartOSPackage class expands to the wrong DSL method
* `CHEF-4592 <http://tickets.opscode.com/browse/CHEF-4592>`_  --- "knife delete" subcommand options not showing on the command line
* `CHEF-4602 <http://tickets.opscode.com/browse/CHEF-4602>`_  --- Errno::ETXTBSY Text file busy
* `CHEF-4610 <http://tickets.opscode.com/browse/CHEF-4610>`_  --- Chef on Windows prints "deprecated" warning for every operation
* `CHEF-4614 <http://tickets.opscode.com/browse/CHEF-4614>`_  --- ResourceReporter should check that before/after state for a resource are hashes
* `CHEF-4615 <http://tickets.opscode.com/browse/CHEF-4615>`_  --- --chef-repo-path doesn't work for knife deps, download, etc
* `CHEF-4625 <http://tickets.opscode.com/browse/CHEF-4625>`_  --- Remote_file local file copy on Windows fails with EACCESS, requires atomic_update false workaround
* `CHEF-4649 <http://tickets.opscode.com/browse/CHEF-4649>`_  --- Auto configure ssl_ca_file on windows when running in omnibus
* `CHEF-4671 <http://tickets.opscode.com/browse/CHEF-4671>`_  --- Remote file cache control handling needs to be updated for HTTP library refactor
* `CHEF-4674 <http://tickets.opscode.com/browse/CHEF-4674>`_  --- 11.6.2 windows MSI does not include Erubis executable

What's Improved
=====================================================
The following improvements were made:

* `CHEF-3609 <http://tickets.opscode.com/browse/CHEF-3609>`_  --- when bootstrapping, should generate no_proxy in /etc/chef/client.rb if no_proxy is configured in knife.rb
* `CHEF-4248 <http://tickets.opscode.com/browse/CHEF-4248>`_  --- Expose timeout attribute on scm resource and associated providers
* `CHEF-4343 <http://tickets.opscode.com/browse/CHEF-4343>`_  --- Only test certain branches on Travis
* `CHEF-4458 <http://tickets.opscode.com/browse/CHEF-4458>`_  --- add chef_ca_cert resource
* `CHEF-4465 <http://tickets.opscode.com/browse/CHEF-4465>`_  --- mdadm provider shouldn't pass chunk size for mirrors
* `CHEF-4469 <http://tickets.opscode.com/browse/CHEF-4469>`_  --- Allow Solaris package install from Jumpstart install server's NFS share of packages
* `CHEF-4471 <http://tickets.opscode.com/browse/CHEF-4471>`_  --- Add Windows 8.1/2012 R2 to Chef Windows Helper
* `CHEF-4477 <http://tickets.opscode.com/browse/CHEF-4477>`_  --- fix typographical errors in autogenerated README.md
* `CHEF-4488 <http://tickets.opscode.com/browse/CHEF-4488>`_  --- Support chef_server_url 'local' running chef-zero
* `CHEF-4497 <http://tickets.opscode.com/browse/CHEF-4497>`_  --- tag method should be moved into the Node object
* `CHEF-4529 <http://tickets.opscode.com/browse/CHEF-4529>`_  --- A Timestamp of backup_filename is too short.
* `CHEF-4568 <http://tickets.opscode.com/browse/CHEF-4568>`_  --- Normalize whitespace
* `CHEF-4571 <http://tickets.opscode.com/browse/CHEF-4571>`_  --- GET '/cookbooks/foo/_latest' returns duplicate JSON keys in recipes
* `CHEF-4578 <http://tickets.opscode.com/browse/CHEF-4578>`_  --- groupadd add non_unique support (-o)
* `CHEF-4585 <http://tickets.opscode.com/browse/CHEF-4585>`_  --- chef/mixin/shell_out should require mixlib/shellout and document why it requires chef/shell_out
* `CHEF-4603 <http://tickets.opscode.com/browse/CHEF-4603>`_  --- Refactor Chef::REST so behavior is swappable
* `CHEF-4648 <http://tickets.opscode.com/browse/CHEF-4648>`_  --- Add Pry as a runtime dep

New Features
=====================================================
The following features were added:

* `CHEF-2928 <http://tickets.opscode.com/browse/CHEF-2928>`_  --- Chef solo's role_path should allow for an array of paths
