## What is HTTP?

HTTP is the foundation for app-level communication across the network.

When a client makes an HTTP request to a server, a TCP/IP* connection is established between the client and server. This TCP/IP connection can be thought of as the tube through which messages are transmitted. HTTP requests and responses are those "messages."

*Note: While HTTP is almost always used with the TCP/IP protocol, it can be adapted for use with other protocols such as UDP.

## Request
* Contains a method (GET, PUT, POST, DELETE, OPTIONS, etc.)
* Contains a URL of the host it is trying to connect to
* Contains headers
* Optionally contains a body, e.g. on POST requests

## Response
* Contains a status code
* Contains headers
* Optionally contains a body