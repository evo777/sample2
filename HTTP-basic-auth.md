# HTTP Basic Auth

## What is it?
- Method for the HTTP user agent (e.g., browser) to provide a username and password during an HTTP request
- Username and password sent in the `Authorization` header field
- To request basic authentication, the server will send a header that looks something like `WWW-Authenticate: Basic realm="myRealm"`

## Security of basic auth
- Offers no confidentiality as the username and password are sent as a base64 encoded string ('username:password') and are not encrypted or hashed (e.g., see how easy it is to compromise Basic Authentication using a tool like wireshark: https://www.youtube.com/watch?v=NvFJHSYC2j4)
- HTTPS is typically used in conjunction with basic auth to provide a better level of security
- Does not include any serverside methods to 'logout' the user