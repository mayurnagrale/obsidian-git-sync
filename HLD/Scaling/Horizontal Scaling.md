- Instead of using one cheap machine start using multiple cheap machine 

In system designing 
- No concepts of one size fits all 
- Its always an trade off and deciding trade off and finding out where the fun is

Trade off between vertical scaling and horizontal scaling 
- Down side of vertical scaling 
	- Cost
	- Preplanning/ estimation 
	- SPOF still exist
- Advantage if horizontal scaling
	- Cost 
	- No need to be super accurate
	- Elasticity is there (being able to increase or decrease load)
	- No SPOF for compute machines (SPOF still exist)
- Disadvantage of Horizontal scaling 
	- Multiple machines communicate via network and network is unreliable 
	- Complex architecture (Complexity in horizontal scaling can be much difficult)
	- Because you now have to distribute compute, storage or multiple modification and the machine will have to talk to each other 
	- Communication b/w machine happens via network and network is always unreliable
- Delicious choose horizontal scaling 

Proxy and Reverse Proxy
Cloud Platform (GCP, Azure, AWS) 
	