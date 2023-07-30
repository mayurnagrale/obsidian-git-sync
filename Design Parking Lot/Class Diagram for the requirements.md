1. Parking_Lot
	id 
	address
	List<Parking_floor>
	List<Gate>
	Map<vehicle_type, price >base
	Map<vehicle_type, duration> multiplier
2. Parking_floor
	id
	floor_number
	capacity
	List<parking_spot>
3. Abstact gate
	id 
	operator
	number
	status
	gate_type
4. Entry_gate
	id 
	operator 
	gate_number
	status
5. Exit_gate
	id 
	operator
	gate_number
	status
6. Parking_spot
	1. id
	2. vehicle_type
	3. number
	4. status

Enums and Entities
1. Vehicle Type
	1. Electric
	2. Car
	3. Bike
	4. Ebike
	5. Premium Car
	6. Truck
2. Parking spot status
	1. Available
	2. Unavailable
	3. Occupied
3. Spot status
4. Payment status
5. Payment mode

Models
1.Parking lot
2.Parking slot
3.Gate
4.Vehicle
5.Ticket
6.Bill 
7.Payment
8.Operator

Interfaces
