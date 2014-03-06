.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A more detailed example:

* A cookbook named ``cumbria`` that is used to build a website
* A file named index.html, which is the root page for the website
* Directories named ``/cities``, ``/places``, and ``/football``, which contains pages about cities, places, and football teams
* A directory named ``/images`` which contains images

These files are placed in the ``/files/default`` directory in the ``cumbria`` cookbook, like this:

.. code-block:: text

   cumbria
     /files
       /default
         index.html
         /cities
           carisle.html
           kendal.html
           penrith.html
           windermere.html
         /football
           carisle_united.html
         /images
           furness_abbey.png
           hadrians_wall.png
         /places
           furness_abbey.html
           hadrians_wall.html

The |resource remote_directory| resource can be used to build a website using these files. This website is being run on an |apache| web server. The resource would be similar to the following:

.. code-block:: ruby

   remote_directory "/var/www/html" do
     files_mode "0440"
     files_owner "yan"
     mode "0770"
     owner "hamilton"
     source "" # does this need a value? what if this is not specified?
   end

When the |chef client| runs, the |resource remote_directory| resource will tell the |chef client| to copy the directory tree from the cookbook to the file system using the structure defined in cookbook:

.. code-block:: text

   /var
     /www
       /html
         index.html
         /cities
           carisle.html
           kendal.html
           penrith.html
           windermere.html
         /football
           carisle_united.html
         /images
           furness_abbey.png
           hadrians_wall.png
         /places
           furness_abbey.html
           hadrians_wall.html

The |chef client| will manage the permissions of the entire directory structure below ``/html``, for a total of 10 files and 4 directories. For example:

.. code-block:: bash

   dr-xr-xr-x 2 root     root 4096 /var/www/html
   dr--r----- 1 yan      root 4096 /var/www/html/index.html
   drwxrwx--- 2 hamilton root 4096 /var/www/html/cities
   dr--r----- 1 yan      root 4096 /var/www/html/cities/carlisle.html
   dr--r----- 1 yan      root 4096 /var/www/html/cities/kendal.html
   dr--r----- 1 yan      root 4096 /var/www/html/cities/penrith.html
   dr--r----- 1 yan      root 4096 /var/www/html/cities/windermere.html
   drwxrwx--- 2 hamilton root 4096 /var/www/html/football
   dr--r----- 1 yan      root 4096 /var/www/html/football/carlisle_united.html
   drwxrwx--- 2 hamilton root 4096 /var/www/html/images
   dr--r----- 1 yan      root 4096 /var/www/html/images/furness_abbey/png
   dr--r----- 1 yan      root 4096 /var/www/html/images/hadrians_wall.png
   drwxrwx--- 2 hamilton root 4096 /var/www/html/places
   dr--r----- 1 yan      root 4096 /var/www/html/places/furness_abbey.html
   dr--r----- 1 yan      root 4096 /var/www/html/places/hadrians_wall.html

