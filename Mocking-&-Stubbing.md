Stubs and mocks are two means through which we can introduce stand ins for real code.
They are both generally used to limit contact with other external systems, things outside of our control that are often non-deterministic or carry side effects [network requests, database access, file access].

Stubs and mocks differ in a few particular ways:

# Stubs
* contain no logic, returns only what you tell it to return
* are useful for getting code under test into a certain state
* carry no expectations/assertions about the way it should be called
* represent an implementation that code under test interacts with; The behavior being tested is your code not the stub

# Mocks
* test interactions between objects
* carry expectations/assertions about the way it should be called
* should be used sparingly as overuse of mocks can obscure purpose of tests and lead to code duplicatio 

