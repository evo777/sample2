# Database Transactions

## What are they?
- A database transaction is a set of separate actions that must all be completely processed in order for the transaction to be successful. For most SQL databases, success is determined by ACID compliance.
- For example, for the query `INSERT INTO USERS (user_name, password, email) VALUES ('foo', 'bar', 'foo@bar.com')` the entire insert operation would be considered to be a transaction containing various separate actions (e.g., inserting a value into each column). In order for the transaction to be considered successful, it much complete in an ACID compliant way.