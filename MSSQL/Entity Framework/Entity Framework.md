- ORM-Object relation Mapping develop by Microsoft 
	 - framework provides high level abstraction and simplifies the process of working
	 - methods for CRUD operation
	 - bridge between oop and rdbms
	 - Linq on entity 
	 - Changes tracking on entities 
	 - Have support for multiple databases

Packages for Entity Framework
Microsoft.EntityFrameworkCore
Microsoft.EntityFrameworkCore.SqlServer
Microsoft.EntityFrameworkCore.Tools

Create Data Folder inside that create one class with class name extending with DbContext  also make it Child of DbContext class.

Create a constructor with DbContextOptions parameter

Create DbSet of the Modals

If you want to create db from your modal then you can use OnModalBuilder method

To connect with the db you need to add DbContext class to service via Injuction 

builder.Services.AddDbContext<AuthorBookDbContext>(Options=>Options.UseSqlServer(builder.Configuration.GetConnectionString("AuthorBookConnectionString")));