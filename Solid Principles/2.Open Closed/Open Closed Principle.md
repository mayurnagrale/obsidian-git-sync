Class should open for extension and closed for modification.

Modification means changing the existing code and extension means adding new functionality.
So we should be able to add new functionality without touching the existing code.

This is because when we touch the existing code we are taking the risk of creating a potential bugs. also we need regression testing on that which can be costly.

It is usually done with the help of abstract class and interfaces.

Lets take an example of exporting data from different part of our application such as grid, report etc.
now we want it to export it in excel from grid and for report we want it in pdf or word file. also sometimes we want grid data in pdf table or csv.

so if we know that this export method is going to be needed at different places. so we should create an interface add export method to it passing so data in parameter and extend that interface in our following class. 
other wise we can implement the logic in abstract class with passing the parameter of file type and use this method in its derived class.
