.. This is an included how-to. 

The following example shows how to specify custom configuration data using the ``configuration_name`` attribute. For example, the following |windows powershell| script defines the ``vi`` configuration:

.. code-block:: powershell

   Configuration 'emacs'  
     {
       Environment 'TextEditor'
       {
         Name = 'EDITOR'
         Value = 'c:\emacs\bin\emacs.exe'
       }
   }
   
   Configuration 'vi'   
   {
       Environment 'TextEditor'
       {
         Name = 'EDITOR'
         Value = 'c:\vim\bin\vim.exe'
       }
   }

Use the following recipe to specify that configuration:

.. code-block:: ruby

   dsc_script `EDITOR` do
     configuration_name 'vi'
     command 'c:\dsc_scripts\editors.ps1'
   end

