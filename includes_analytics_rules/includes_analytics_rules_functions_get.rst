.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Use ``get()`` to identify a field, and then identify an associated value.

The syntax for this function:

.. code-block:: ruby

   get(variableToGet, valueToSet OR defaultIfMissing)

where:

* ``variableToGet`` specifies the field to look for
* ``valueToSet`` specifies the value to use
* ``defaultIfMissing`` specifies to use the default value if there is no user-defined value

For example:

.. code-block:: ruby

   rule on action when
     get(foo, false) = false
   then
     notify('some_alias')
   end

will pass if ``foo`` is missing in the |json| object.
