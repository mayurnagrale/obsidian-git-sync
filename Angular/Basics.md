
**Ng directive** : 
- its a class that are used to extend the behavior of html elements
- directive are used to manipulate Dom elements, add event handlers , apply style , and to create reusable components
- three types of directive 1.component directive 2.attribute directive 3.structural directive 
- component directive @component
- attribute directive : to change the existing behavior of Dom elements @directive
- to change the structure of the Dom element 

**Default directive in angular**:
- ngIf: Conditionally adds or removes elements from the DOM based on a given expression. 
           ex. *ngIf="showContent"
- ngFor: Iterates over a collection and generates elements for each item.
- ngSwitch: Conditionally renders elements based on multiple cases.
- ngClass: Adds or removes CSS classes based on conditions. ex.[ngClass]="{'highlight': isHighlighted, 'italic': isItalic}".
- ngStyle: Dynamically applies inline styles based on conditions. ex.[ngStyle]="{'color': textColor, 'font-size.px': fontSize}".
- ngModel: Binds input, select, and textarea elements to a component property for two-way data binding. ex.<input [(ngModel)]="username" placeholder="Username">.
- ngSubmit: Binds to the submit event of a form element and triggers a function in the component.
   ex 	<form (ngSubmit)="submitForm()">
					<!-- form controls -->
					<button type="submit">Submit</button>
					</form>
- ngNonBindable: Prevents Angular from processing or interpreting the contents of an element.
- Custom directive: [[Custom Directive Example]]

**Ngmodule** :
- Its a decorator used to define a module in angular application
- when we define module with ngmodule it provides some properties such as declareation, import,providers,bootstrap
- Declaration - (specify component,directive and pipes) , 
- Import - (to import other module ex. commonmodule), 
- Providers - (to register services and other providers at module level
- Bootstrap - (specify the root component of the application)
- by defining NgModule we can control the compilation and runtime behavior of ang app ,manage dependancy and promote modular development/

**AppModule** :
- it serves as root module for angular application and responsible for bootstraping the application, loading the other modules as needed.

**Filters & Pipes** :
- filters has been replaced with pipes in angular
- we use pipes to transform and format the data in our angular template 
- it can be use to filter, sort, data format dates and currency and perform custom transformation
- Pipes examples [[Pipes Examples]]


**Promise and Observable** : 
Both are use for handling asynchronus operation and manage the flow of data
	Observable: we need to subscribe (chart, data update every second)
				Emit multiple values over a period of time.
	Promise: Emit a single value at a time.(grid data refreshing it manually to get the updates data