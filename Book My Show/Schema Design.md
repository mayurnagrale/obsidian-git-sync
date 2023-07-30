Rules of Schema Design
1. Classes and Enums becomes tables.
2. Primitive attribute becomes columns.
3. Relationship(non primitive datatypes) 1:1 --> foreign key any side.
    1:M or M:1--> foreign key on m side, M:M --> Cardinality(need mapping table)

All Enums as table with two columns -->  id, value

Classes becomes tables 
1. City: id, name
2. Theatre: id, name, address , maxSeatsBA | City_id(C:T)
3. Audi: id, name,  row, col | Theatre_id(T:A) | AudiFeatures
4. User: id, name, username, password | UserTable
5. Seat: id, number, row, col | Audi_id(A:S), SeatType_id(S:ST)
6. Show: id, name, startTime, endTime | Audi_id(A:S) | ShowFeature
7. Ticket: id, bookingTime | U_id(T:U)
8. Payment: id, amount, transac_id | Ticket_id(T:P)
9. SeatInShow: id | Seat_id, Show_id, SeatStatus_id
10. SeatTypeInShow: id, price | SeatType_id, Show_id

Tables from M:M relationships
1. AudiFeatures: id, Audi_id, Feature_id(enum table)
2. UserTable: id, U_id, R_id
3. ShowFeature: id ,S_id, F_id 
