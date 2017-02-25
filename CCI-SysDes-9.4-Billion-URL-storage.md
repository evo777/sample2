## Prompt

You have 10 billion URLs. How do you detect the duplicate documents?

Duplicate means that the URLs are identical

## Constraints

* Optimize for availability and speed

## Storing 1 URL 

* Datatype is a string, consisting of around 200 char
* Use a really big key-value store! (A giant hash table)
* Run string through hashing function of your choice (SHA-256 or MD5)

## Scaling volume of URLs

* Client hits server with key-value map that informs request which machine to visit
* Sharding - Split up data across multiple Redis instances
* Clustering - replicate data for each shard. complexity is introduced when talking about how the shard and its replica remain in sync

## Writing

* Use a write buffer with a commit log (memtable) in case machines fail.

## Increase read speed

* Use a Bloom filter to hash the URL. A negative result means that the URL is unique and you start writing almost immediately (without having to wait for the lookup to fail)