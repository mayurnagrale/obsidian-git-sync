We use case statement to do that _->_

Select 
ID 
Max(Case
When Name = 'Name' then Value Else ' ' End) as Name

Max(Case
When Name = 'Gender' then Value Else ' ' End) as Name

Max(Case
When Name = 'Salary' then Value Else ' ' End) as Name

from Employee

Group By Id