Replication : Create copies of data, creates copy of data to achieve durability and Redundancy. 

1 way of doing replication is **Master - Slave Replication** or Leader - Follower Replication.
Means we are maintaining a operations at one main machines and other machines which have the copies of the original data is to maintain the copy

**In-Sync Replication** : When "Write" come to main machine and then it will get copied to other slave machines and that machines will respond back to the main machine. 
and after all machines responses main machine will say write is completed.

M-S replication is one way of replication which ensures that data is durable /data does not get lost forever.

The other use case of M-S replication is that Write Can perform on master machine but read request can be transfer(divided amongst) to Slave machine. 

Read Replica -Another word for slave machines used when we have reads >>> write system

For this system : we have better Consistency and Low Availability according to CAP theorem and High latency according to PACELC theorem.

But one more advantage will be apart from consistency is that in case of master failing and new slave is being updated 0 data loss will be there.

**Async Replication** : As we are not writing immediately to slaves consistency will come down but latency will be reduced. And availability will increase as write can be still taken even slave is not available.

In case of master failing and new slave is being updated some data loss will be there.


**Quorum Approach** : In between of above to replication type.


Replication will be there primarily where storing of data is needed. in catching usually we don't require replication as it has a limited storage.

Sharding : Dividing or Distribute 