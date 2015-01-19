.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the ``control`` method to define a specific series of tests that comprise an individual audit. A ``control`` method MUST be contained within a ``control_group`` block. A ``control_group`` block may contain multiple ``control`` methods.

The syntax for the ``control`` method is as follows:

.. code-block:: ruby

   control_group "audit name" do
     control "name" do
       it "should do something" do
         expect(something).to/.to_not be_something
       end
     end
   end

where:

* ``control_group`` groups one (or more) ``control`` blocks
* ``control "name" do`` defines an individual audit
* Each ``control`` block must define at least one validation
* Each ``it`` statement defines a single validation. ``it`` statements are processed individually when the |chef client| is run in |chef client_audit|
* An ``expect(something).to/.to_not be_something`` is a statement that represents the individual test. In other words, this statement tests if something is expected to be (or not be) something. For example, a test that expects the |postgresql| pacakge to not be installed would be similar to ``expect(package("postgresql")).to_not be_installed`` and a test that ensures a service is enabled would be similar to ``expect(service("init")).to be_enabled``
* An ``it`` statement may contain multiple ``expect`` statements
