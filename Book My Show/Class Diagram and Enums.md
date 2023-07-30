Enums 
1. Seat type
	1. Silver
	2. Gold 
	3. Platinum
2. Role
	1. Admin
	2. Owner
	3. User/Customer
3. features of show or Audis
	1. 2D
	2. 3D
	3. Dolby
	4. 4dx
4. status of seat in a show
	1. Under Maintenance
	2. Locked
	3. Booked
	4. Available
5. theatre status
	1. Open
	2. Closed
6. payment mode 
	1. Card
	2. Net-banking
	3. UPI
7. payment status
	1. Failed 
	2. Successful 
	3. In process
8. Event type
	1. Movie
	2. Live Match
	3. Comedy/Poetry show

Class diagram 
1. City
	1. Id
	2. Name
	3. List<Theatre> 
2. Theatre 
	1. Id 
	2. Name
	3. Address
	4. City
	5. List<Auditorium>
3. Auditorium
	1. Id 
	2. Name
	3. List<seat>
	4. List<features> SupportedFeature
4. Seat
	1. Id
	2. Number
	3. Type
	4. Row and Column
5. Show
	1. Id 
	2. start time and end time
	3. Auditorium
	4. Name
	5. EventType
	6. List<feature> RequiredFeature
6. Ticket
	1. id
	2. user
	3. booking time
	4. Seat in a show
7. User
	1. Id
	2. Name
	3. UserId/UserName
	4. Password
	5. List<role>
8. Payment
9. Event
	1. id
	2. Name
	3. Type/EventType
10. Bill
11. SeatInShow
	1. id
	2. Seat
	3. Show
	4. Seat status
12. SeatTypeInShow
