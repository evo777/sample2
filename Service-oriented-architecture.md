## What is SOA?

* SOA is an architectural pattern in computer software design (contrast with monolithic and microservices)
* Components provide services to other components via a communications protocol (REST), typically over a network.
* Compare to microservices: complex applications that are composed of small, independent processes communicating with each other using language-agnostic APIs

A smart guy said this

> “Microservices are the kind of SOA we have been talking about for the last decade. Microservices must be independently deployable, whereas SOA services are often implemented in deployment monoliths. Classic SOA is more platform driven, so microservices offer more choices in all dimensions.”- Torsten Winterberg


## Benefits of SOA

* Decoupled services allow for large teams to be working on different parts of the app with minimal interference
* Flexibility - you can write components in whatever language/platform suits you
* Test and debugging - you can test individually rather than making your way through a monolithic call stack
* Scalability - Easier to scale since you can choose which to throw more machines at
* Reusability - Goes without saying that this helps optimize developer time

## Cautionary tales

* Increases complexity across the stack for management since services must communicate together to perform tasks
* High investment cost and overhead
