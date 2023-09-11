Storing copies of data so that the reads can be quicker and ultimately latency for user can be reduced. 

**Type of catching** : 
1. Client side catching (In Browser Catching)
2. DNS Catching
3. CDN Catching 
4. App Server Catching
5. Global Catching
6. DB Catching

Redis 

Catche static resources
1. DNS Mappings 
2. Images, Videos 
3. JS Files 

Hot-star  Problems in Streaming platforms 
1. Super high latency for end user
2. Bandwidth clocking at hot-star's end

Solution for this problems 
CDN
Content Delivery Network
- Akamai (OG)
- Cloud Flare
- Cloud Front by AWS
- Fastly 

1. Now Hot-star Copy its data to Central CDN Server
2. Based on agreement of usage pattern and deals with related to it this CDN company with push its content on CDN global server -> push it to its top machine (main server machines across the world ) 
3. Now based on the user response on video CDN will send copy from top main CDN servers to other remaining servers (initial video will slower for some user because it will get pulled from the top servers)
4. 2 ways CDN can send data to users
	1. Based on your location it will give you CDN link of nearest or nearby node
	2. Anycast Routing



FB maintains a copy of trending profile in a Global cache so that Latency for millions of requests can be reduced.
Global Cache : Its a cluster of machines storing data in main memory / SSD so that latency can be reduced.


Cache Hit Rate
1. No Cache 
	1. Latency = Network Time + DB Read Time + DB Connection Time 
2. Cache 
	1. Cache Hit
	2. Cache Miss
