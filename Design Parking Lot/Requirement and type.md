What is it? What kind of system do we need to create?
web based application.

Gathering requirements
1. Multiple floors
2. Multiple entry exit gates
3. Different type of vehicles
4. At entry gate ticket is generated
5. At exit gate bill is generated
6. Assign a spot at entry
7. Payment can be done at exit 
8. Different spot for different type of vehicle
9. Different payment mode (cash, upi)
10. Status of the spot

Clarifying requirements
1. Support multiple ways to assign spots ([[Strategy design pattern]])
2. How bill is going to be generated? 
    1. Duration of the parking
    2. Type of the vehicle
3. Supports partial payments (online + cash)
4. Multiple ways to calculate parking charges(fees)
5. Payment algorithm (different prices for different vehicles + multiplier)
6. For electric vehicle spot with charging slow and also different fees according to electricity unit used in the meter at the spot
