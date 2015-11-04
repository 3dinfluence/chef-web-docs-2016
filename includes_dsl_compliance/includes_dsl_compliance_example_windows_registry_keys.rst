.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following test shows how to audit machines to ensure Safe DLL Seach Mode is enabled:

.. code-block:: ruby

   control 'windows-base-101' do
     impact 1.0
     title 'Safe DLL Search Mode is Enabled'
     desc '
       @link: https://msdn.microsoft.com/en-us/library/ms682586(v=vs.85).aspx
     '
     describe registry_key('HKLM\\System\\CurrentControlSet\\Control\\Session Manager') do
       it { should exist }
       it { should_not have_property_value('SafeDllSearchMode', :type_dword, '0') }
     end
   end
