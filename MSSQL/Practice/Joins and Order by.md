|EmployeeID|EmployeeName|DepartmentID|Salary|
|---|---|---|---|
|1|Alice|101|50000.00|
|2|Bob|102|60000.00|
|3|Carol|101|55000.00|


|DepartmentID|DepartmentName|
|---|---|
|101|HR|
|102|IT|


- Calculate the total salary spent on each department.
	- SELECT Departments.DepartmentName, SUM(Employees.Salary) AS TotalSalary FROM Employees INNER JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID GROUP BY Departments.DepartmentName;
