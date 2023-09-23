Row_Num() :

with temp_name_cte as (

Select Id Firstname, Lastname, Row_Num() 
over (Partition by Firstname , Lastname Order by Id ) as RowNum
	From Employee
)

Delete from temp_name_cte where RowNum > 1

Rank() :

with temp_name_cte as (

Select * , Rank()
over (Partition by Firstname , Lastname Order by Id desc ) as Rank
	From Employee
)

Delete from temp_name_cte where Rank  > 1