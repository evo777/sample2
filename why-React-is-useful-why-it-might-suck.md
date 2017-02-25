## Pros
* supports [[ES6]] syntax
* virtual [DOM](What is the DOM) quickly and automatically re-renders relevant components when underlying data changes
* one-way data flow between components (via props) makes behavior more predictable and debugging easier
* components can be composed together and nested, making them highly reusable and adaptable 
* components can be stateless or stateful, when necessary
* components are written in [[JSX]], which is semantic, easy to visualize, and very similar to HTML & JS
* mental model is easy to grasp/diagram, compared to other libraries and frameworks which rely more heavily on events


## Cons
* initial setup can be difficult and time consuming
* must be transpiled for use with non-ES6 interpreters
* there is no global state by default, making state difficult to manage when components are nested several layers deep
* is a library, rather than a fully-featured framework (must be paired with other libraries for many features such as state management)
* often paired with global state containers such as [[Redux]], which have a steeper learning curve
* Virtual DOM paradigm can be confusing and lead to bugs if developers are unfamiliar (eg. jQuery and standard DOM manipulation approaches will not work on the virtual DOM)
* There is a steep learning curve for front-end developers who are unfamiliar with Javascript/JSX

## See also
* [[React Native]]
* [[JSX]]
* [[Babel]]
* [[Redux]]
* [[Webpack]]