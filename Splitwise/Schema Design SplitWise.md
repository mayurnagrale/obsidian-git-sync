Tables
1. User
	1. Id
	2. Name 
	3. Password
	4. Pno
	5. Role
2. Group 
	1. Id 
	2. Name
	3. User Created By (from User to Group (1:M Relationship means  1 User can create many group)
3. Group Participant
	1. Id
	2. Group Id (from Group Participant to Group (M:1) Relationship )
	3. User Id(from Group Participant to User(M:1) As 1 User can be in Multiple Group)
	4. Role
4. Expanse
	1. Id
	2. Name
	3. Expanse_Date
	4. Amount
	5. User Created By (Expanse to User M:1 )
5. Expanse Paid By
	1. Id 
	2. Amount 
	3. User to Expanse Paid by User (M:M) 
	4. eid
	5. uid
Two foreign key can refer to same column

6. ExpenseSharedBy
	1. Id
	2. eid
	3. uid
	4. Amount

7. Settlement 
	1. id 
	2. from_user_id
	3. to_user_id
	4. Amount

    