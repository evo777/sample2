## PROS
* Easy to get started: Doesn't need extensive set-up. Uses HTML to build the site.
* Built-in $HTTP service: Doesn't require external frameworks (Request/jQuery) to do AJAX calls
* Dependency Injection: Dynamically injects module dependencies into the function call by doing back-end parsing of parameter names 
* Manages state with use of Directives.
* Easy Testability: One of the primary goals of AngularJS development was to ease test-driven development

## CONS
* Two-way-data-binding: Hard to track what is changing the state.
* Dynamic Scoping: Nested scopes can alter the same model, but changing one, isn't the same as changing the * other.
  * try for yourself: http://jsfiddle.net/1op3L9yo/
* Parameter Name Based Dependency Injection: Minifying code breaks it.
* Digest Loop: Angular looks through everything looking for changes, updates, and keeps searching/updating until there are no more changes. VERY expensive. Literally puts a hard limit on the size of the UI while remaining performant.

## Usage
* Directives: Extended HTML attributes with the prefix ng- . The ng-app directive initializes an AngularJS application. The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.
* Factory: Create an object, add properties to it, then return that same object. When you pass this service into your controller, those properties on the object will now be available in that controller through your factory.
* Service: Instantiated with the ‘new’ keyword. Because of that, you’ll add properties to ‘this’ and the service will return ‘this’. When you pass the service into your controller, those properties on ‘this’ will now be available on that controller through your service.
* Providers: The only service you can pass into your .config() function. Use a provider when you want to provide module-wide configuration for your service object before making it available.


## Misconceptions
* React is _always_ faster than Angular: FALSE.
  * Source: http://blog.500tech.com/is-reactjs-fast/

## Sources
* http://tylermcginnis.com/angularjs-factory-vs-service-vs-provider/
* http://www.wintellect.com/devcenter/jlikness/10-reasons-web-developers-should-learn-angularjs
* https://medium.com/@mnemon1ck/why-you-should-not-use-angularjs-1df5ddf6fc99#.6n76dq0dt
* https://www.backand.com/the-pros-of-angularjs/
* Angular Docs