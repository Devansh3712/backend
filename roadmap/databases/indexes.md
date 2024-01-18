an index maps search keys to corresponding data on disk by using different in-memory and on-disk data structures. index is used to quicken the search by reducing the number of records to search for.

# difference between key and index
the terms `key` and `index` are used interchangeably, `key` means a constraint imposed on the behaviour of the column whereas `index` is a special data structure that facilitates data search across the table.

# clustered index
a clustered index is collocated with the data in the same table or same disk file. records are stored on the disk block in any arbitrary order. whenever new records are added, they get added to the next available space.

![clustered index](https://cdn-media-1.freecodecamp.org/images/aVIkXV0c5nNwQHjL1T501JC0OG-E9iZGzt3H)

this ordering of related data actually makes a clustered index faster. the clustered index reduces the number of disk IO by collocating related data as much as possible in the same data block, which causes improvement in performance.

since a clustered index impacts the physical organisation of the data, there can be only one clustered index per table.

# structure of clustered index
an index is usually maintained as a B+ tree on disk and in-memory, and any index is stored in blocks on disk, and are called index blocks. the entries in the index block are always sorted on the index/search key.

# primary indexing
it is a type of clustered indexing wherein the data is sorted according to the search key and the primary key of the database table is used to create the index. as primary keys are unique and are stored in a sorted manner, the performance of the searching operation is quite efficient.

# types of primary indices
- **dense index**
	- an index appears for *every* search key value in file
	- this record contains search key value and a pointer to the actual record
	- faster in general
- **sparse index**
	- index records are created only for *some* of the records
	- to locate a record, we find the index record with the largest search key value less than or equal to the search key value
	- requires less space and impose less maintenance for insertions and deletions
	- the data should be sorted

# secondary indexing
it just gives a list of virtual pointers or references to the location where the data is actually stored. data is not physically stored in the order of the index. we can have only dense ordering in secondary (non-clustered) index as the data is not physically organised.

# multilevel indexing
the multilevel indexing segregates the main block into various smaller blocks so that the same can be stored in a single block. the outer blocks are divided into inner blocks which in turn are pointed to the data blocks.

# references
- https://www.freecodecamp.org/news/database-indexing-at-a-glance-bb50809d48bd/
