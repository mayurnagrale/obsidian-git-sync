Ways to update catche (how to keep catche updated)
1. Write through catche
2. ![[write-through-catch.png]]
	1. Adv : Always in-sync with the database
	2. Con : 
		- More latency of write
		- Less availability 
3. Write back catche 
4. ![[write-back-catch.png]]
	1. Pros : 
		- Catche is always up to date
		- Latency of read is super low
		- Catching of writes also very fast
	2. Cons :  
		- Data can be out of sync / in-consistent 
		- Data may get lost forever
5. Write around catche
6. ![[Screenshot 2023-09-10 at 12.36.56 PM.png]]
	1. Pros : 
		- Data is never lost
		- More available
		- Avg latency
	2. Cons : 
		- Data is out of sync 


Catche eviction strategy
There should be ways to decide if we should kick out / delete less important  data in order to make place for more important data.

Ways :
1. FIFO
2. LRU
3. LIFO
4. MFU
5. MRU