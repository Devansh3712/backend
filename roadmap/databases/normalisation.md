normalisation is a database design technique that reduces data redundancy and eliminates undesirable characteristics like insertion, update and deletion anomalies. normalisation rules divides larger tables into smaller tables and links them using relationships.

# 1NF (first normal form)
- each table cell should contain a single value
- each record needs to be unique

# 2NF (second normal form)
- table should be in 1NF
- single column primary key that does not functionally dependant on any subset of candidate key relation
	- functional dependency is a constraint that determines the relation of one attribute to another attribute

# 3NF (third normal form)
- table should be in 2NF
- have no transitive functional dependency
	- a transitive functional dependency is when changing a non-key column might cause any of the other non-key columns to change

# BCNF (boyce-codd normal form)
even when a database is in 3NF, still there would be anomalies resulted if has more than one candidate key. a candidate key is any set of columns that have a unique combination of values in each row.