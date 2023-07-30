1. ASP.NET MVC Architecture: Understand the Model-View-Controller (MVC) architectural pattern and how it separates concerns in web development.
	    Advantages:
	    1. easier to maintain, test, and extend.(Separation of Concerns)
	    2. can be unit tested independently, enabling better test coverage.(Testability)
	    3. The Model and business logic can be reused across different Views and user interfaces.(Reusability)
	    4. MVC supports building large-scale applications with modular components.(Scalability)    
2. Controllers: Know how controllers handle incoming HTTP requests, process data, and return responses to the client.
	    1. Handling HTTP Requests: GET, POST, PUT, DELETE
	    2. Accessing Request Data
	    3. Processing Data and Business Logic
	    4. Returning Responses -> `ActionResult`, `ViewResult` (renders corresponding view), `JsonResult`, `RedirectResult`, `PartialViewResult`
	    5. TempData and ViewBag : To transfer data from controller to view we have tempdata and viewbag
3. Views: Understand how views are used to render the user interface and present data to users.
	    1. Presentation Layer:
	    2. Data Binding:
	    3. Razor Syntax:
	    Example of databinding and razor syntax
		    <p> @if (Model.Age >= 18) { <p>You are an adult.<p> } </p>
		4. Layouts and Partial Views
			1. Layouts: A layout is a shared template that wraps around multiple views, providing a common header, footer, and navigation for all pages.
			2. Partial Views:Partial views are reusable components that can be embedded within other views. They help promote code reuse and simplify the organization of complex user interfaces.
		5. View Models: To keep Views decoupled from the Model and to provide only the data needed for rendering the UI, Views often use View Models.
		   <p> public class PersonViewModel { public string FirstName { get; set; } public string LastName { get; set; } }</p> ^50104a
	 6. Strongly Typed Views:  This allows for compile-time type checking and reduces the likelihood of runtime errors.
4. Models: Know how models represent the data and business logic of the application.
5. Routing: Understand URL routing in ASP.NET MVC and how it maps incoming URLs to specific controllers and actions.
	1.  Type of routing
		1. Convention-based 
			RouteConfig.cs -> Register routes -> map route
		2. Attributes
			way to define routes directly within the controller or action methods, 
			URL pattern and route constraints
6. Action Results: Know about different types of action results (e.g., ViewResult, JsonResult, RedirectResult) and how to return them from controller actions.
	 1. Data Representation
	 2. Data Access and Manipulation
	 3. Business Logic
	 4. Validation
	 5. View Models
7. Razor Syntax: Understand Razor syntax used in views to dynamically generate HTML.
    1. Inline Expression
        - to display data from the Model, execute loops and conditionals, and perform calculations.
        - <Welcome, @Model.FirstName!
    1. Code Blocks 
        - @{ }
    2. Html Helpers
        - @Html.ActionLink("Click Here", "About", "Home")
    3. Form handling and Modal binding
        - 
    4. Layouts and partial view
        - to create reusable components and define consistent page structures.
8. Data Annotations and Model Validation: Know how to use data annotations to apply validation rules to model properties.
    1. Required Attributes
        - [Required]
    2. String Length Attributes
       - [StringLength(50, MinimumLength = 3)]
    3. Regular Expression Attribute
       - [RegularExpression(@"^\d{5}$", ErrorMessage = "Please enter a valid ZIP code.")]
    4. Range Attributes
       - [Range(1, 100)]
    5. Compare Attributes
       - [Compare("ConfirmPassword", ErrorMessage = "Passwords do not match.")]
    6. Custom Validation Attribute
       - You can create your own custom validation attributes by inheriting from the `ValidationAttribute` class and overriding the `IsValid` method.
9. Form Handling: Understand how to handle form submissions and data binding between views and controllers.
    
