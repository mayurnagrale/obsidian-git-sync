**Domain Layer** :
- Interfaces are declared here in domain layer and the implementation is mostly done  in Infrastructure layer.  sa.Repository  Also Entities. 


**Application Layer** :
- Commands and Queries
- Commands -> 
	1. CreateApplicationCommand 
	2. CreateApplicationCommandHandler
		1.Handle Method that will have insert logic using ef in that
	3. CreateApplicationCommandValidator 
	4. CreateApplicationCommandRequest 
- Queries ->
	1. GetApplicationDataById
	2. GetApplicationDataByIdQuery
	3. GetApplicationDataByIdHandler
	4. ApplicationResponse
- Design Pattern -split the flow of reading and writing data

**Infrastructure Layer** :
- ApplicationDbContext
- Configurations
- Migrations 
- Repositories

**Presentation Layer** :
- Controllers
	- Ex. User Controller
	- It will have methods sa HttpGet, HttpPost etc

To be able to support dependency Injection you need to define all of your service registration inside of web application, that means you have to reference all of the project inside of your solution so that the controller inside the presentation layer will gain access to anything that has define in out application.

**Web Application** :
- Middleware
- startup.cs 
	- var presentationAssembly = typeof(Presentation.AssemblyReference).Assembly
	- services.AddControllers().AddApplicationPart(presentationAssembly)

**Architecture Tests** :
- NetArchitectureRule
- [[DomainTestEx]]