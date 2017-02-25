# NoSQL Databases

## What is it?
NoSQL databases (aka non-SQL or non-relational or not-only-SQL) are a method of storing/retrieving data that do not rely on the tabular/relational methods used by traditional SQL databases.

The key characteristics of NoSQL databases are:

* **Schemaless**: NoSQL databases generally do not have a predefined schema and are, as a result, less structured.
* **Non-relational**: Unlike SQL/relational databases, NoSQL databases do not make uses of foreign keys/join tables to track relations between tables.
* **Not table-based**: Whereas SQL databases make use of tables, NoSQL databases use other data storage structures such as key-value pairs and graphs.
* **Less emphasis on ACID properties**: SQL databases focus on being ACID compliant (Atomicity, Consistency, Isolation, Durability). NoSQL databases will sometimes sacrifice some ACID compliance in favor of CAP (Consistency, Availability, Partition Tolerance). This focus is based on the [Brewers CAP Theorem](https://en.wikipedia.org/wiki/CAP_theorem).

MongoDB is a popular example of a NoSQL database.