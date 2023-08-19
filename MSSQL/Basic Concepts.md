**Keys in Sql** :

**Super Key** :
- Set of attributes that helps us to identify unique row

**Candidate Key** : 
- A collection of attribute that uniquely identify the tuple with minimal attribute 
- A candidate key in SQL is a set of one or more columns that can uniquely identify a row within a table.
- A table can have multiple candidate keys, but only one of them can be chosen as the primary key. The primary key is used as the official unique identifier for a row within the table.
- A super key is a set of attributes that can uniquely identify each row in a table. A candidate key is a subset of a super key that cannot be further reduced without losing its uniqueness.

**Composite Key** :
- A composite key in SQL is a combination of two or more columns that are used to uniquely identify a row in a table. Each column in a composite key must be unique, and the combination of all columns must be unique.

**Primary Key** :  
- Enforce data integrity, no null values, uniquely identify the row, one primary key in table
- we will have one primary key for one table but we can define two columns together as a primary known as composite primary key

**Unique Key** : 
- Enforce uniqueness in the column, one null value.
- Unique keys are useful for ensuring that data is unique in a table, but they do not have to uniquely identify each row. This makes them a good choice for columns that are not unique identifiers, but that still need to be unique.

**Is primary key can be a unique key or vice versa** :
- Yes, a primary key is always a unique key, but a unique key is not necessarily a primary key.
- A primary key is a special type of unique key that is chosen to be the official unique identifier for a table. Only one primary key can be chosen for each table.

**Normalization** :
- Normalization is a process of organizing data in a database to reduce redundancy and improve data integrity. It is a key concept in database design, and it can help to improve the performance and scalability of your database.

- 1NF,2NF,3NF,BCNF

- **1NF (First Normal Form)**: A table is in 1NF if all of its columns contain atomic values. This means that each column cannot contain multiple values, and each value in a column must be unique.

- **2NF (Second Normal Form)**: A table is in 2NF if it is in 1NF and all of its non-key attributes are fully functionally dependent on the primary key. This means that each non-key attribute must depend on the entire primary key, not just a part of it.

- **3NF (Third Normal Form)**: A table is in 3NF if it is in 2NF and there are no transitive dependencies between its attributes. This means that no attribute can depend on another attribute that is not part of the primary key.

- **BCNF (Boyce-Codd Normal Form)**: A table is in BCNF if it is in 3NF and every non-prime attribute is non-transitively dependent on the primary key. This is a stricter form of 3NF that eliminates some anomalies that can occur in 3NF tables

**Denormalization** :
-  Access data from higher to lower form


**Store procedure and Function** : 
A **store procedure** is a block of SQL statements that is stored in the database. It is executed as a single unit, which can improve performance and security. Store procedures can be used to perform a variety of tasks, such as:

- Inserting, updating, and deleting data from tables
- Retrieving data from tables
- Calculating values
- Validating data
- Enforcing business rules

A **function** is also a block of SQL statements, but it can only return a single value. Functions are often used to perform calculations or to return a value that can be used in other queries.

The main difference between store procedures and functions is that store procedures can return multiple values, while functions can only return a single value. Store procedures can also be used to perform DML (Data Manipulation Language) statements, while functions cannot.

Example, you could say that a store procedure could be used to insert a new record into a table, while a function could be used to calculate the total sales for a month.

SQL functions: 
	To perform calculations on data 
	To convert data type 
	To format number and dates 
	To modify individual data items 
	To manipulate the output

[[Stored Procedure Examples]]

**Triggers** :
- A trigger is a special type of stored procedure that is executed automatically when a specific event occurs in a table.
- The events that can trigger a trigger are INSERT, UPDATE, and DELETE.
- Triggers can be used to perform a variety of tasks, such as:
    - Logging changes to a table
    - Validating data
    - Enforcing business rules
    - Updating related tables
- Triggers can be created at the table level or at the database level.
- Triggers are executed in the order in which they are created.
- [[Triggers Example]]

**index - clustered and non-clustered** :
**Clustered index** :
- A clustered index is a special type of index that physically orders the rows in a table. The clustered index is the primary key of the table. Only one clustered index can be created on a table.

**Non-clustered index** :
- A non-clustered index is an index that does not physically order the rows in a table. The non-clustered index is created on one or more columns of a table.


identity column: a numeric column in the table that automatically populate when new row is added
				-we can create identity column while creating a table or altering a table
				-identity(seed, increment) .seed is the first value

cross joins - maps the row from first table  to all the rows from second table



union - combines the result of two or more select statement

nvarchar and varchar : nvarchar uses 2byte per character,stores unicode data,multilingual support
						varchar uses 1byte per character, ascii
						char ;for fixed character length in the column

**Delete and Truncate** :
-Delete: row\ , rollback, DML-Data Manipulation , slower than truncate
-Truncate: /Delete all row from table ,no rollback, DDL-Data Definition , faster
	Truncate table table_name;
Drop
-removes table from database
	Drop table table_name;
	
