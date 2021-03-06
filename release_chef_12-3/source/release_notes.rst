=====================================================
Release Notes: |chef client| 12.3
=====================================================

.. include:: ../../includes_chef/includes_chef.rst

What's New
=====================================================
The following items are new for |chef client| 12.3 and/or are changes from previous versions. The short version:

* **Socketless local mode with chef-zero** Port binding and HTTP requests on localhost may be disabled in favor of socketless mode.
* **Minimal Ohai plugins** Run only the plugins required for name resolution and resource/provider detection.
* **Dynamic resource and provider resolution** Four helper methods may be used in a library file to get resource and/or provider mapping details, and then set them per-resource or provider.
* **New clear_soruces attribute for the chef_gem and gem_package resources** |clear_sources|

Socketless Local Mode
-----------------------------------------------------
The |chef client| may disable port binding and HTTP requests on localhost by making a socketless request to |chef zero|. This may be done from the command line or with a configuration setting.

Use the following command-line option:

``--[no-]listen``
   |chef_zero_no_listen| Use ``--no-listen`` to disable port binding and HTTP requests on localhost.

Or add the following setting to the |client rb| file:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``listen``
     - |chef_zero_no_listen| Set to ``false`` to disable port binding and HTTP requests on localhost.

Minimal |ohai|
-----------------------------------------------------
The following option may be used with |chef client|, |chef solo|, and |chef apply| to speed up testing intervals:

``--minimal-ohai``
   |minimal_ohai|

This setting may be configured using the ``minimal_ohai`` setting in the |client rb| file.

Dynamic Resolution
-----------------------------------------------------
.. include:: ../../includes_libraries/includes_libraries_dynamic_resolution.rst


Changelog
=====================================================
https://github.com/chef/chef/blob/12.3-stable/CHANGELOG.md

