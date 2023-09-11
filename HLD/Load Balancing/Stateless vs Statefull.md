In horizontal scaling we are handling request with multiple machine and Gateway machines has to decide where to forward request

- All the machines are powerful/capable enough to serve incoming request
- It can be assign to any machine by load balancer that which machine will serve the request and send the result back 

Stateless : All the machine are equally well-equipped to take any request 
- Round Robin Algorithm

Stateful : Maintain some state for every request so that related request can be handled by some particular machines. 
- Consistent Hashing Algorithm

Storage layer is always stateful

Compute layer can be stateless or stateful

App-server should be made stateless whenever we can do that as stateless app servers are much easier to manage / scale up /scale down 
But 
You cant afford to have stateless app server always.
Why??
Because at times its better for app server to store some states so that the computation can be faster / slower


+network time 
+db access/ query
+computing the vector 