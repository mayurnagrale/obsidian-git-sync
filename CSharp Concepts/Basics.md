**Read-only and Constant**
	Constant - define at the time of compilation, we need to pass the value to the constant at the time of define.
	Read-only - passing value at definition not necessarily needed. we can call this as run time variable as we can pass value later
	
**Static class** 
- It contains only static members such as methods properties and fields 
- There members can be access directly with class name without creating object of the class
- we cant create object of static class

**Linq** 
- to write query on different source of data such as datasource, collection(list) , xml docs also to perfoms some operation such as filtering sorting  grouping joining aggrigation
- var queryResult = from item in dataSource
                  where item.Property == someValue
                  orderby item.OtherProperty
                  select item;

**Lambda Expression** 
- Inline expression (parameter)=>expression :define small makes code more readable and maintainable
- Func<int, int> square = x => x * x;

**Delegates** 
 - treat method as a entity and pass it to some variable, encapsulation over events

static data mambers -one copy is provided to the entire solution
static classes - we cant create object of an static class it can be directly access using its class name and it will have all the data members static inside it.
static data members and static function/methods can be using the name of the class without creating the object of the class also we can make class private constructor to avoid 
object creation outside the class 

virtual - to let it override , we define methods as virtual if we want to let it modify by child or derived class
override- we use this concept when we are modifying the existing functionality of the base class from child class
sealed - to restrict it for overriding for method , to restrict class from inheritance 
Abstract -method should be implemented by derived classes
new - to hide base class method from derived class
partial - we can write methods in two different classes with same name, at runtime it will be treated as one single method
type of constructor - parameterised and non parameterised and copy constructor
private constructor - to restrict the object creation outside the class

boxing and unboxing - type conversion from small to large and viceversa
boxing:value type to object type

parsing -converion of data type

Arrays: fixed side, same type elements only(type oriented)
List<T>: dynamic array , can grow n shrink its size in runtime

Difference between referance type and value type:

Difference between ref and out parameter
	ref- enable two-way communication between the calling code and the method.
			-When using ref, the variable passed as a parameter must be initialized before calling the method; otherwise, a compilation error will occurWhen using ref, 
			the variable passed as a parameter must be initialized before calling the method; 
			otherwise, a compilation error will occur
	out- The primary purpose of out parameters is to allow a method to return multiple values
	
Using -to ensure that object is properly disposed of after leaving the using block

Asynchronus Programming 
Async - to execute task before completing the previous one in thread
Await - to wait current task to be executed before completing the previous one

Difference between asynchronous synchronous and multithreading
synchronous programming follows a sequential execution model, asynchronous programming allows tasks to execute independently without blocking, 
and multithreading involves running multiple threads simultaneously, which can be used to implement both synchronous and asynchronous behavior.

Dependancy Injuction
Define life time of the object
Singleton - Caching and shared services - one instance is created and shared throught the application
scope -  repository for the same transaction - one instance is created and shared throught the scope
transient - instance should not affect each other + thread safety - every time it is requested it will create a new instance 

Extenstion methods 
	Helps you to add new method to existing type without modifying the existing code, and without any inheritance and aggrigation
	
Why do we need getters and setters?
 to have more control over attributes, suppose if we want to add some restriction like which value should we pass we use set inside the setter 

Reflections - used for obtaining the type information at runtime 