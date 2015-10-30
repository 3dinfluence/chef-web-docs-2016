.. This is an included how-to. 

.. To test if a rule contains a matching element that is identified by a regular expression:

.. code-block:: ruby

   describe audit_daemon_rules do
     its("LIST_RULES") {
       should contain_match(/^exit,always arch=.*
       key=time-change
       syscall=adjtimex,settimeofday/)
     }
   end
