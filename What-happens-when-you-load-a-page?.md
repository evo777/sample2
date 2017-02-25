Let's say you type google.com into the browser.

### 30-second answer
1. Check cache.
1. Perform DNS lookup.
1. Open TCP/IP connection to send and receive HTTP request/response.
1. Handle response.

### Slightly more detail
1. Browser checks its cache to see if it already has a non-expired cache of the page. If yes, it simply renders that.
1. If not, browser asks a DNS (Domain Name Server) to resolve the hostname into an IP address.
1. Once resolved, browser opens a TCP/IP connection to the server.
1. Browser sends HTTP request through the TCP/IP connection.
1. Browser receives response via the same connection.
1. If cacheable, browser caches response.
1. Browser checks status code of response to figure out how to handle it. For example:
  * 2xx: Browser will render page or open dialog to download file.
  * 3xx: Browser will redirect or perform other conditional logic.
  * 401: Browser will pop up a dialog to authorize the request.
  * 4xx, 5xx: Browser will indicate error.
  * etc.

##### Source
http://stackoverflow.com/questions/2092527/what-happens-when-you-type-in-a-url-in-browser