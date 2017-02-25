# Popular relational database management systems (RDBMS):

## Open-sourced

- SQLite - Unlike other RDMSs, SQLite is not a client-server database engine. Instead, it is an 'embedded' system, meaning that it is closely tied to the application that it serves. In other words, SQLite databases are self contained and don't run on a separate server.
    - **Advantages:**
        - Requires 'zero configuration'
        - Does not require a separate server process in order to run
        - Self-contained and does not rely on external dependencies. As such, it works well for applications that require portability (e.g., Android/iOS apps)
        - ACID compliant
    - **Disadvantages:**
        - Certain SQL commands not supported (E.g., RIGHT OUTER JOIN, FULL OUTER JOIN)
        - Size limitations (usually 2GB)
        - Not scalable
        - Does not allow multiple write operations (not realistic for applications with high write volumes)

- MySQL - Most popular of the large-scale RDMSs (it is the database used in the popular LAMP stack). It developed by Oracle, but still open-sourced.
    - **Advantages:**
        - Easy to work with - installation is simple and many third-party tools that make it easy to get started
        - Many built-in security features
        - Scalable as it can handle large amounts of data
        - Very fast (although this comes at the cost of not complying with some SQL standards)
    - **Disadvantages:**
        - Lacks some features found in other 'state of the art' RDMS options
        - Can be less reliable than some other RDMS options
        - Stagnated development since its acquisition by Oracle
        - Not great with concurrent read/write operations

- PostgreSQL - Aims to be the most advanced open-source RDMS
    - **Advantages:**
        - Fully SQL and ACID compliant (i.e., very good data integrity)
        - Very experienced community and strong third-party support
        - Extensible - additional custom functionality can be added  
    - **Disadvantages:**
        - Not as fast as MySQL
        - Set-up can be more complicated


## Proprietary: 

- Oracle Database - Commercial database that offers all the 'bells and whistles'
    - **Advantages**:
        - World-class support (because you pay for it)
        - More advanced feature than open-source options
    - **Disadvantages**:
        - Expensive

## Additional resources
https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems