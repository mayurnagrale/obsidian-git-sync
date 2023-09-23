1. For all the classes in your class diagram create tables.
2. For the primitive types attributes in those classes we will represent them as columns in the corresponding tables.
3. For non primitive attributes -> relationship/associations
	1. Find cardinality of the relation (1:M,M:1,M:M)
	2. Depending on the cardinality represent it in the table
	3. For Enums and Inheritance relationship represent the attributes accordingly
	4. To avoid having many null values in single column we can create sparse table for mapping  table

	This will be the initial stage for creating database later on you will need to adjust and expand the schema based on additional requirements and complexities, there are other things also that need to be considered ex.
**Data Validation** :
**User Authentication** :
**Handling Edge Cases** :
**Optimizing Database Queries** :


Latency And Throughput : 
Latency : How long "it" takes
Throughput : How many "Per unit of time"


![[Screenshot 2023-09-17 at 9.53.49 PM.png]]

In our system we are checking wha impact throughput the most and latency?
Throughput can be affected by size of the hardware and efficiency of the individual operation. 
Schema, Queries, Indexes can help in getting better result in efficiency of the operation.

Schema Anti-Pattern : 
1. Over Normalisation
	1. Joins 
	2. read vs writes 
	3. Polymorphic collection 
	4. Polymorphic field 
2. Over Embedding 
	1. Unbounded growth 
	2. Deeply nested array 
	3. Really large document 

Find and Modify (update and return) vs Update One (update)

UpdateOne : returns -> how many documents are updated match or not found 