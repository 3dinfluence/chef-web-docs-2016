.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the ``audit_policy`` |inspec resource| to test auditing policies on the |windows| platform. An auditing policy is a category of security-related events to be audited. Auditing is disabled by default and may be enabled for categories like account management, logon events, policy changes, process tracking, privilege use, system events, or object access. For each auditing category property that is enabled, the auditing level may be set to ``No Auditing``, ``Not Specified``, ``Success``, ``Success and Failure``, or ``Failure``.
