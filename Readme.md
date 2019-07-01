# Interview Questions for FSD: 
-------------------
## FrontEnd:
-------------------

## Angular:

### 1. What are the Building blocks of Angular?

**Answer:**
1. Modules: An angular module is set of angular basic building blocks like component, directives, services etc. 
   An application is divided into logical pieces and each piece of code is called as "module" which perform a single task.
2. Component: These are the basic building blocks of angular application to control HTML views.
3. Template: This represent the views of an Angular application.
4. Directives: Directives add behaviour to an existing DOM element or an existing component instance.
5. Data Binding: The mechanism by which parts of a template coordinates with parts of a component is known as data binding.
6. Services: It is used to create components which can be shared across the entire application.
7. Metadata: This can be used to add more data to an Angular class.
8. Dependency Injection:Angular makes use of DI to provide required dependencies(Services) to new components.
9. Routing: An Angular router is responsible for interpreting a browser URL as an instruction to navigate to a client-generated view. 

### 2. What are the Types of Directives in Angular?

**Answer:** 
Directives add behaviour to an existing DOM element or an existing component instance.
 - Attribute Directive - ngClass, ngStyle
 - Stuctural Directive - ngIf, ngFor, ngSwitch
 - Custom Directive - DropDown, Highlighter

### 3. What are the advantages of Angular over any other frontend framework?

**Answer:**
AngularJS supports MVC pattern
Can do two ways data binding using AngularJS
It has per-defined form validations
It supports both client server communication
It supports animations
AngularJS uses dependency injection and make use of separation of concerns.
AngularJS provides reusable components.

### 4. What is the difference between @inject and @injectable?

**Answer:**
@Injectable() : Lets Angular know that a class can be used with the dependency injector.
@Inject() : Manual mechanism for letting Angular know that a parameter must be injected.

### 5. What is Bootstraping?

**Answer:**
To implement AngularJS in your web pages, you need to bootstrap the HTML document. 
Bootstrapping involves two parts. The first part is to define the application module by using the ng-app directive, 
and the second is to load the angular.js library in a <script> tag

### 6. What is Transpiling in Angular?

**Answer:**
Transpiling is the process of converting the typescript into javascript. 
Though typescript is used to write code in the Angular applications, the code is internally transpiled into javascript.


### 7. What is AOT (Ahead of Time) in Angular?

**Answer:**
The angular compiler takes typescript code, compiles it and produces javascript code again but during the compile time. 
Ahead-of-Time Compilation does not happen every time or for every user, as is the case with Just-In-Time (JIT) Compilation where compilation happens during runtime. 
ng build --aot
ng serve --aot

### 8. How do we send the property value from Parent to Child and vice versa in Angular?

**Answer:**
When it comes to the communication of Angular Components, which are in Parent-Child Relationship; 
we use @Input in Child Component when we are passing data from Parent to Child Component 
and @Output is used in Child Component to receive an event from Child to Parent Component. 

### 9. What is String interpolation in Angular?

**Answer:**
{{variableName}}, here the ‘variableName’ is actually typescript (component) data representing its value on the template

### 10. What is DataBinding in Angular?

**Answer:**
Data binding can be done in 3 ways: https://alligator.io/angular/data-binding-angular/

(0) Interpolation -  Name: {{ user.name }}
(i) Property Binding - [value]="user.email"
(ii) Event Binding - (click)="cookBacon()"
(iii) Two-Way Data Binding. - [(ngModel)]="user.email"

### 11. What is Component in Angular Terminology?

**Answer:**
A Component is basically a block in which the data can be displayed on HTML using some logic usually written in typescript. 

### 12. Differentiate between Observables and Promises?

