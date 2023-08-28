Difference between Asp.net and Asp.net core
- Asp.net core is a improved version with richer functionality more comfortable, more libraries, and some other distinction.
- Asp.net core support cross platform application and can run on macOS, Linux, Windows but Asp.net application will run on windows OS only. 

Value Objects:
Type Safety
Immutability
Encapsulation
Structural integrity

Primitive obsession

Life Cycle in MVC
Application Life Cycle :

Initialization : 
Application start ->Initializes MVC framework-> instance of the model view and controller will be created
User Interaction -> Interaction can in the form of button clicking, entering input or any other form of interacting with UI 
Controller Handling: View the forward input or events to controller -> controller decide to take action based on current state of Model and input 
Model update: changes in model then get updated into view
View Update: view gets the updated data from the model and present it
Termination: when user exit the application.


Request Life Cycle:
Request-> Routing ->Controller Initialization -> Action Execution -> 
Result Execution -> Response 

Middleware in mvc : 
Allow us to perform various task before processing the request to controller or after the response 
Request Middleware -> performs task like (logging , validation authentication etc)
Controller Action Execution -> 
Response Middleware -> it performs task like modifying the response, setting headers, 

- **Authentication and Authorization:** Middleware can check if a user is authenticated and authorized to access a specific route or resource. If not, it can redirect them to a login page or return an error.
    
- **Logging:** Middleware can log requests, responses, and other relevant information for debugging and auditing purposes.
    
- **Input Validation:** Middleware can validate incoming request data to ensure it meets certain criteria before it reaches the controller action method.
    
- **Caching:** Middleware can implement caching mechanisms to improve performance by serving cached responses instead of processing requests repeatedly.
    
- **Compression:** Middleware can compress response data before sending it to the client to reduce bandwidth usage and improve load times.
    
- **Error Handling:** Middleware can catch and handle exceptions or errors that occur during request processing, providing custom error pages or responses.
    
- **Content-Type Negotiation:** Middleware can negotiate the content type of the response based on the client's preferences, such as JSON or HTML.
    
- **Routing:** In some cases, routing itself can be implemented as middleware, directing requests to the appropriate controller action based on URL patterns.


**Difference between Tempdata and Viewbag** :
Viewbag : 
- Valid for only one http req
- Can store any type of data doest not get typechecked at runtime
- ex. to send some message in view.

Tempdata : 
- Not limited to single request
- **Usage**: `TempData` is commonly used when you need to pass data from one action to another action (typically after a redirection) within the same session.
- For example, you might use `TempData` to store data temporarily during a form submission, then retrieve and display it on a confirmation page.

**Resource Files in Dotnet** :
In .NET, a resource file is a file that contains non-executable data that is used by your application. This data can include strings, images, icons, and other binary data. Resource files are typically used to localize your application, i.e. to make it available in multiple languages.

Resource files can be stored in a variety of formats, including XML, binary, and JSON. The most common format for resource files in .NET is XML. XML resource files are called .resx files.