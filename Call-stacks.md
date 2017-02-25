## What is it?
It's a data structure that records where we are in the program.  When a function is called in a program executes, it gets added to the stack. When a function returns, it gets popped off the call stack.

<a href="https://www.youtube.com/watch?v=8aGhZQkoFbQ" target="_blank"><img src="https://i.ytimg.com/vi/8aGhZQkoFbQ/hqdefault.jpg?custom=true&w=196&h=110&stc=true&jpg444=true&jpgq=90&sp=68&sigh=IwhmuaaKqzzsfs5F7B7pMUdYXx8" 
alt="IMAGE ALT TEXT HERE" width="240" /></a>

### Stack Trace
A stack trace (also called stack backtrace or stack traceback) is a report of the active stack frames at a certain point in time during the execution of a program.

### Blocking
If a function in the call stack is taking a long time to return, then the browser is stuck.  The solution is asynchronous callbacks.
