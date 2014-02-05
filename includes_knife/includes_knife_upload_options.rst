.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Knife.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


This subcommand has the following options:

``--chef-repo-path PATH``
   |path chef_repo| This setting will override the default path to the |chef repo|. Default: same value as specified by ``chef_repo_path`` in |client rb|.

``--concurrency``
   |concurrency| Default: ``10``.

``--[no-]diff``
   |diff_upload| Set to ``false`` to upload all files. Default: ``true``.

``--[no-]force``
   |force knife upload| Default: ``--no-force``.

``--[no-]freeze``
   |freeze| Default: ``false``.

``-n``, ``--dry-run``
   |dry_run| Default: ``false``.

``--[no-]purge``
   |purge knife upload| Default: ``--no-purge``.

``--[no-]recurse``
   |no_recurse_upload| Default: ``--recurse``.

``--repo-mode MODE``
   |repo_mode| Default: ``everything`` / ``hosted_everything``.