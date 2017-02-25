#Prototypes

##What are they?

Prototypes are objects that are delegated to in the case of a failed property lookup.

All types in javascript have a built-in prototype object (e.g., string prototype, number prototype, object prototype, array prototype, etc.).

Arrays and functions also delegate to the object prototype. However, in most cases, the array and function prototypes mask this relationship.

New prototype relationships can be created via the `Object.create` method. For example, this is used in the prototypal instantiation patterns as well as in pseudoclassical subclasses.

##Primitives and prototypes

When accessing a property on a primitive (E.g., `1.toString()` or `'abc'.length`) the JavaScript interpreter will temporarily coerce the primitive value into an object, which then delegates to its prototype (E.g., number prototype of string prototype).