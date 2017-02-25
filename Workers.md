## What is it?
The JavaScript code you write usually executes in a single thread. In fact new threads can be executed in the background without interrupting the main thread, and effectively creating a multi-threaded architecture.  Web workers provide a simple way to have scripts running in the background without interfering the main user interface. Once created, a worker can communicated with the javascript that created it by sending messages to an event handler in the JavaScript code.

## How does it work in code?
### Spawning a dedicated worker
Call the Worker() constructor, specifying the URI of a script to execute in the worker thread (main.js):
```
var myWorker = new Worker("worker.js");
```

### Sending message to and from a dedicated worker
* postMessage()
When you want to send a message to the worker, you post messages to it like this (main.js):
```
first.onchange = function() {
  myWorker.postMessage([first.value,second.value]);
  console.log('Message posted to worker');
}

second.onchange = function() {
  myWorker.postMessage([first.value,second.value]);
  console.log('Message posted to worker');
}
```
* onmessage
In the worker, we can respond when the message is received by writing an event handler block like this (worker.js):
```
onmessage = function(e) {
  console.log('Message received from main script');
  var workerResult = 'Result: ' + (e.data[0] * e.data[1]);
  console.log('Posting message back to main script');
  postMessage(workerResult);
}
```
Back in the main thread, we use onmessage again, to respond to the message sent back from the worker:
```
myWorker.onmessage = function(e) {
  result.textContent = e.data;
  console.log('Message received from worker');
}
```

### Terminate a worker
```
myWorker.terminate();
```
In the worker thread, workers may close themselves by calling their own close method:
```
close();
```

## Use Cases

* image processing by using the data extracted from the <canvas> or the <video> elements. You can divide the image into several zones and push them to the different Workers that will work in parallel. You'll then benefit from the new generation of multi-cores CPUs. The more you have, the faster you'll go.

* big amount of data retrieved that you need to parse after an XMLHTTPRequest call. If the time needed to process this data is important, you'd better do it in background inside a Web Worker to avoid freezing the UI Thread. You'll then keep a reactive application.

* background text analysis: as we have potentially more CPU time available when using the Web Workers, we can now think about new scenarios in JavaScript. For instance, we could imagine parsing in real-time what the user is currently typing without impacting the UI experience. Think about an application like Word (of our Office Web Apps suite) leveraging such possibility: background search in dictionaries to help the user while typing, automatic correction, etc.

* concurrent requests against a local database. IndexDB will allow what the Local Storage can't offer us: a thread-safe storage environment for our Web Workers.

