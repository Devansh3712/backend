a relational database organises data into rows and columns, which collectively form a table. data is typically structured across multiple tables, which can be joined together via a primary key or a foreign key.

# transactions
a transaction is any operation that is treated as a single unit of work, which either completes fully or does not complete at all, and leaves the storage system in a consistent state.

![how transactions work](https://images.contentful.com/po4qc9xpmpuh/6jbcyfzdVJlc6XCUbzgMzb/96b1a9f0594f1d769f2254bd1abf25c1/database-transaction-1__1_.png)

# transaction states
1) **active**: a transaction is active as long as its instructions are performed
2) **partially committed**: a change has been executed in this state, but the database has not yet committed the change on disk (data is stored in memory buffer)
3) **committed**: all transaction updates are permanently stored in the database, i.e not possible to rollback the transaction after this point
4) **failed**: if a transaction fails or has been aborted in the active state or partially committed state,it enters into a failed state
5) **terminated**: the last and final transaction state after a committed or aborted state, marks the end of the database transaction life cycle

![transaction states](https://images.contentful.com/po4qc9xpmpuh/3CQA2Vahq9s71Iifwz8SHG/15acd162da3b04a09d5c048aa121ce8d/database-transaction-2.png)

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