Subset of sql 
-DDL - define database schema 
-DML - manipulation of data inside table
-DCL - deals with right, permissions
-TCL - deals with the transactions of database


Constraints : Specify limit on the data type of the table
	Level of constraints are : column level and table level
	
	NOT NULL - No null values in table
	UNIQUE
	CHECK - to satisfy some specific condition
	DEAFULT
	INDEX - faster retrieval of data

Index - Performance tuning method 
	Creates entry for each values
	faster retrieval

Data Integrity :Accuracy, Consistency 

ACID: Atomicity, Consistency, Isolation, Durability

	
Cross Join : produces the cross product (cartesian product) between two tables

Subquery (query inside query) 
	Outer Query                                                   Subquery
	Select Firstname, Lastname from Employee Where AddressCode IN (Select AddressCode from Office Where Country="India")
	
	Subquery will execute first and passes the data to outer query 
	
Group by : groups the row that have same values into summery row
	often used with aggregate functions 
	Count Max Min Sum Avg

BETWEEN and IN
	between is a range 
	in is from this (from specific set)
	
	
CLAUSE : 
	limit the result set by providing the condition to the query 
	helps filter the row from the entire set of records 

	WHERE and HAVING
	
	HAVING: used in select statement 
			used along with group by 
			without group by it acts like where 
	WHERE: applied to each row on actual table
	
Common records from two table : Intersect ,join , union

Case manipulation functions 
UPPER ,LOWER , INITCAP

DISTINCT
 used to get the unique values from the table
 
View : Virtual table 
	takes less space 
	can combine more tables into one
	
User define function
	Scalar function
	multi-statement valued
	inline table valued 

Auto Increment and Indentity 

*Display current date: Select GETDATE();

*Count the number of records in a table
-Select * from table;
-Select Count(*) from table;
-Select row from sysindex where id=object_id(table1) AND ind_id<2

*(Select Employee From the table that start with the name A
Select Firstname from Employee where Firstname like 'A%';

* Third highest salary from employee table
Select Top 1 from(select Top 3 salary from employee order by salary desc) As emp order by asc

Without using the top keyword
	SELECT salary
FROM employees
WHERE salary < (
    SELECT MAX(salary)
    FROM employees
    WHERE salary < (
        SELECT MAX(salary)
        FROM employees
    )
);	`	`	+

Insert null value in table 
	1.omit column 
	2.insert NULL keyword in values clause

*Fetch alternate record from the table
- using mod function
For even
Select studentId from (select rowno,studentId from Students) where mod(rowno,2)=0; 
For odd
Select studentId from (select rowno,studentId from Students) where mod(rowno,2)=1;

First five characters 
	substring(string,1,5) ..start and end
	right(string,5) ..end
	
	
*Flip the value of a column having 0 and 1 numeric values

Update table_name

SET column_name CASE
	WHEN column_name = 0 THEN 1
	WHEN column_name = 1 THEN 0
	ELSE column_name
END

* Having and group by
	we use group by with aggrigate functions 
	and we use having with group by
	
	Select p.cityname, COUNT(p.city) 
	From Personal p INNERJOIN City c
	ON p.city == c.id 
	Group by city 
	Having Count(p.city) > 3
	Order by Count(p.city) 

*Create stored procedure having two input parameter and one output parameter

create procedure sp 
	@firstInput varchar(50)
	@secondInput varchar(50)
	
	@countofsomething INT OUTPUT
As
Begin 
	selcet @countofsomething = count(*) 
	From table
	where fname=@firstInput
		AND lname=@secondInput
	group by salary
	Having salary>50000
END	

	
How to increase performance of a query?
1.Use index for search and create index of commonly used column in where condition
2.for storing numeric value use define column INT only dont use varchar
3.where we are sure that thre will be no duplicate the dont use UNION -> use union all
4.Minimise the use of distinct keyword
 
 
 Difference between CTE and Temp table
 
 Common Table Expressions - Temporary result set
	-A Common Table Expression (CTE) is a named temporary result set that can be referred to within the context of a single SQL query.
	 Syntax for CTE
	 WITH cte_name (column1, column2, ...) AS (
		SELECT ...
		FROM ...
		WHERE ...
	)
	SELECT ...
	FROM cte_name
	WHERE ...

	-Use of cte
		-Simplify complex query
		-Recursive query
		-Avoid Code Duplication
		
 Temp Table-Temp Tables are physically created in the tempdb database.
 Temporary Tables:
Temporary tables are physical tables that are created in the temporary database (or session) and 
exist only for the duration of a session or a transaction. 
They are primarily used for storing intermediate results during complex data processing tasks.

CREATE TEMPORARY TABLE temp_table_name (
    column1 datatype,
    column2 datatype,
    ...
)

Use of Temporary Tables:
 -Store intermediate results:
 -Break down complex tasks
 -Optimize performance:
 
 Drop Column
 ALTER TABLE Customers
 DROP COLUMN ContactName;