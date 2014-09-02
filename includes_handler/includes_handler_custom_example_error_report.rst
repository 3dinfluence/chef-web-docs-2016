.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The `error_report <https://github.com/opscode/chef/blob/master/lib/chef/handler/error_report.rb>`_ handler is built into the |chef client| and can be used for both exceptions and reports. It serializes error report data to a |json| file. This handler may be enabled in one of the following ways.

By adding the following lines of |ruby| code to either the |client rb| file or the |solo rb| file, depending on how the |chef client| is being run:

.. code-block:: ruby

   require 'chef/handler/error_report'
   report_handlers << Chef::Handler::ErrorReport.new(:path => "/var/chef/reports")
   exception_handlers << Chef::Handler::ErrorReport.new(:path => "/var/chef/reports")

By using the :doc:`chef_handler </resource_chef_handler>` resource in a recipe, similar to the following:

.. code-block:: ruby

   chef_handler "Chef::Handler::ErrorReport" do
     source "chef/handler/error_report"
     arguments :path => '/var/chef/reports'
     action :enable
   end