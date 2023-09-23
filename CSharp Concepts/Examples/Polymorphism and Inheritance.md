public class DemoParent {
  int _count;
  public DemoParent(int count) {
    _count = count;
    Console.WriteLine($"DemoParent Ctor Called - {_count}");
  }
  public virtual void Run01() => Console.WriteLine("DemoParent.Run01 Method");
  public void Display() => Console.WriteLine("DemoParent.Display Method");
  public void DisplayParent() => Console.WriteLine("DemoParent.DisplayParent Method");
}

public class DemoChild01 : DemoParent {
  public DemoChild01(int count) : base(count) => Console.WriteLine($"DemoChild01 Ctor called - {count}");
  public override void Run01() => Console.WriteLine("DemoChild01.Run01 Method");
  public void Display() => Console.WriteLine("DemoChild01.Display Method");
  public void DisplayChild() => Console.WriteLine("DemoChild01.DisplayChild Method");
}



If we want to call base class method using child class object then
we will update method child class using base: methodname() 

public Display(){
	base.Display(); <- this will call the base class method
	cw("child class method")
}

When we create object of child class
DemoChild01 dmcObj = new DemoChild01();
This will call the the constructor of child class and parent class
public DemoChild01(int count) : base(count) because of this line 

and from parent class constructor 
	DemoParent Ctor Called - 0
	DemoParent Ctor Called - 10
and the from child class constructor
	DemoChild01 Ctor called - 10



dmcObj.Display();

Can we access parent class method using child class object in c#?
No. We have to call parent class method inside child class method using base.ParentClassMethod() then we to call this child class method using child class object 

public class DemoParent
{
    public virtual void Run()
    {
        Console.WriteLine("DemoParent.Run() Method");
    }
}

public class DemoChild : DemoParent
{
    public override void Run()
    {
        Console.WriteLine("DemoChild.Run() Method");
        // Call the parent class Run() method
        base.Run();
    }
}