10. ASP.NET Identity: Know how to implement user authentication and authorization using ASP.NET Identity.
     -  Identity is a membership system that provides authentication and authorization features
     -  public void ConfigureServices (IServiceCollection services) Add Identity services
     -  User Registration and Login: With ASP.NET Identity set up, you can now implement user registration and login functionality. In your application's controllers and views, you can use the `UserManager` to create and manage user accounts.
     - **Authentication and Authorization**
        [Authorize(Roles = "Admin")]
        [Authorize(Roles = "User, Admin")]
     - **Additional Authentication Features:**
         - Two-factor authentication (2FA)
         - Account confirmation and password reset via email
         - Lockout and account recovery policies
         - Social login (OAuth providers)
11. Bundling and Minification: Understand how to bundle and minify CSS and JavaScript files for optimized performance.

	   - Bunding: Bundling is the process of combining multiple CSS or JavaScript files into a single file. 
	    - The browser makes a single request to fetch the bundled file, reducing the number of HTTP requests and improving the page load speed.
	    - Minification: Minification is the process of removing unnecessary whitespace, comments, and renaming variables to shorten the names in the CSS and JavaScript files. 
	    - The minified version of the code has the same functionality but is much smaller in size, leading to faster download times.
	    - `System.Web.Optimization`  , `BundleConfig.cs` , `BundleTable.EnableOptimizations`
12. Partial Views and Layouts: Know how to use partial views to create reusable components and layouts for consistent page structure.
    
13. Action Filters: Understand how action filters are used to perform cross-cutting concerns, such as logging and authentication.
     1. Authorization Filter -> Restrict access to the specific user(Roles)
     2. Action Filter -> OnActionExecuting, OnActionExecuted
     3. Result Filter
     4. Exception Filter -> 
    
14. Dependency Injection: Know how to use dependency injection to improve code maintainability and testability.
    
15. Routing Attributes: Understand how to use routing attributes (e.g., `[Route]`, `[HttpGet]`, `[HttpPost]`) to define routes directly on controller actions.
      1.Route Attribute
      2.HTTP Method Attributes
      3.Route Constraints {}
      4.Route Prefix 
1. TempData and ViewBag: Know how to use `TempData` and `ViewBag` to pass data between controller and view.
	    1. TempData (single session state in one req) and ViewBag (pass data from controller to view no session state, data is available within current request)
2. ViewModel: Understand the use of ViewModel to pass data from controller to view and vice versa.
    1. Data Aggrigation
           ViewModels allow you to combine data from multiple models into a single object, making it easier to work with complex views that require data from different sources.
    2. Data Transformation
	    Sometimes, the data required by the view may not directly match the structure of the model. The ViewModel can transform the data into a format that better suits the view's needs.
    3. Enhance Abstraction
    4. Avoid over exposure of Model data
3. Web API: Know how to build RESTful Web APIs using ASP.NET MVC Web API.
    
19. Unit Testing: Understand the importance of unit testing and how to write unit tests for controllers and services.
    
20. Error Handling: Know how to implement global error handling and custom error pages.
    
21. Deployment: Understand the deployment process for ASP.NET MVC applications.
    
22. Authentication and Authorization: Know how to implement different types of authentication and authorization mechanisms in ASP.NET MVC.
    
23. Performance Optimization: Understand common techniques for optimizing the performance of ASP.NET MVC applications.
    
24. Security: Know how to handle security concerns and prevent common vulnerabilities like SQL injection and Cross-Site Scripting (XSS).
    
25. Session and Caching: Understand how to manage session state and implement caching for improved performance.
    
26. jQuery and AJAX: Know how to use jQuery and AJAX to enhance the user experience in ASP.NET MVC applications.
    
27. Cross-Origin Resource Sharing (CORS): Understand how to enable cross-origin requests in ASP.NET MVC Web API.
    
28. Entity Framework: Know how to use Entity Framework for data access and mapping data models to the database.
    
29. LINQ: Understand how to use LINQ (Language Integrated Query) for querying data.
    
30. Async and Await: Know how to use async and await to handle asynchronous operations in ASP.NET MVC.
