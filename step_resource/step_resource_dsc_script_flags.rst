.. This is an included how-to. 

If a |windows powershell_dsc_short| script contains configuration data that takes parameters, those parameters may be passed using the ``flags`` attribute. For example, the following |windows powershell| data file takes parameters for the ``EditorChoice`` and ``EditorFlags`` settings:

.. code-block:: javascript

   $choices = @{'emacs' = 'c:\emacs\bin\emacs';'vi' = 'c:\vim\vim.exe';'powershell' = 'powershell_ise.exe'}
     Configuration 'DefaultEditor' 
       {
         [CmdletBinding()]
         param
           (
             $EditorChoice,
             $EditorFlags = ''
           )
         Environment 'TextEditor'
         {
           Name = 'EDITOR'
           Value =  "$($choices[$EditorChoice]) $EditorFlags"
         }
       }

Use the following recipe to set those parameters:

.. code-block:: ruby

   dsc_script `DefaultEditor` do
     flags { :EditorChoice => 'emacs', :EditorFlags => '--maximized' }
     command 'c:\dsc_scripts\editors.ps1'
   end
