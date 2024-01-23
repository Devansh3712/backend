the CAP theorem states that a distributed system cannot simultaneously be consistent, available and partition tolerant.
- **consistency**: all clients see the same data at the same time, no matter which node they connect to
- **availability**: any client making a request for data gets a response, even if one or more nodes are down
- **partition tolerance**: the cluster must continue to work despite any number of communication breakdowns between nodes in the system

NoSQL databases are ideal for distributed network applications. they are classified based on the 2 CAP characteristics they support:
- **CP database**: delivers consistency and partition tolerance at the expense of availability. when a partition occurs between any 2 nodes, the system has to shut down the non-consistent node until the partition is resolved
- **AP database**: delivers availability and partition tolerance at the expense of consistency. when a partition occurs, all nodes remain available but those at the wrong end of a partition might return an older version of the data than others
- **CA database**: delivers consistency and availability across all nodes. it can't do this if there is a partition between any 2 nodes in the system, and therefore can't deliver fault tolerance

in a distributed system, partitions can't be avoided. for all practical purposes a CA distributed database can't exist.