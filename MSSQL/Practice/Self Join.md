| employeeid |   fname   |   lname   | managerid |
|------------|-----------|-----------|-----------|
|     1      |   John    |   Smith   |    2      |
|     2      |   Sarah   |   Johnson |    3      |
|     3      |   Michael |   Davis   |   NULL    |
|     4      |   Emily   |   Wilson  |    2      |
|     5      |   David   |   Lee     |    1      |

Fetch the managers of employee 

Select emp.fname +'  '+emp.lname as Employee , 
	mgr.fname+' '+mgr.lname as Manager
from Employee emp INNER JOIN Employee mgr 
ON emp.managerid = mgr.employeeid 