.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

In the event that the |windows ad| or |ldap| server goes down or becomes unreachable it is still possible for a user to log into the |chef server| as long as they have a system recovery password set on their |chef server| account.

Once a user has a system recovery password, they can log into the system by clicking the System Recovery link found on the right hand side of the login page. Once on the System Recovery page, the user will be asked to enter their username and system recovery password.

Once the user successfully logs in, they will gain access to the system and see the same screens as if |windows ad| or |ldap| were functioning.

If a user does not have a system recovery password enabled for their account (even if they have a system recovery password set) they will be redirected to the login page and a message will be shown stating that they do not have System Recovery enabled and to contact the system administrator.