SQLite is a library that is embedded in the application. 

Advantages:

* Fast and efficient: integration uses direct calls to the database and does not require connecting via a port or socket

* Portable: the entire database consists of a single file on the disk (file-based), which makes reading/writing easy

* Follows standards: uses SQL and follows ANCI standards, omitting some features

* Feature-rich

Disadvantages:

* Does not have support for users (i.e. cannot vary accessibility to different users)

* Only allow one single write operation to happen at a given time

SQLite is good for test, development, or embedded applications that require portability but not expansion (single-user local apps, mobile apps, or games), but not for multi-user applications.