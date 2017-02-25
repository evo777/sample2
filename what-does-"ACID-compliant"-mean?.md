#ACID Compliance

ACID compliance is a set of standards for database transactions. ACID stands for Atomicity, Consistency, Isolation, and Durability.

## Atomicity
The Atomicity property of ACID compliance states that either all or none of the properties of a transaction are completed. For example in the following case, either both name and age will be updated, or neither will in the event of a failure. A database with Atomic transactions will never have only one updated.

```sql
UPDATE USER WHERE id=1 SET name="John", age="25"
```

## Consistency
The Consistency property of ACID compliance states that the stored data will remain consistent with any rules set for that data. For example the following syntax for SQL Server will not allow for null input nor numbers less than 100 to be inserted into it.

```sql
create table numbers (
    number int not null
        check(number >= 100),
    ...
)
```

## Isolation
Any database transactions (e.g., reads, writes) that are in process must remain isolated from other transactions. As such, two transactions cannot interact with the same piece data at the same time. Different RDMS implement this in different ways (e.g., during a transaction they may lock a single row, the entire table, or, as is the case of SQLite, the entire database)

## Durability
The Durability property of ACID compliance states that after a transaction has successfully completed, it will not be undone, even in the event of power loss to the database.