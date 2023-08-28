**Lazy Loading** :
- In c# we often use lazy loading to defer the initialization of the object or data until it is needed.
- this is useful when we are dealing with large dataset or expensive resource.
- The `Lazy<T>` class in C# provides a straightforward way to implement lazy loading.

**Eager Loading** :
- Eager loading is a technique in software development that loads all related data when you load a particular object. This can be done to improve performance by reducing the number of queries that need to be executed.
- var customers = context.Customers.Include(c => c.Orders); 

**Read-only and Constant** :
	Constant - define at the time of compilation, we need to pass the value to the constant at the time of define.
	Read-only - passing value at definition not necessarily needed. we can call this as run time variable as we can pass value later?
	
**Static class** :
- It contains only static members such as methods properties and fields 
- There members can be access directly with class name without creating object of the class
- we cant create object of static class
**Static** :
- Static data members -one copy is provided to the entire solution
- Static classes - we cant create object of an static class it can be directly access using its class name and it will have all the data members static inside it.
- static data members and static function/methods can be using the name of the class without creating the object of the class also we can make class private constructor to avoid 
  object creation outside the class 

**Linq** 
- to write query on different source of data such as datasource, collection(list) , xml docs also to preforms some operation such as filtering sorting  grouping joining aggregation
- var query_Result = from item in dataSource
                  where item.Property == someValue
                  orderby item.OtherProperty
                  select item;

**Lambda Expression** 
- Inline expression (parameter)=>expression :define small makes code more readable and maintainable
- Fun<int, int> square = x => x * x;

**Delegates** 
 - Treats method as a entity and pass it to some variable, encapsulation over events
 - delegates are object that encapsulate method
 - delegates are used to connect events with event handler
 
**Events** :
- An event is a notification that something has happened 
- Ex. A button click event is a notification that a button has been clicked.
- An event handler is a method that is called when an event occurs. 
- Ex. A button click event is a method that is called when a button is clicked.
[[Button click event handler]]


**Keywords for classes and methods** :

#Virtual - to let it override , we define methods as virtual if we want to let it modify by child or derived class
#Override- we use this concept when we are modifying the existing functionality of the base class from child class
#Sealed - to restrict it for overriding for method , to restrict class from inheritance 
#Abstract -method should be implemented by derived classes
#new - to hide base class method from derived class
#partial - we can write methods in two different classes with same name, at runtime it will be treated as one single method
type of constructor - parameterized and non parameterized and copy constructor
#private_constructor - to restrict the object creation outside the class
#static_constructor - is get called when the object is created for the first time
#boxing and #unboxing - type conversion from small to large and vice-versa
boxing: value type to object type
#parsing -conversion of data type


**Difference between reference type and value type** :
- **Reference types** are objects that store a reference to the actual data. When you pass a reference type to a method, you are passing the reference itself, not the actual data. This means that any changes made to the data in the method will be reflected in the original variable.

- **Value types** are primitive types that store the actual data. When you pass a value type to a method, you are passing the actual data itself, not a reference to it. This means that any changes made to the data in the method will not be reflected in the original variable.

**Difference between ref and out parameter** :
	ref- enable two-way communication between the calling code and the method.
			- When using ref, the variable passed as a parameter must be initialized before calling the method; otherwise, a compilation error will occur When using ref, 
			the variable passed as a parameter must be initialized before calling the method; 
			otherwise, a compilation error will occur
	out- The primary purpose of out parameters is to allow a method to return multiple values
	
#Using -to ensure that object is properly disposed of after leaving the using block

**Asynchronous Programming** : 
Async - to execute task before completing the previous one in thread
Await - to wait current task to be executed before completing the previous one

Difference between asynchronous synchronous and multithreading
synchronous programming follows a sequential execution model, asynchronous programming allows tasks to execute independently without blocking, 
and multithreading involves running multiple threads simultaneously, which can be used to implement both synchronous and asynchronous behavior.

**Threads and Tasks** :
- Threads : part of os
- Tasks: part of the framework

**Dependency Injection** :
1. **Dependencies**: In an application, you have various classes and components that depend on each other to perform tasks. These dependencies are typically other classes or services that a component needs to function correctly.
    
2. **Injection**: Instead of creating these dependencies within a class, you "inject" them from the outside. This can be done via constructor injection, property injection, or method injection.

**Define life time of the object** : 
Singleton - Caching and shared services - one instance is created and shared thought the application
scope -  repository for the same transaction - one instance is created and shared thought the scope
transient - instance should not affect each other + thread safety - every time it is requested it will create a new instance 

**Extension Method** :
	Helps you to add new method to existing type without modifying the existing code, and without any inheritance and aggregation
	
**Why do we need getters and setters?**
 - to have more control over attributes, suppose if we want to add some restriction like which value should we pass we use set inside the setter 

- #Reflections - used for obtaining the type information at runtime 

- Arrays: fixed side, same type elements only(type oriented)
- List<T>: dynamic array , can grow n shrink its size in runtime.





 