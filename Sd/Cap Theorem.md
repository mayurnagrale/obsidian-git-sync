- C= Consistency
- A= Availability 
- P= Partition Tolerance

Consistency : You always reading the latest version of the data or you are getting always the sync or updated data 

Availability : You should be able to support / answer the request 

Partition Tolerance : ![[Screenshot 2023-09-10 at 10.28.16 PM.png]]

All the machine talk to each other via network and network is always unreliable.

Network Partition - Two machines are not able to connect via network  and reason can be anything.

Partition Tolerance : is that we are agreeing that in a distributed system there will be always Network Partition can happen and we are there to handle that

CAP Theorem : In any distributed system you can only have 2/3 Properties.


Distributed System : Partition tolerance will be always there so we will have to choose between Consistency and Availability and one of them is always compromise.
so we will be building 'AP' or 'CP system here'.

In a distributed system there will be communication between machines and network will be there and whenever network is there the will be network partition due to unreliability of the network and whenever network partition is there. there will be Partition tolerance.

Any distributed system you build can always have partitions at any time which means that partition tolerance is given hence the choice boils down between A or C

Vertical System : As we don't have multiple machine we can have consistency and availability here and can build a 'CA' system.

MSSQL server can be a example of CA system.


