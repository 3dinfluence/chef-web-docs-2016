.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A |resource http_request| resource block sends HTTP requests with an arbitrary message. For example, send a ``DELETE`` request to "http://www.chef.io/some_page?message=please_delete_me".

.. code-block:: ruby

   http_request 'please_delete_me' do
     url 'http://www.chef.io/some_page'
     action :delete
   end

The full syntax for all of the attributes that are available to the |resource http_request| resource is:

.. code-block:: ruby

   http_request 'name' do
     headers                    Hash
     message                    Object # defaults to 'name' if not specified
     notifies                   # see description
     provider                   Chef::Provider::HttpRequest
     url                        String
     action                     Symbol # defaults to :get if not specified
   end

where 

* ``http_request`` is the resource
* ``name`` is the name of the resource block
* ``:action`` identifies the steps the |chef client| will take to bring the node into the desired state
* ``headers``, ``message``, ``provider``, and ``url`` are attributes of this resource, with the |ruby| type shown. |see attributes|
