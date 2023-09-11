**PersonsEntryTable** :

Id	Name	CreateDate
1	John	2022-10-18
2	Jane	2022-09-30
3	Bob	2023-06-27
4	Alice	2022-11-20
5	Charlie	2022-11-16
6	Eve	2022-10-23
7	John	2023-08-15
8	Jane	2023-07-13
9	Bob	2023-01-27

1. Write a query to get the latest date from a table with its name and id
 - Select * from PersonsEntryTable where CreateDate=(Select Max(CreateDate) as LatestDate From PersonsEntryTable);

2. Write a query to get all the latest entry from a table
 - SELECT Name, MAX(CreateDate) AS LatestDate
    FROM PersonsEntryRecord
    GROUP BY Name

3. Now I want all the entries with its id name and the latest entry of the person
 - SELECT p1.Id, p1.Name, p1.CreateDate
	FROM PersonsEntryRecord p1
	INNER JOIN (
    SELECT Name, MAX(CreateDate) AS LatestDate
    FROM PersonsEntryRecord
    GROUP BY Name)
	p2 ON p1.Name = p2.Name AND p1.CreateDate = p2.LatestDate;

4. We can get all the unique names with group by 
 -  Select Name
	From PersonsEntryTable 
	Group By Name