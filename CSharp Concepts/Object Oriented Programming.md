**Composition and Aggregation**
1. These are terms that describe different ways in which objects can be related to each other.
2. These terms are used to define the nature of the relationship between objects and how their lifetimes are managed.
3. Composition: Composition represents a strong "whole-part" relationship between objects, where one object contains other objects as its parts.
4. Example of composition [[Composition in oop]]
5. Aggregation: Aggregation represents a "has-a" relationship between objects, where one object contains or references another object, but the contained object can exist independently.
6. Example of aggregation [[Aggregation in oop]]

**Static classes** :
1. Cannot Be Instantiated: this prevents you from creating objects of the class.
2. Cannot Have Instance Members: Static classes cannot contain instance members such as instance fields, properties, or methods that require an instance of the class to operate.
3. Can Only Contain Static Members: Static classes can only contain static members, including static methods, static properties, and static fields. These members can be accessed using the class name itself, without needing an instance.
4. Sealed by Default: A static class is implicitly `sealed`, which means you cannot derive a class from it. In other words, you cannot create a subclass that inherits from a static class.
5. [[Static class example]]


**Object Oriented Programming**
- Object replicate real word entity, key concept ( classes, objects, encapsulation, inheritance, polymorphism, abstraction) manage and maintain complex system promotes reuse enhance readability.
- Allows modeling of real word entities and their relationship in more intuitive manner.

**Abstraction and Encapsulation** :
- **Abstraction** is the process of hiding the implementation details of an object or system from the user. This allows the user to focus on the essential features of the object without having to worry about how it works.

- **Encapsulation** is the binding together of data and the methods that operate on that data. This means that the data and its associated methods are kept together in a single unit, called an object. The data in an object can only be accessed through the object's methods, which helps to protect the data from unauthorized access

The main difference between abstraction and encapsulation is that abstraction deals with hiding the implementation details of an object, while encapsulation deals with hiding the data in an object. Abstraction is typically used to hide the complexity of an object, while encapsulation is typically used to protect the data in an object.

- Abstraction is often implemented using abstract classes and interfaces.
- Encapsulation is often implemented using access modifiers, such as private, protected, and public.
- Abstraction and encapsulation are complementary concepts. They can be used together to create objects that are both easy to use and secure.

**Abstract class and Interfaces** :
- Abstract class : 
	 1. Should have at least  one abstract method 
	 2. When we know partial requirements but commonly used functionalities
	 3. Whatever methods are defined does not have to be implemented
	 4. Can have access modifiers or it can be static
- Interfaces :
	1.  Set of abstract methods and properties
	2.  data members do not have access modifiers by default it is public static and final
	3.  A class can implement one or more interfaces, and it must provide implementation for all  the methods and properties 
	4.  whatever methods declared in interfaces must be implemented in its derived class 
	5.  when we know the requirements but we don't know the implementation

**Method Overloading and Method Overriding**
- Method overloading: 
1. Ability to define multiple methods in the same class with the same name but different parameter lists.
2. Different Parameter Lists: differ in the number of parameters ex.[[Different Parameter Lists]]
3. Different Parameter Types: differ in the types of parameters they accept ex.[[Different Parameter Types]]
4. Different Return Types: The return type alone cannot be used to distinguish between overloaded methods. 
5. Is this a example of method overloading or it will give error ? 
	``` 
	void Add(int a, int b)
	{
	}
	void Add(ref int a, ref int b)
	{
	}
	```
	
	Yes its an example of method overloading, as we are passing int a and int b with pass by reference its an example of method overloading

- Method Overriding:
6. Allows a derived class to provide a specific implementation for a method that is already defined in its base class.
7. The overridden method in the derived class should have the same method signature (method name, return type, and parameters) as the method in the base class.
8. Method overriding example: [[Method Overriding Example]]





**Type of constructor**
1. Default Constructor
2. Parameterized Constructor
3. Copy Constructor

copy constructor-
class a{
	name:
	age:
	
	a(string name,int age){
		name=this.name;
		age=this.age;
	}
	
	a(a obj){
		name = obj.name;
		age = obj.age;
	}
}

Interfaces
public class SampleClass : IControl, ISurface
{
    void IControl.Paint()
    {
        System.Console.WriteLine("IControl.Paint");
    }
    void ISurface.Paint()
    {
        System.Console.WriteLine("ISurface.Paint");
    }
}

**Passing a Reference vs. Value**
-reference to data stored in memory(heap)
-Objects are an example of a reference type

Can we make a obj of abstract class?
No, we can't create an object of an abstract class. But we can create a reference variable of an abstract class.
The reference variable is used to refer to the objects of derived classes (subclasses of abstract class).