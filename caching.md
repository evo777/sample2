### What is caching?
Caching is a technique to shorten the time to access data, where a copy of the original source of truth is duplicated.  

## Locations where caching can be done in memory or disc on the following systems
* database machine
* server machine
* client browser

## Populating cache?
* Upfront population: It is decided before hand what data should be cached.
* Lazy population: Data is cached only when requested
* Combination of Upfront and Lazy

## How to keep data in sync?
* write through: when the data can only be updated via the computer keeping the cache.
* Time Based Expiry: cached data is removed when the data is expired, and a fresh set is read and cached again when the data is needed.
* Active Expiry: when data changes on the remote system, it will inform the system that keeps the cache and update.

## Manage size of cache
In order to manage the size of cache on local system, to make space for new data. There are a few standard cache eviction techniques. These are 
* Time based eviction.
* First in, first out (FIFO).
* First in, last out (FILO).
* Least accessed.
* Least time between access.

