RESTful protocol is to use nouns instead of verbs for HTTP methods. Some of the common REST methods are:

GET: retrieves a resource
-should not have any side effects, also known as idempotence. For example, data should never be modified on the server side as a result of a GET request
-instructs the server to transmit the data identified by the URL to the client

POST: creates a resource in a collection
-this is the only idempotent method

PUT: changes the state of a resource or updates it
-requests contain the data to use in updating or creating the resource in the body

DELETE: removes a resource
