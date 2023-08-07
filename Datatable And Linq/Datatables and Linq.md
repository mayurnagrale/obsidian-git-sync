Class Employee: Datatable{
	public Employee(){
		this.column.add("Id",typeof(int)); Name,Age Dept and Salary
	}
}


Datatable employee;
employee.add(1,"Name",30,"IT",5000);

-Using Ling query to the datatable
	var query = from em in Employee.AsEnumerable() //To make iterable
				where em.Field<string> ("Dept")=="IT"
				orderedby em.Field<int> ("Salary") descending
				select new{
					Id=em.Field<int> ("Id"),
					Name...
				}
	
	printing the result of query
	foreach(var item in query){
		Console.writeline("Id":{0},,,,item.Id,item.Name...);
	}