NoSQL are non-tabular databases and store data differently than relational tables. it allows one to store huge amounts of unstructured data, giving a lot of flexibility.

# BASE
it is an acronym that stands for basically available, soft state, eventually consistent. it represents a set of properties that are often desired in distributed and NoSQL database systems.
- **basically available**: system remains operational and responsive despite failures, prioritises availability over consistency
- **soft state**: the system's state might change over time, even without input or action from the user. this concept allows for eventual consistency
- **eventually consistent**: while the system might exhibit inconsistency at any given moment due to asynchronous updates and replication delays, it will eventually resolve those inconsistencies

# types
- **document**: store data in documents similar to *JSON* objects. each document contains pairs of fields and values
- **key-value**: a simpler type of database where each item contains keys and values
- **wide-column**: store data in table, rows and dynamic columns
- **graph**: store data in nodes and edges. nodes typically store information about people, places, and things, while edges store information about relationship between the nodes

# data modelling
data modelling refers to the organisation of data within a database and the links between related entities. NoSQL databases have a flexible schema, i.e, a field's data type can differ between records. the schema can change over time as needs of the application change.

# database scaling
database scalability is the ability to expand or contract the capacity of system resources in order to support the changing usage of an application.
- **vertical scaling**: refers to increasing the processing power of a single server or cluster
- **horizontal scaling**: refers to bringing on additional nodes to share the load