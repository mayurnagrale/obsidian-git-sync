1. User
	1. id 
	2. name 
	3. phno
	4. pwd
	5. Role
2. Group
	1. id 
	2. name
	3. created by
3. Group Participants or members
	1. id
	2. user
	3. Group
	4. Role

4. Enums
	1. Role
5. Expanses
	1. Id
	2. Name
	3. Expanse Date
	4. User CreatedBy
	5. User PaidBy
	6. Amount
How much is contributed by A in new year expense?
Map Expanse with User Also we need Amount(for how much)

6. Expanse paid by
	1. Id 
	2. Expanse
	3. User
	4. Amount

Do we need two classes for paidby and shared by?
7. Expanse Shared By
	1. Id
	2. Exapanse
	3. User
	4. Amount
Yes because we cannot have logic in data we cannot add both of there in single table
and we need logic in service layer

Sparse table
8. Group Expanse
	1. Id
	2. Group
	3. Expanse
		