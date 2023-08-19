CREATE TRIGGER MyTrigger ON MyTable
AFTER INSERT
AS
BEGIN
    INSERT INTO MyLogTable (Message) VALUES ('New record inserted');
END;


CREATE TRIGGER MyTrigger ON MyTable
AFTER UPDATE
AS
BEGIN
    IF UPDATE(Name) THEN
        UPDATE MyOtherTable SET Name = NEW.Name
        WHERE MyOtherTable.ID = OLD.ID;
END;


*Create stored procedure having two input parameter and one output parameter

create procedure sp 
	@firstInput varchar(50)
	@secondInput varchar(50)
	
	@countofsomething INT OUTPUT
As
Begin 
	selcet @countofsomething = count(*) 
	From table
	where fname=@firstInput
		AND lname=@secondInput
	group by salary
	Having salary>50000
END	
