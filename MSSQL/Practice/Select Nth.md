
with temp_name_cte as (

Select * , Dense_Rank() over (order by salary desc) as salary_order from Employee

)

select * from temp_name_cte where salary_order = 1