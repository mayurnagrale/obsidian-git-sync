
**Ng directive** : 
- Its a class that are used to extend the behavior of html elements
- directive are used to manipulate Dom elements, add event handlers , apply style , and to create reusable components
- three types of directive 1.component directive 2.attribute directive 3.structural directive 
- component directive @component
- attribute directive : to change the existing behavior of Dom elements 
- structural directive :to change the structure of the Dom element 

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
Both are use for handling asynchronous operation and manage the flow of data
	Observable: we need to subscribe (chart, data update every second)
				Emit multiple values over a period of time.
	Promise: Emit a single value at a time.(grid data refreshing it manually to get the updates data

**Data Binding In Angular** :
- It is a technique to link your data to your view layer.
- There are three types of data binding in Angular:
	- **Property binding** : It  is used to bind a property in your component to an HTML element. For example, you can bind the `name` property of your component to the `value` attribute of an input element.
	- **Event binding** :It is used to bind an event in your component to an HTML element. For example, you can bind the `click` event of your component to the `onclick` attribute of an button element.
	- **Two-way binding** :It is a combination of property binding and event binding. It allows you to bind a property in your component to an HTML element and vice versa. For example, you can bind the `name` property of your component to the `value` attribute of an input element and the `input` event of the input element to the `onNameChange` event of your component.

**Data transfer between components  :**  
- **Passing data from parent to child using @Input()** : This is the simplest way to pass data from a parent component to a child component. The parent component defines an input property with the @Input() decorator, and the child component can bind to that property using property binding.
	
- **Passing data from child to parent using @Output()** : This method allows the child component to emit an event with data, which the parent component can then listen for. The child component defines an output property with the @Output() decorator, and the parent component can subscribe to that property using event binding.

- **Using services for data sharing** : Services are a great way to share data between components that are not related to each other. A service is a class that can be used to store and retrieve data. Components can inject the service into their constructor and then use it to get and set data.

- **Calling ViewChild , ViewChildren , ContentChild , and ContentChildren** : These decorators can be used to access a child component's properties or methods from the parent component. This can be useful for passing data from the parent component to the child component, or for calling methods on the child component from the parent component.


**Decorators in Angular** : 
In Angular, a **decorator** is a special function that is used to modify the behavior of a class, property, or method. Decorators are declared using the `@` symbol.

There are four main types of Angular decorators:

- **Class decorators** are used to modify the behavior of a class. For example, the `@Component` decorator is used to mark a class as an Angular component.
- **Property decorators** are used to modify the behavior of a property. For example, the `@Input` decorator is used to mark a property as an input property.
- **Method decorators** are used to modify the behavior of a method. For example, the `@HostListener` decorator is used to listen for events on the host element.
- **Parameter decorators** are used to modify the behavior of a parameter. For example, the `@Inject` decorator is used to inject a dependency into a method.

**Interceptor in Angular** :
Interceptors are a way to intercept HTTP requests and responses.
**Logging:** Logging all requests and responses.
**Error handling:** Handling errors that occur during requests.
**Authentication:** Authenticating requests before they are sent.
**Authorization:** Authorizing requests to access specific resources.
**Caching:** Caching responses to improve performance.

interceptors are implemented as classes that implement the `HttpInterceptor` interface. The `HttpInterceptor` interface defines two methods:
- `intercept(request: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>>;`
- `supports(request: HttpRequest<any>): boolean;`

**Lazy Loading :** 
- Lazy loading is a technique to delay loading of module or component until it is actually needed.
- This is helpful in improving the performance in application as we don't need to initialize those components or module which is not needed
- div ngModule="myModule"></div
- In above div module will not get loaded till we render div \
- At the start of the application we don't need to load all the routes if it the big application
- loadChildren can be a example of lazy loading 

<div ngModule="myModule"></div>

