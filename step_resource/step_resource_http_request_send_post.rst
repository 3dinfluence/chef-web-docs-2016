.. This is an included how-to. 

To send a ``POST`` request as |json| data, convert the message to |json| and include the correct content-type header. For example:

.. code-block:: ruby

   http_request 'posting data' do
     action :post
     url 'http://example.com/check_in'
     message ({:some => 'data'}.to_json)
     headers({'AUTHORIZATION' => "Basic #{
       Base64.encode64('username:password')}",
       'Content-Type' => 'application/data'
     })
   end
