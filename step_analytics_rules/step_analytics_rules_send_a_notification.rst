.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Using the ``notify()`` function, notifications can be sent when a rule's conditions are met.

Once you've created a notification you'll use its name as the first argument given to the ``notify()`` function. For example, suppose you've created a notification with the name ``email-admins``:

.. image:: ../../images/analytics_email_notification_name.png

This notification could then be triggered by creating a rule that calls ``notify()``, e.g.:

.. code-block:: ruby

   notify("email-admins", "Your message here.")

The below rule would trigger this notification for every ``run_start`` message:

.. code-block:: ruby

   rule "Email notification" on run_start
   when
     true
   then
     notify("email-admins", "Run started on {{message.node_name}}")
   end
