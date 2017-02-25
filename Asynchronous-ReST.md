# Asynchronous ReST

## What is it?
- ReST calls that require an asynchronous operation.
- Some asynchronous operations are quick and can be responded to right away. Other operations may take significantly longer (e.g., minutes) and cannot be completed before the `HTTP` request times out. In these situations, the server will respond, letting the client know that the operations has started.
- For example, if the client makes a `GET` request that takes 20-30min of processing on the serverside, the server won't be able to respond with the resource immediately.

## How it works?
- Client makes a `GET` request: `GET /api/someCrazyLongAnalysis`
- Server responds to request with `202 Accepted` and a location where the client can check for completion:
```javascript
{
  location: '/api/analysisQueue/12345'
}
```
- Client checks the status of the request: `GET /api/analysisQueue/12345`
- Server responds with `200 OK` and a status object
```javascript
{
  status: 'Pending', // Status
  etaMins: 10, // Estimated minutes to completion
}
```
- Client checks the status after 10 minutes: `GET /api/analysisQueue/12345`
- Server responds with `303 See other` and details on the location of the resource
```javascript
{
  location: /api/completedAnalyses/12345
}
```
- Client retrieves the resource with `GET /api/completedAnalyses/12345`

## Additional Resources
https://www.adayinthelifeof.nl/2011/06/02/asynchronous-operations-in-rest/
http://farazdagi.com/blog/2014/rest-long-running-jobs/