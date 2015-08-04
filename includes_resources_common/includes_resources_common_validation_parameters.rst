.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following parameters can be passed to the attribute keyword to validate a parameter that has been set on a resource in a recipe:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Parameter
     - Description
   * - ``:default``
     - Set the default value for a parameter.
   * - ``:kind_of``
     - Ensure that a value is a ``kind_of?(whatever)``. Pass this parameter as an array to ensure that a value is one of those types.
   * - ``:required``
     - Raise an exception if a parameter is missing. Valid values: ``true`` or ``false``. Default value: ``false``.
   * - ``:regex``
     - Match the value of a parameter against a regular expression.
   * - ``:equal_to``
     - Match the value of a parameter with ``==``. An array means it can be equal to any of the values.
   * - ``:name_attribute``
     - Specify the name of a resource. Valid value: ``true`` or ``false``.
   * - ``:callbacks``
     - Use a |hash| of |ruby proc|, which should return ``true`` if the argument is valid. The key will be inserted into the error message if the |ruby proc| does not return true: ``"Option #{key}'s value #{value} #{message}!"``.
   * - ``:respond_to``
     - Ensure that a value has a given method. Takes one method name or an array of method names.