**Delete Duplicate Data** :

DELETE from table_name
Where RowId IN (
	Select RowId from table_name
	Group By column_name
	Having Count(*) > 1
)

example : 
Delete from PersonsEntryRecord
  where Name IN(
  SELECT  Name 
    FROM PersonsEntryRecord
    GROUP BY Name
    HAVING COUNT(*) >1
  )

**Get Duplicate value from the table** :

Select Name,Count('*') as Ct
From table_name
Group By Name 
Having Count("**")>1;


**Delete using cte** :

with cte As(
		Select column_name,ROW_NUMBER() over (PARTITION BY Name ORDER BY Name) AS row_num from table_name;
)
Delete from cte
Where row_num > 1;

- With: creates a temporary table of name 'cte'
- over: requires with ROW_NUM() function
- PARTITION BY clause:  This groups the rows in the `cte` table by the specified column(s). In this case, we are grouping the rows by the `Name` column.


To delete all the duplicate records along with the  its original record

Delete from tabe_name
Where Name IN(
	Select Name From table_name
	Group by Name
	Having Count(*)>1

)

If we want to delete only duplicate record 

with cte as(
	select name,row_number() over (partition by name group by name) as row_num
)

Detete from cte 
where row_num>1
