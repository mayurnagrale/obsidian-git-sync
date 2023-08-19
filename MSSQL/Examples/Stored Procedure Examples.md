Stored procedure query to insert a data inside table
	create procedure sp @firstName varchar(50), @lastName varchar(50)
	as
	begin
		insert into details (firstName,lastName) values (@firstName, @lastName)
	end