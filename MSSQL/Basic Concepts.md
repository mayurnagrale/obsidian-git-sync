primary + auto increment to create a index column with unique index id

primary : enforce data integrity,no null values, uniquely identify the row, one primary key in table
			we will have one primary key for one table but we can define two columns together as a primary known as composite primary key
unique : enforce uniqeness in the column, one null value,  
joins 

store procedure and function

index - clustered and non-clustered

identity column: a numeric column in the table that automatically populate when new row is added
				-we can create identity column while creating a table or altering a table
				-identity[(seed,increment)] ...seed is the first value

cross joins - maps the row from first table column to all the rows from second table

stored procedure query to insert a data inside table
	create procedure sp @firstName varchar(50), @lastName varchar(50)
	as
	begin
		insert into details (firstName,lastName) values (@firstName, @lastName)
	end

union - combines the result of two or more select statement

nvarchar and varchar : nvarchar uses 2byte per character,stores unicode data,multilingual support
						varchar uses 1byte per character,ascii
						char ;for fixed character length in the column

SQl INTERVIEW PREP

Delete and Truncate 
-Delete: ro\ , rollback,DML-Data Manipulation , slower than truncate
-Truncate: /Delete all row from table ,no rollback, DDL-Data Defination , faster
	Truncate table table_name;
Drop
-removes table from database
	Drop table table_name;
	
Subset of sql 
-DDL - define database schema 
-DML - manipulation of data inside table
-DCL - deals with right, permissions
-TCL - deals with the transactions of database

Primary key : uniquely identify a tuple or set of attributes

Unique key: uniquely indentify single row in a table
            multiple unique keys are allowed in a table
			null values are allowed
			duplicate values not allowed
			
Foreign key: maintains a referentiel integrity between two tables by enforcing a link between
			 foreign key in child table -primary key in parent table link
			 it prevents all the actions that can destroy the link between two tables
	

Constraints : Spacify limit on the data type of the table
	Level of contraints are : column level and table level
	
	NOT NULL - No null values in table
	UNIQUE
	CHECK - to satisfy some specific condition
	DEAFULT
	INDEX - faster retrieval of data

Index - Performance tuning method 
	Creates entry for each values
	faster retrieval

Data Integrity :Accuracy,Consistency 
Unique Index : 
Clustered and Non-Clustered INDEX
Clustered: sort out row by column
	Searching is faster in cluster index as it create a data using btree structure format if we want a rearrange data
	if you are searching for specific value or do filtering then non clustered is faster
	
	but insertion and updation is faster in non clustedIndex 

Denormalisation : access data from higher to lower form
Normalisation : Avoid duplicacy and redundancy
	1NF,2NF,3NF,BCNF

ACID:Atomicity,Consistency,Isolation,Durability

Trigger: Special type of stored procedure 
	execute automatically after the modification of the data
	insert update delete , before after 

	
Cross Join : produces the cross product (cartesian product) between two tables

Subquery (query inside query) 
	Outer Query                                                   Subquery
	Select Firstname,Lastname from Employee Where AddressCode IN (Select AddressCode from Office Where Country="India")
	
	Subquery will execute first and passes the data to outer query 
	
Group by : groups the row that have same values into summery row
	often used with aggrigate functions 
	Count Max Min Sum Avg

BETWEEN and IN
	between is a range 
	in is from this (from specific set)
	
SQL functions: 
	To perform calculations on data 
	To convert data type 
	To format number and dates 
	To modify individual data intems 
	To manipulate the output
	
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
	

STORED PROCEDURE: 
	A function which consists many sql statement
	several statements are consolidate into stored procedure and are executed whenever wherever
	Saves time and avoid writing code again and again

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