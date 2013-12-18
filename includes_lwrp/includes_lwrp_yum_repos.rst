.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The following cookbooks are used in conjunction with the |cookbook yum| cookbook to manage repositories that are available to specific platforms and/or repositories. In some cases, such as |amazon linux|, |centos|, and |fedora|, the cookbooks contain additional repository-specific attributes that may be helpful, but are not required. In other cases, such as |elrepo|, |fedora epel|, |erlang solutions|, |redhat ius|, |percona|, |postgresql|, and |repoforge|, the cookbooks contain additional defaults that are not included in the |cookbook yum| cookbook and are required.

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Cookbook
     - Description
   * - `yum-amazon <https://github.com/opscode-cookbooks/yum-amazon>`_
     - Optional for |amazon linux| repositories. Use the |cookbook yum_amazon| cookbook to manage the following repositories: ``amzn-main``, ``amzn-main-debuginfo``, ``amzn-nosrc``, ``amzn-updates``, ``amzn-updates-debuginfo``, ``amzn-preview``, and ``amzn-preview-debuginfo``.
   * - `yum-centos <https://github.com/opscode-cookbooks/yum-centos>`_
     - Optional for |centos| repositories. Use the |cookbook yum_centos| cookbook to manage the following repositories: ``base``, ``updates``, ``extras``, ``centosplus``, and ``contrib``.
   * - `yum-elrepo <https://github.com/opscode-cookbooks/yum-elrepo>`_
     - Required for |elrepo| repositories. Use the |cookbook yum_elrepo| cookbook to manage the following repositories: ``elrepo``.
   * - `yum-epel <https://github.com/opscode-cookbooks/yum-epel>`_
     - Required for |fedora| |fedora epel| repositories. Use the |cookbook yum_epel| cookbook to manage the following repositories: ``epel``, ``epel-debuginfo``, ``epel-source``, ``epel-testing``, ``epel-testing-debuginfo``, and ``epel-testing-source``.
   * - `yum-erlang_solutions <https://github.com/opscode-cookbooks/yum-erlang_solutions>`_
     - Required for |erlang solutions| repositories. Use the |cookbook yum_erlang| cookbook to manage the following repositories: ``erlang_solutions``.
   * - `yum-fedora <https://github.com/opscode-cookbooks/yum-fedora>`_
     - Optional for |fedora| repositories. Use the |cookbook yum_fedora| cookbook to manage the following repositories: ``fedora``, ``fedora-debuginfo``, ``fedora-source``, ``updates``, ``updates-debuginfo``, ``updates-source``, ``updates-testing``, ``updates-testing-debuginfo``, and ``updates-testing-source``.
   * - `yum-ius <https://github.com/opscode-cookbooks/yum-ius>`_
     - Required for |redhat ius| repositories. Use the |cookbook yum_ius| cookbook to manage the following repositories:  ``ius``, ``ius-debuginfo``, ``ius-source``, ``ius-archive``, ``ius-archive-debuginfo``, ``ius-archive-source``, ``ius-testing``, ``ius-testing-debuginfo``, ``ius-testing-source``, ``ius-dev``, ``ius-dev-debuginfo``, ``ius-dev-source``.
   * - `yum-percona <https://github.com/opscode-cookbooks/yum-percona>`_
     - Required for |percona| repositories. Use the |cookbook yum_percona| cookbook to manage the following repositories: ``percona``.
   * - `yum-pgdg <https://github.com/opscode-cookbooks/yum-pgdg>`_
     - Required for |postgresql| repositories. Use the |cookbook yum_pgdg| cookbook to manage the following repositories: ``base``, ``updates``, ``extras``, ``centosplus``, and ``contrib``.
   * - `yum-repoforge <https://github.com/opscode-cookbooks/yum-repoforge>`_
     - Required for |repoforge| repositories. Use the |cookbook yum_repoforge| cookbook to manage the following repositories: ``rpmforge``, ``rpmforge-extras``, and ``rpmforge-testing``.

