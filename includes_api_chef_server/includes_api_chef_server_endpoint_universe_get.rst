.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to retrieve the universe data.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /universe

**Response**

The response will return an embedded hash, with the name of each cookbook as a top-level key. Each cookbook will list each version, along with its location information and dependencies:

.. code-block:: javascript

   {
     "ffmpeg": {
       "0.1.0": {
         "location_path": "http://supermarket.chef.io/api/v1/cookbooks/ffmpeg/0.1.0/download"
         "location_type": "supermarket",
         "dependencies": {
           "git": ">= 0.0.0",
           "build-essential": ">= 0.0.0",
           "libvpx": "~> 0.1.1",
           "x264": "~> 0.1.1"
         },
       },
       "0.1.1": {
         "location_path": "http://supermarket.chef.io/api/v1/cookbooks/ffmpeg/0.1.1/download"
         "location_type": "supermarket",
         "dependencies": {
           "git": ">= 0.0.0",
           "build-essential": ">= 0.0.0",
           "libvpx": "~> 0.1.1",
           "x264": "~> 0.1.1"
         },
       },
      "pssh": {
       "0.1.0": {
         "location_path": "http://supermarket.chef.io/api/v1/cookbooks/pssh.1.0/download"
         "location_type": "supermarket",
         "dependencies": {},
       }
     }
   }

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok| One (or more) cookbooks and associated cookbook version information was returned.
