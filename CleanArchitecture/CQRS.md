Command Query Responsibility Segregation
- Command : It represent the actions that modifies the state of the system. like create, update and delete.

- Command Model : It represents data and logic needed to be process and execute commands

- Command Handler : These are components responsible for processing commands, enforcing business rules, and updating the write model

- Query : It represent operation that are used to retrieve data from the system without modifying the state of the system

- Query Model : The query model represents a denormalized view of the data that is optimized for reading

- Query Handler : These components are responsible for handling queries and retrieving data from the optimized query model.

- Event Sourcing : Event sourcing involves storing the history of changes as a sequence of events. These events are used to build the current state of the system's models. This can be especially beneficial for audit trails, debugging, and maintaining a historical record of changes.

- Read and Write Databases : CQRS often advocates using separate databases for read and write operations. The write database stores the authoritative data and is optimized for writes, while the read database stores the denormalized data and is optimized for fast queries.