**Answer:**
Observaleble: this.http.get(`https://www.amazon.com`).subscribe((data: any) => {
Promise: this.http.get(`https://www.amazon.com`).toPromise().then((data: any) => {

Observables are lazy, which means nothing happens until a subscription is made. 
Whereas Promises are eager; which means as soon as a promise is created, the execution takes place. 

Observable is a stream in which multiple events is possible and the callback is called for each event. 
Whereas, promise handles a single event.

Observables can be cancelled upon requests.
Promises cannot be cancelled upon requests.

### 13. Define Subscribe in Angular?

**Answer:**
It is a method which is subscribed to an observable. Whenever subscribe method is called, independent execution of observable happens.  
this.http.get(`https://www.amazon.com`).subscribe((data: any) => {

### 14. Explain Sequence of Angular Lifecycle Hooks?

**Answer:**
OnChanges: When the value of a data bound property changes, then this method is called.
OnInit: This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens.
DoCheck: This is for the detection and to act on changes that Angular can't or won't detect on its own.
AfterContentInit: This is called after Angular projects external content into the component's view.
AfterContentChecked: This is called after Angular checks the content projected into the component.
AfterViewInit: This is called after Angular initializes the component's views and child views.
AfterViewChecked: This is called after Angular checks the component's views and child views.
OnDestroy: This is the cleanup phase just before Angular destroys the directive/component.

### 15. What are Angular CLI commands?

**Answer:**
npm install -g @angular/cli
ng new my-first-project
cd my-first-project
ng serve
ng generate <filename>

--------------------

## ReactJs:

### 1. How React works? How Virtual-DOM works in React?
**Answer:**
React creates a virtual DOM. When state changes in a component it firstly runs a “diffing” algorithm, 
which identifies what has changed in the virtual DOM. The second step is reconciliation, 
where it updates the DOM with the results of diff.

### 2. What is JSX?

**Answer:**
JSX is a syntax extension to JavaScript and comes with the full power of JavaScript. 
JSX produces React “elements”. You can embed any JavaScript expression in JSX by wrapping it in curly braces. 
After compilation, JSX expressions become regular JavaScript objects.

### 3. What is the difference between state and props?

**Answer:**
The state is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.
Props (short for properties) are a Component’s configuration. Props are how components talk to each other. 
They are received from above component and immutable as far as the Component receiving them is concerned. 
A Component cannot change its props, but it is responsible for putting together the props of its child Components. 
Props do not have to just be data — callback functions may be passed in as props.

### 4. Explain the components of Redux.

**Answer:**
Redux is composed of the following components:
Action — Actions are payloads of information that send data from our application to our store. They are the only source of information for the store. We send them to the store using store.dispatch(). Primarly, they are just an object describes what happened in our app.
Reducer — Reducers specify how the application’s state changes in response to actions sent to the store. Remember that actions only describe what happened, but don’t describe how the application’s state changes. So this place determines how state will change to an action.
Store — The Store is the object that brings Action and Reducer together. The store has the following responsibilities: Holds application state; Allows access to state via getState(); Allows state to be updated via dispatch(action); Registers listeners via subscribe(listener).

### 5. What are the features of React? 

**Answer:**
Major features of React are listed below:

It uses the virtual DOM instead of the real DOM.
It uses server-side rendering.
It follows uni-directional data flow or data binding.

### 6. List some of the major advantages of React?

**Answer:**
Some of the major advantages of React are:

It increases the application’s performance
It can be conveniently used on the client as well as server side
Because of JSX, code’s readability increases
React is easy to integrate with other frameworks like Meteor, Angular, etc
Using React, writing UI test cases become extremely easy

### 7. What are the limitations of React?

**Answer:**
Limitations of React are listed below:

React is just a library, not a full-blown framework
Its library is very large and takes time to understand
It can be little difficult for the novice programmers to understand
Coding gets complex as it uses inline templating and JSX

### 8. What is Props?

**Answer:**
Props is the shorthand for Properties in React. They are read-only components which must be kept pure i.e. immutable. 

### 9. Is it possible to send Props from child to parent component?

**Answer:**
Props are always passed down from the parent to the child components throughout the application. 
A child component can never send a prop back to the parent component. 
This help in maintaining the unidirectional data flow and are generally used to render the dynamically generated data.

### 10. What is a state in React and how is it used?

**Answer:**
States are the heart of React components. States are the source of data and must be kept as simple as possible. 
Basically, states are the objects which determine components rendering and behavior. 
They are mutable unlike the props and create dynamic and interactive components. They are accessed via this.state().

### 11. What are the different phases of React component’s lifecycle?

**Answer:**
There are three different phases of React component’s lifecycle:

Initial Rendering Phase: This is the phase when the component is about to start its life journey and make its way to the DOM.
Updating Phase: Once the component gets added to the DOM, it can potentially update and re-render only when a prop or state change occurs. That happens only in this phase.
Unmounting Phase: This is the final phase of a component’s life cycle in which the component is destroyed and removed from the DOM.

### 12. Explain the lifecycle methods of React components in detail.

**Answer:**
Some of the most important lifecycle methods are:

componentWillMount() – Executed just before rendering takes place both on the client as well as server-side.
componentDidMount() – Executed on the client side only after the first render.
componentWillReceiveProps() – Invoked as soon as the props are received from the parent class and before another render is called.
shouldComponentUpdate() – Returns true or false value based on certain conditions. If you want your component to update, return true else return false. By default, it returns false.
componentWillUpdate() – Called just before rendering takes place in the DOM.
componentDidUpdate() – Called immediately after rendering takes place.
componentWillUnmount() – Called after the component is unmounted from the DOM. It is used to clear up the memory spaces.

### 13. What is an event in React?

**Answer:**
In React, events are the triggered reactions to specific actions like mouse hover, mouse click, key press, etc. 
Handling these events are similar to handling events in DOM elements.

### 14. What do you understand by refs in React?

**Answer:**
Refs is the short hand for References in React. It is an attribute which helps to store a reference to a particular 
React element or component, which will be returned by the components render configuration function. 
It is used to return references to a particular element or component returned by render(). 

-------------------------

## BackEnd:

## SpringBoot:

### 1. What is Spring boot?

**Answer:**
Spring Boot makes it easier for you to create production ready applications in no time. It is an opinionated view to create Spring application quickly. It follows convention over configuration. In simple terms, it comes with default configurations for most of the Spring projects, you don’t need to do much to bootstrap any spring application.

### 2. Why did you use Spring boot in your application?

**Answer:**
As discussed earlier, Spring boot makes it easier for you to create Spring application, it can save a lot of time and efforts.

### 3. Can you list advantages of Spring boot?

**Answer:**
Advantages of Spring boot are:

It provides a lot of default configurations which help you to create Spring application faster.
It comes with embedded tomcat or jetty server, so you don’t have to deploy jar.
It reduces development code by avoiding a lot of boilerplate code.
It increases productivity as you can create Spring application quickly.
It provides a lot of starter project for easy maven integration.You don’t have to worry about version mismatch.
You can quickly create using sample project using spring boot initializer

### 4. What are disadvantages of Spring boot?

**Answer:**
If you want to convert your old spring application to Spring boot application, it may not be straight forward and can be time consuming.

### 5. How can you override default properties in Spring boot Project?

**Answer:**
Spring boot provides a lot of properties which can be overridden by specifying them in application.properties.

### 6. How can you run Spring boot application on custom port?

**Answer:**
You can simply put server.port properties in application.properties.

For example:server.port=8050

### 7. What is Spring boot starter and how it is useful?

**Answer:**
Spring boot comes with a lot of starters which is set of convenient dependency descriptors which you can include in your pom.xml.

### 8. What is name of the configuration file which you use in Spring boot?

**Answer:**
Configuration file used in Spring boot projects is application.properties. 
It is very important file as it is used to override all default configurations.

### 10. What is actuator in Spring boot?

**Answer:**
Spring boot actuator is one of the most important features of Spring boot. 
It is used to access current state of running application in production environment. 
There are various metrics which you can use to check current state of the application.

### 11. What is @SpringBootApplication annotation in Spring boot project?

**Answer:**
@SpringBootApplication annotation is the combination of the below mentioned annotations

@Configuration
@EnableAutoConfiguration
@ComponentScan

### 12. What is dependency injection in SpringBoot?

**Answer:**
When you try to initialize an object of class A to class B you use @Autowire annotation

@Autowired
This annotation is applied on fields, setter methods, and constructors. The @Autowired annotation injects object dependency implicitly.
When you use @Autowired on fields and pass the values for the fields using the property name, Spring will automatically assign the fields with the passed values.
You can even use @Autowired  on private properties, as shown below. (This is a very poor practice though!)

### 13. What is DevTools in Spring boot?

**Answer:**
No need to redeploy your application every time you make the changes.Developer can simply reload the changes without restart of the server.
It avoids pain of redeploying application every time when you make any change. 

### 14. What is @ComponentScan annotation?

**Answer:**
@ComponentScan
This annotation is used with @Configuration annotation to allow Spring to know the packages to scan for annotated components.
@ComponentScan is also used to specify base packages using basePackageClasses or basePackage attributes to scan. 
if specific packages are not defined, scanning will occur from the package of the class that declares this annotation.

### 15. Ask common annotations in SpringBoot?

**Answer:**
@Component
This annotation is used on classes to indicate a Spring component. The @Component annotation marks the Java class as a bean or say component so that the component-scanning mechanism of Spring can add into the application context.

@Controller
The @Controller  annotation is used to indicate the class is a Spring controller. This annotation can be used to identify controllers for Spring MVC or Spring WebFlux.

@Service
This annotation is used on a class. The @Service marks a Java class that performs some service, such as execute business logic, perform calculations and call external APIs. This annotation is a specialized form of the @Component annotation intended to be used in the service layer.

@Repository
This annotation is used on Java classes which directly access the database. The @Repository annotation works as marker for any class that fulfills the role of repository or Data Access Object.

@EnableAutoConfiguration
This annotation is usually placed on the main application class. The @EnableAutoConfiguration annotation implicitly defines a base “search package”. This annotation tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings.

-----------------

## Core Java:

### 1. What is constructor in java?

**Answer:**
Constructor can be considered a special code which is used to initiaze objects.
It has two main points:

Class and Constuctor name should match
Constructor should not have any return type else it will be same as method.

### 2. Can we declare constructor as final?

**Answer:**
No, Constructor can not be declared as final. If you do so, you will get compile time error.

### 3. What are access modifier available in java?

**Answer:**
It Specifies accessibility of variables, methods , constructor of class.
There are four access modifier in java
Private : Accessible only to the class.
Default : Accessible in the package.
Protected : Accessible in the packages and its subclasses.
Public : Accessible everywhere

### 4. What is difference between Abstract class and interface?

**Answer:**
Abstract class can have both Abstract and Non Abstract methods, however interface can have only Abstract methods

### 5. Can one interface implement another interface in java?

**Answer:**
No, One interface can not implement another interface. It can extend it using extends keyword.

### 6. What is marker interface?

**Answer:**
Marker interfaces are interfaces which have no method but it is used to indicate JVM to behave specially when any class implement these interfaces.
For example : If you implement cloneable interface and then call .clone method of object, it will clone your object. If you do not implement cloneable interface, it will throw cloneNotSupported exception.

### 7. What is method overloading and method overriding in java?

**Answer:**
Method overloading : Method overloading is concept that allows a class to have same method name but diferent method arguments. Method overloading is also known as compile time polymorphism.

Method overriding : If child class contain same method as parent class with same method signature. This is called method overriding. Method overriding is also known as dynamic polymorphism.

### 8. Can you override static methods in Java?

**Answer:**
No, you can not override static methods in Java. You can create same method in child class but it won’t be dynamic polymorphism. It will be method hiding. Static methods belong at class level not at object level hence you can not override static method.

### 9. Can you override private methods in Java?

**Answer:**
No, you can not override private methods in Java. 
Private methods are not visible to subclass, hence you can not override private method but you can hide it.

### 10. Define Lifecycle of Thread?

**Answer:**
New : When you create a thread object and it is not alive yet.
Runnable:  When you call start method of thread, it goes into Runnable state. Whether it will execute immediately or execute after some times , depends on thread scheduler.
Running : When thread is being executed, it goes to running state.
Blocked : When thread waits for some resources or some other thread to complete (due to thread’s join), it goes to blocked state.
Dead: When thread’s run method returns, thread goes to dead state.

### 11. Can we start a thread twice in java?

**Answer:**
No, Once you have started a thread, it can not be started again. 
If you try to start thread again , it will throw IllegalThreadStateException.

### 12. What is garbage Collection?

**Answer:**
Garbage Collection is a process of looking at heap memory and deleting unused object present in heap memory. 
Garbage Collection frees unused memory. Garbage Collection is done by JVM.

### 13. What is use of finalize() method in object class?

**Answer:**
Finalize method get called when object is being collected by Garbage Collector. This method can be used to write clean code before object is collected by Garbage Collector.

### 14.What is difference between final, finally and finalize in Java?

**Answer:**
final : Final is a keyword which is used with class to avoid being extended, with instance variable so they can not reassigned, with methods so that they can not be overridden.
finally : Finally is a keyword used with try, catch and finally blocks. Finally block executes even if there is an exception. It is generally used to do some clean up work.
finalize :  Finalize is a method is used to invoke garbage collection for clean up unreachable object.