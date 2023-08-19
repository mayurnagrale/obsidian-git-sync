
using system
public class Dependancy{
	
	public void printMessage(){
		Console.WriteLine("Im dependancy here");
	}
	
}

public class DependantClass{
	private __dependacy;
	public DependantClass(Dependancy dependancy){
		_dependacy = dependancy;
	}
	
	public void doSomething(){
		_dependacy.printMessage();
	}
}


public class program{
	public void main(){
		Dependancy dependancy = new Dependancy();
		
		DependantClass dependant = new DependantClass(dependancy);
		
		dependant.doSomething();
		
	}
}



[[Dependency Injection In Angular]]
[[Dependency Injection In Asp.net]]





