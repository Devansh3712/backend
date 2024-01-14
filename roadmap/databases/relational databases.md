a relational database organises data into rows and columns, which collectively form a table. data is typically structured across multiple tables, which can be joined together via a primary key or a foreign key.

# transactions
a transaction is any operation that is treated as a single unit of work, which either completes fully or does not complete at all, and leaves the storage system in a consistent state.

# ACID properties
- **atomicity**: all changes to data are performed as if they are a single operation, that is, all the changes are performed, or none of them are
- **consistency**: data remains in a consistent state from start to finish, reinforcing data integrity
- **isolation**: the intermediate state of a transaction is not visible to other transactions, and as a result, transactions that run concurrently appear to be serialised
- **durability**: after the successful completion of a transaction, changes to data persist and are not undone, even in the event of a system failure

# SQL
structured query language is a programming language for storing and processing information in a relational database. SQL queries are valid instructions that the DBMS understand.

SQL commands are specific keywords or statements that one can use to manipulate data stored in a relational database. they can be categorised as:
- **data definition language**: DDL statements refers to commands that design the database structure
- **data manipulation language**: DML statements write new information or modify existing records in a relational database
- **transaction control language**: the relational engine uses TCL to automatically make database changes