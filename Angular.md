
## Technology Docs

- [Angular](Angular.md)  
- [MongoDB](MongoDB.md)  
- [MySQL](Mysql.md)  
- [Node.js](Node-Js.md)  
- [TypeScript](TypeScript.md)  
- [JavaScript](JavaScript.md)
  
Here is a comprehensive list of 100+ Angular interview questions and answers with code examples:

### 1. **What is Angular?**
   **Answer**: Angular is a platform and framework for building client-side applications using HTML, CSS, and TypeScript. It is a complete rewrite of AngularJS (Angular 1.x) and is designed for single-page applications (SPA).

### 2. **What are the key features of Angular?**
   **Answer**: 
   - Two-way data binding
   - Dependency injection
   - Modular architecture
   - Components-based architecture
   - Directives for DOM manipulation
   - RxJS for handling asynchronous operations
   - Routing and navigation support

### 3. **Explain the Angular Architecture.**
   **Answer**: Angular architecture is based on modules, components, services, directives, and pipes:
   - **Modules**: The basic building blocks in Angular that provide functionality and organizational structure to an application.
   - **Components**: Define the view (UI) and the logic for each part of the application.
   - **Services**: Share data and functionality across components, typically handling business logic.
   - **Directives**: Extend HTML functionality by adding behavior to elements in the DOM.
   - **Pipes**: Transform data displayed in the template.

### 4. **What is a Component in Angular?**
   **Answer**: A component is a building block of an Angular application that controls a view (HTML template). It consists of a TypeScript class, HTML template, and CSS styles.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-hello',
     template: `<h1>Hello, {{name}}</h1>`,
     styles: [`h1 { color: blue; }`]
   })
   export class HelloComponent {
     name = 'Angular';
   }
   ```

### 5. **What is data binding in Angular?**
   **Answer**: Data binding is a mechanism that allows you to bind the data from your component class to the view (template). Angular provides various types of data binding:
   - **One-way binding**: From the component to the view or vice versa.
   - **Two-way binding**: Using `[(ngModel)]` to bind data both ways.

   **Code Example**:
   ```html
   <input [(ngModel)]="name" placeholder="Enter your name">
   <p>Hello, {{ name }}</p>
   ```

### 6. **Explain Dependency Injection in Angular.**
   **Answer**: Dependency Injection (DI) is a design pattern in Angular where components or services receive their dependencies from an external source, rather than creating them. Angular uses DI to manage the lifecycle and scope of dependencies.

   **Code Example**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class DataService {
     getData() {
       return ['Data1', 'Data2'];
     }
   }

   @Component({
     selector: 'app-data',
     template: `<div *ngFor="let item of data">{{ item }}</div>`
   })
   export class DataComponent implements OnInit {
     data: string[];

     constructor(private dataService: DataService) {}

     ngOnInit() {
       this.data = this.dataService.getData();
     }
   }
   ```

### 7. **What are Directives in Angular?**
   **Answer**: Directives are classes that allow you to extend the behavior of elements in the DOM. There are three types of directives:
   - **Component**: Directives with templates.
   - **Structural Directives**: Change the layout of the DOM, e.g., `*ngIf`, `*ngFor`.
   - **Attribute Directives**: Change the appearance or behavior of an element, e.g., `ngClass`, `ngStyle`.

   **Code Example**:
   ```html
   <div *ngIf="isVisible">This is visible</div>
   ```

### 8. **What are Services in Angular?**
   **Answer**: A service is a class used to share data and logic between components. Services are usually injected into components via Dependency Injection (DI).

   **Code Example**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class MyService {
     getData() {
       return ['Data1', 'Data2', 'Data3'];
     }
   }
   ```

### 9. **What is RxJS in Angular?**
   **Answer**: RxJS (Reactive Extensions for JavaScript) is a library for reactive programming using Observables. It provides operators like `map`, `filter`, `mergeMap`, etc., to handle asynchronous operations.

   **Code Example**:
   ```typescript
   import { Observable } from 'rxjs';
   
   const observable = new Observable(observer => {
     observer.next('Hello');
     observer.next('World');
     observer.complete();
   });

   observable.subscribe({
     next: data => console.log(data),
     complete: () => console.log('Complete!')
   });
   ```

### 10. **What is Angular Routing?**
   **Answer**: Angular routing allows you to navigate between different views or components based on the URL. It is implemented using the `RouterModule`.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: '', component: HomeComponent },
     { path: 'about', component: AboutComponent }
   ];

   @NgModule({
     imports: [RouterModule.forRoot(routes)],
     exports: [RouterModule]
   })
   export class AppRoutingModule {}
   ```

### 11. **What are Angular Pipes?**
   **Answer**: Pipes are used for transforming the output in templates. Angular provides built-in pipes like `date`, `uppercase`, `currency`, etc., and you can also create custom pipes.

   **Code Example**:
   ```html
   <p>{{ birthday | date:'short' }}</p>
   ```

   **Custom Pipe Example**:
   ```typescript
   @Pipe({
     name: 'reverse'
   })
   export class ReversePipe implements PipeTransform {
     transform(value: string): string {
       return value.split('').reverse().join('');
     }
   }
   ```

### 12. **What is Lazy Loading in Angular?**
   **Answer**: Lazy loading is a technique where modules are loaded on demand (when the user navigates to a route) instead of loading all modules upfront.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'admin', loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule) }
   ];
   ```

### 13. **What is Angular CLI?**
   **Answer**: Angular CLI (Command Line Interface) is a tool to automate various tasks in Angular, such as creating components, services, modules, etc. It simplifies the workflow.

   **Common Commands**:
   - `ng new`: Create a new Angular project.
   - `ng generate component <name>`: Generate a new component.
   - `ng serve`: Run the application in development mode.
   - `ng build`: Build the project for production.

### 14. **What is Change Detection in Angular?**
   **Answer**: Change detection is the process of checking for changes in the model and updating the view accordingly. Angular provides different strategies for change detection:
   - **Default**: Checks the entire component tree.
   - **OnPush**: Checks only when input properties change or events are fired.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-child',
     changeDetection: ChangeDetectionStrategy.OnPush,
     template: `{{ data }}`
   })
   ```

### 15. **What is the purpose of ngOnInit?**
   **Answer**: `ngOnInit` is a lifecycle hook that is called once after the component’s constructor. It is used to initialize the component and fetch data before the view is rendered.

   **Code Example**:
   ```typescript
   ngOnInit() {
     console.log('Component initialized');
   }
   ```

### 16. **What are Observables in Angular?**
   **Answer**: Observables are a core part of RxJS and Angular's async operations. They allow you to work with asynchronous data streams.

   **Code Example**:
   ```typescript
   import { Observable } from 'rxjs';
   
   const obs = new Observable(observer => {
     observer.next('Hello');
     observer.complete();
   });
   
   obs.subscribe(data => console.log(data));
   ```

### 17. **What is a Module in Angular?**
   **Answer**: An Angular module is a container for the different parts of an application. It defines a compilation context for components, provides services, and imports other modules.

   **Code Example**:
   ```typescript
   @NgModule({
     declarations: [AppComponent],
     imports: [BrowserModule],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule {}
   ```

---
Here’s a continuation of the list of Angular interview questions and answers with code examples:

### 18. **What is an Observable in Angular?**
   **Answer**: An Observable is a core part of Angular's reactive programming model. It represents a stream of values over time and is often used to handle asynchronous data, such as HTTP requests, user input, or events.

   **Code Example**:
   ```typescript
   import { Observable } from 'rxjs';

   const observable = new Observable(observer => {
     observer.next('Data 1');
     observer.next('Data 2');
     observer.complete();
   });

   observable.subscribe({
     next: value => console.log(value),
     complete: () => console.log('Observable complete')
   });
   ```

### 19. **What are the lifecycle hooks in Angular?**
   **Answer**: Angular components have several lifecycle hooks that allow you to tap into different phases of a component’s lifecycle:
   - `ngOnChanges()`: Called when any data-bound input properties change.
   - `ngOnInit()`: Called once the component is initialized.
   - `ngDoCheck()`: Called during every change detection cycle.
   - `ngAfterContentInit()`: Called after content is projected into the component.
   - `ngAfterContentChecked()`: Called after content is checked.
   - `ngAfterViewInit()`: Called after the component's view is initialized.
   - `ngAfterViewChecked()`: Called after the component's view is checked.
   - `ngOnDestroy()`: Called before Angular destroys the component.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnInit, OnDestroy {
     ngOnInit() {
       console.log('Component Initialized');
     }

     ngOnDestroy() {
       console.log('Component Destroyed');
     }
   }
   ```

### 20. **How do you handle forms in Angular?**
   **Answer**: Angular supports two types of forms:
   - **Template-driven forms**: Simple to use and rely on the HTML template.
   - **Reactive forms**: More complex and offer more control, used for more dynamic and scalable forms.

   **Code Example (Template-driven)**:
   ```html
   <form #form="ngForm">
     <input name="username" ngModel>
     <button [disabled]="!form.valid">Submit</button>
   </form>
   ```

   **Code Example (Reactive Forms)**:
   ```typescript
   import { FormGroup, FormBuilder, Validators } from '@angular/forms';

   export class MyFormComponent implements OnInit {
     form: FormGroup;

     constructor(private fb: FormBuilder) {}

     ngOnInit() {
       this.form = this.fb.group({
         username: ['', Validators.required]
       });
     }

     onSubmit() {
       console.log(this.form.value);
     }
   }
   ```

### 21. **What are the different types of directives in Angular?**
   **Answer**: There are three main types of directives in Angular:
   - **Component Directives**: These are directives with templates. They define a view for a component.
   - **Structural Directives**: These modify the DOM structure, e.g., `*ngIf`, `*ngFor`.
   - **Attribute Directives**: These modify the appearance or behavior of DOM elements, e.g., `ngClass`, `ngStyle`.

   **Code Example (Structural Directive)**:
   ```html
   <div *ngIf="isVisible">This content is visible if isVisible is true</div>
   ```

   **Code Example (Attribute Directive)**:
   ```html
   <div [ngStyle]="{'color': color}">This text changes color</div>
   ```

### 22. **What is NgModule in Angular?**
   **Answer**: NgModule is a fundamental concept in Angular. It is a class decorated with `@NgModule` that organizes an Angular application by grouping related components, services, and other modules. It provides the context for Angular's injector and determines how to build the application.

   **Code Example**:
   ```typescript
   @NgModule({
     declarations: [AppComponent, HomeComponent],
     imports: [BrowserModule, AppRoutingModule],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule {}
   ```

### 23. **What is the role of the `@Injectable` decorator in Angular?**
   **Answer**: The `@Injectable` decorator is used to define a service or class that can be injected into other components or services. It makes the class available to Angular’s dependency injection system.

   **Code Example**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class MyService {
     constructor() {}
     
     getData() {
       return 'Some data';
     }
   }
   ```

### 24. **What is the `ngFor` directive in Angular?**
   **Answer**: The `ngFor` directive is used to loop through an array or list of data and display them in the view.

   **Code Example**:
   ```html
   <ul>
     <li *ngFor="let item of items">{{ item }}</li>
   </ul>
   ```

### 25. **What is the purpose of the `ngIf` directive in Angular?**
   **Answer**: The `ngIf` directive is used to conditionally add or remove elements from the DOM based on a boolean condition.

   **Code Example**:
   ```html
   <div *ngIf="isVisible">This content is conditionally visible</div>
   ```

### 26. **What is a Template Reference Variable in Angular?**
   **Answer**: Template reference variables are used to reference DOM elements or Angular components within the template. They can be used to access the properties of these elements.

   **Code Example**:
   ```html
   <input #inputElement>
   <button (click)="logInputValue(inputElement.value)">Log Input</button>
   ```

### 27. **How do you make an HTTP request in Angular?**
   **Answer**: Angular provides the `HttpClient` module to make HTTP requests. It allows you to interact with REST APIs or backend services.

   **Code Example**:
   ```typescript
   import { HttpClient } from '@angular/common/http';

   @Component({
     selector: 'app-my-component',
     template: ``
   })
   export class MyComponent implements OnInit {
     constructor(private http: HttpClient) {}

     ngOnInit() {
       this.http.get('https://api.example.com/data')
         .subscribe(data => console.log(data));
     }
   }
   ```

### 28. **What is Angular's HttpClientModule?**
   **Answer**: The `HttpClientModule` is an Angular module that provides HTTP client functionalities. It allows making HTTP requests using `HttpClient` service and includes support for interceptors, error handling, and other features.

   **Code Example**:
   ```typescript
   @NgModule({
     imports: [HttpClientModule],
     ...
   })
   export class AppModule {}
   ```

### 29. **What are Angular Guards?**
   **Answer**: Guards are used to control navigation in Angular applications. They are interfaces that can be implemented to prevent or allow navigation based on certain conditions.

   **Types of Guards**:
   - **CanActivate**: Determines whether a route can be activated.
   - **CanActivateChild**: Determines whether a child route can be activated.
   - **CanDeactivate**: Determines whether a route can be deactivated.
   - **CanLoad**: Determines whether a route can be lazily loaded.

   **Code Example (CanActivate Guard)**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class AuthGuard implements CanActivate {
     constructor(private authService: AuthService) {}

     canActivate(): Observable<boolean> | Promise<boolean> | boolean {
       return this.authService.isAuthenticated();
     }
   }
   ```

### 30. **What is the `ngModel` directive in Angular?**
   **Answer**: The `ngModel` directive is used for two-way data binding between the component class and the view. It binds the input element value to the component property.

   **Code Example**:
   ```html
   <input [(ngModel)]="username">
   <p>Your name is {{ username }}</p>
   ```

---

Here are more Angular interview questions and answers, along with code examples:

### 31. **What is the purpose of the `async` pipe in Angular?**
   **Answer**: The `async` pipe in Angular is used to subscribe to an observable or a promise directly in the template. It automatically handles subscription and unsubscription.

   **Code Example**:
   ```html
   <div *ngIf="data | async as result">
     <p>{{ result }}</p>
   </div>
   ```

### 32. **What is Angular’s Change Detection Strategy?**
   **Answer**: Angular uses change detection to update the view whenever data changes. The two strategies are:
   - **Default**: It checks every component in the component tree.
   - **OnPush**: It checks only when the input properties change or when events are fired.

   **Code Example (OnPush)**:
   ```typescript
   @Component({
     selector: 'app-child',
     changeDetection: ChangeDetectionStrategy.OnPush,
     template: `{{ data }}`
   })
   export class ChildComponent {
     @Input() data: string;
   }
   ```

### 33. **What is the difference between `ngOnInit` and `constructor` in Angular?**
   **Answer**: 
   - The `constructor` is called when the component is created, and it is used to initialize class members or inject services.
   - `ngOnInit` is a lifecycle hook that is called after Angular has initialized all data-bound properties of a component.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnInit {
     constructor() {
       console.log('Constructor called');
     }

     ngOnInit() {
       console.log('ngOnInit called');
     }
   }
   ```

### 34. **What is the role of `ngZone` in Angular?**
   **Answer**: `ngZone` is an Angular service that helps with running code outside of Angular’s zone and ensuring Angular’s change detection is triggered when necessary.

   **Code Example**:
   ```typescript
   import { NgZone } from '@angular/core';

   export class MyComponent {
     constructor(private zone: NgZone) {}

     triggerChangeDetection() {
       this.zone.run(() => {
         console.log('Change detection triggered');
       });
     }
   }
   ```

### 35. **What is the difference between `@Input` and `@Output` decorators in Angular?**
   **Answer**: 
   - `@Input`: Allows data to flow from the parent component to the child component.
   - `@Output`: Allows data to flow from the child component to the parent component through event binding.

   **Code Example (Using `@Input`)**:
   ```typescript
   @Component({
     selector: 'app-child',
     template: `<p>{{ message }}</p>`
   })
   export class ChildComponent {
     @Input() message: string;
   }
   ```

   **Code Example (Using `@Output`)**:
   ```typescript
   @Component({
     selector: 'app-child',
     template: `<button (click)="sendData()">Send Data</button>`
   })
   export class ChildComponent {
     @Output() messageEvent = new EventEmitter<string>();

     sendData() {
       this.messageEvent.emit('Hello from Child!');
     }
   }
   ```

### 36. **What is the purpose of `ng-content` in Angular?**
   **Answer**: `ng-content` is used for content projection, allowing you to project content from the parent component into the child component’s template. It is useful for creating reusable and flexible components.

   **Code Example**:
   ```html
   <!-- Parent Component -->
   <app-card>
     <div>Projected content</div>
   </app-card>

   <!-- Child Component -->
   <div class="card">
     <ng-content></ng-content>
   </div>
   ```

### 37. **What is the `ngOnChanges` lifecycle hook in Angular?**
   **Answer**: The `ngOnChanges` lifecycle hook is called whenever there is a change in one of the input properties bound to the component. It provides the previous and current values of the changed property.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnChanges {
     @Input() data: string;

     ngOnChanges(changes: SimpleChanges) {
       console.log(changes);
     }
   }
   ```

### 38. **What is the `@ViewChild` decorator in Angular?**
   **Answer**: `@ViewChild` is a decorator used to get a reference to a child component, directive, or DOM element within the template of the parent component. It allows interaction with child components or elements directly.

   **Code Example**:
   ```typescript
   import { ViewChild, ElementRef } from '@angular/core';

   export class MyComponent {
     @ViewChild('inputElement') input: ElementRef;

     ngAfterViewInit() {
       this.input.nativeElement.focus();
     }
   }
   ```

### 39. **What is the purpose of `ngModel` in forms?**
   **Answer**: `ngModel` is used for two-way data binding in Angular forms. It binds the value of an input field to a property in the component class, and any changes in the input field are reflected in the property and vice versa.

   **Code Example**:
   ```html
   <input [(ngModel)]="username">
   <p>Your name is {{ username }}</p>
   ```

### 40. **How do you make an HTTP GET request in Angular?**
   **Answer**: You can make an HTTP GET request using Angular’s `HttpClient` service, which is part of the `HttpClientModule`.

   **Code Example**:
   ```typescript
   import { HttpClient } from '@angular/common/http';

   @Component({
     selector: 'app-my-component',
     template: ''
   })
   export class MyComponent implements OnInit {
     constructor(private http: HttpClient) {}

     ngOnInit() {
       this.http.get('https://api.example.com/data').subscribe(data => {
         console.log(data);
       });
     }
   }
   ```

### 41. **What is the `HttpInterceptor` in Angular?**
   **Answer**: An `HttpInterceptor` is used to intercept and modify HTTP requests and responses globally. It can be used for adding authentication tokens, handling errors, etc.

   **Code Example**:
   ```typescript
   import { Injectable } from '@angular/core';
   import { HttpInterceptor, HttpRequest, HttpHandler, HttpEvent } from '@angular/common/http';
   import { Observable } from 'rxjs';

   @Injectable()
   export class AuthInterceptor implements HttpInterceptor {
     intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
       const clonedRequest = req.clone({
         headers: req.headers.set('Authorization', 'Bearer ' + localStorage.getItem('token'))
       });
       return next.handle(clonedRequest);
     }
   }
   ```

### 42. **What is the `ngOnDestroy` lifecycle hook in Angular?**
   **Answer**: `ngOnDestroy` is called just before Angular destroys the component or directive. It is often used for cleanup tasks such as unsubscribing from observables, clearing timeouts, or stopping intervals.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnDestroy {
     ngOnDestroy() {
       console.log('Component destroyed');
     }
   }
   ```

### 43. **How do you handle routing in Angular?**
   **Answer**: Routing in Angular is handled using the `RouterModule`. You define routes in your application using `RouterModule.forRoot(routes)`, where `routes` is an array of route objects.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'home', component: HomeComponent },
     { path: 'about', component: AboutComponent }
   ];

   @NgModule({
     imports: [RouterModule.forRoot(routes)],
     exports: [RouterModule]
   })
   export class AppRoutingModule {}
   ```

### 44. **What is the `ActivatedRoute` in Angular?**
   **Answer**: `ActivatedRoute` is used to access the current route’s parameters, query parameters, and other route-related information.

   **Code Example**:
   ```typescript
   import { ActivatedRoute } from '@angular/router';

   export class MyComponent implements OnInit {
     constructor(private route: ActivatedRoute) {}

     ngOnInit() {
       this.route.paramMap.subscribe(params => {
         const id = params.get('id');
         console.log('Route parameter:', id);
       });
     }
   }
   ```

### 45. **How do you create a custom pipe in Angular?**
   **Answer**: You can create a custom pipe by implementing the `PipeTransform` interface and using the `@Pipe` decorator.

   **Code Example**:
   ```typescript
   import { Pipe, PipeTransform } from '@angular/core';

   @Pipe({
     name: 'reverse'
   })
   export class ReversePipe implements PipeTransform {
     transform(value: string): string {
       return value.split('').reverse().join('');
     }
   }
   ```

---
Here are more Angular interview questions and answers with code examples:

### 46. **What is Lazy Loading in Angular?**
   **Answer**: Lazy loading is a technique in Angular where modules are loaded only when they are needed, rather than at the initial application load. This improves the performance of the application by reducing the initial load time.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: '', component: HomeComponent },
     { path: 'about', loadChildren: () => import('./about/about.module').then(m => m.AboutModule) }
   ];

   @NgModule({
     imports: [RouterModule.forRoot(routes)],
     exports: [RouterModule]
   })
   export class AppRoutingModule {}
   ```

### 47. **What is the `trackBy` function in `ngFor`?**
   **Answer**: The `trackBy` function helps Angular identify items in the list more efficiently by tracking the unique identifier of each item, preventing unnecessary re-renders of the entire list.

   **Code Example**:
   ```html
   <ul>
     <li *ngFor="let item of items; trackBy: trackById">{{ item.name }}</li>
   </ul>
   ```

   ```typescript
   export class MyComponent {
     items = [{ id: 1, name: 'Item 1' }, { id: 2, name: 'Item 2' }];

     trackById(index: number, item: any) {
       return item.id;
     }
   }
   ```

### 48. **What is `ngAfterViewInit` lifecycle hook in Angular?**
   **Answer**: The `ngAfterViewInit` lifecycle hook is called after Angular has initialized the component's view and child views. It is often used when you need to perform an action after the component's view has been fully initialized.

   **Code Example**:
   ```typescript
   export class MyComponent implements AfterViewInit {
     @ViewChild('myElement') elementRef: ElementRef;

     ngAfterViewInit() {
       console.log(this.elementRef.nativeElement);
     }
   }
   ```

### 49. **What is the difference between `ngOnInit` and `ngAfterViewInit`?**
   **Answer**: 
   - `ngOnInit`: Called after the component's input properties are set, but before the view is initialized.
   - `ngAfterViewInit`: Called after the component's view and child views are initialized.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnInit, AfterViewInit {
     ngOnInit() {
       console.log('ngOnInit called');
     }

     ngAfterViewInit() {
       console.log('ngAfterViewInit called');
     }
   }
   ```

### 50. **What is the role of the `ng-template` in Angular?**
   **Answer**: The `ng-template` directive is used to define a template that is not rendered immediately but can be rendered later, based on specific conditions or events. It is commonly used with structural directives like `*ngIf` or `*ngFor`.

   **Code Example**:
   ```html
   <ng-template #loading>
     <p>Loading...</p>
   </ng-template>

   <div *ngIf="isLoading; else loading">Data Loaded</div>
   ```

### 51. **How do you pass data from a parent to a child component in Angular?**
   **Answer**: In Angular, data can be passed from a parent component to a child component using the `@Input` decorator.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-child',
     template: `<p>{{ message }}</p>`
   })
   export class ChildComponent {
     @Input() message: string;
   }

   @Component({
     selector: 'app-parent',
     template: `<app-child [message]="parentMessage"></app-child>`
   })
   export class ParentComponent {
     parentMessage = 'Hello from Parent';
   }
   ```

### 52. **How do you pass data from a child to a parent component in Angular?**
   **Answer**: In Angular, data can be passed from a child component to a parent component using the `@Output` decorator with an `EventEmitter`.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-child',
     template: `<button (click)="sendData()">Send Data</button>`
   })
   export class ChildComponent {
     @Output() dataEvent = new EventEmitter<string>();

     sendData() {
       this.dataEvent.emit('Hello from Child');
     }
   }

   @Component({
     selector: 'app-parent',
     template: `<app-child (dataEvent)="receiveData($event)"></app-child>`
   })
   export class ParentComponent {
     receiveData(data: string) {
       console.log(data); // 'Hello from Child'
     }
   }
   ```

### 53. **What is Angular CLI?**
   **Answer**: Angular CLI (Command Line Interface) is a command-line tool for automating common Angular development tasks. It helps in creating components, services, and modules, running tests, building applications, and more.

   **Code Example**:
   To create a new Angular component using Angular CLI:
   ```bash
   ng generate component my-component
   ```

### 54. **How do you define routes in Angular?**
   **Answer**: Routes in Angular are defined in the `RouterModule` configuration. You can specify the path and the associated component to load when the path is accessed.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'home', component: HomeComponent },
     { path: 'about', component: AboutComponent }
   ];

   @NgModule({
     imports: [RouterModule.forRoot(routes)],
     exports: [RouterModule]
   })
   export class AppRoutingModule {}
   ```

### 55. **What is a service in Angular?**
   **Answer**: A service is a class that provides functionality that can be shared across components in Angular. It typically encapsulates business logic, HTTP requests, or data management.

   **Code Example**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class MyService {
     getData() {
       return 'Hello from Service';
     }
   }

   @Component({
     selector: 'app-my-component',
     template: `{{ data }}`
   })
   export class MyComponent implements OnInit {
     data: string;

     constructor(private myService: MyService) {}

     ngOnInit() {
       this.data = this.myService.getData();
     }
   }
   ```

### 56. **What is the role of `ngOnChanges` in Angular?**
   **Answer**: `ngOnChanges` is a lifecycle hook that is called when any data-bound input properties change. It provides the previous and current values of the changed properties.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnChanges {
     @Input() data: string;

     ngOnChanges(changes: SimpleChanges) {
       console.log('Previous:', changes.data.previousValue);
       console.log('Current:', changes.data.currentValue);
     }
   }
   ```

### 57. **What is `ng-content` used for in Angular?**
   **Answer**: `ng-content` is used for content projection in Angular, allowing you to insert content into a component's template from the parent component. It enables building reusable components.

   **Code Example**:
   ```html
   <!-- Parent Component -->
   <app-card>
     <p>This content is projected into the card.</p>
   </app-card>

   <!-- Child Component -->
   <div class="card">
     <ng-content></ng-content>
   </div>
   ```

### 58. **What is the purpose of `changeDetection` in Angular?**
   **Answer**: `changeDetection` is a strategy in Angular used to check for changes in the application and update the view accordingly. By default, Angular uses `ChangeDetectionStrategy.Default`, but you can use `ChangeDetectionStrategy.OnPush` for performance optimization.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-child',
     changeDetection: ChangeDetectionStrategy.OnPush,
     template: `{{ data }}`
   })
   export class ChildComponent {
     @Input() data: string;
   }
   ```

### 59. **What are the different types of directives in Angular?**
   **Answer**: There are three main types of directives in Angular:
   - **Structural Directives**: These change the structure of the DOM (e.g., `*ngIf`, `*ngFor`).
   - **Attribute Directives**: These modify the appearance or behavior of an element (e.g., `ngClass`, `ngStyle`).
   - **Component Directives**: These define a view along with its behavior (e.g., a component).

   **Code Example (Structural Directive)**:
   ```html
   <div *ngIf="isVisible">This content is visible if isVisible is true</div>
   ```

---
Here are more Angular interview questions and answers with code examples:

### 60. **What are Observables in Angular?**
   **Answer**: Observables are a core part of reactive programming in Angular. They represent a stream of data that can be observed and manipulated over time. Angular uses Observables heavily, especially with HTTP requests and reactive forms.

   **Code Example**:
   ```typescript
   import { Observable } from 'rxjs';
   import { HttpClient } from '@angular/common/http';

   @Component({
     selector: 'app-my-component',
     template: ''
   })
   export class MyComponent implements OnInit {
     constructor(private http: HttpClient) {}

     ngOnInit() {
       this.http.get('https://api.example.com/data')
         .subscribe(data => {
           console.log(data);
         });
     }
   }
   ```

### 61. **What is a Pipe in Angular?**
   **Answer**: A pipe in Angular is a simple function that transforms input data to a desired output format. It can be used in templates to format data before display. Angular provides built-in pipes like `date`, `currency`, `lowercase`, etc., and custom pipes can also be created.

   **Code Example**:
   ```typescript
   import { Pipe, PipeTransform } from '@angular/core';

   @Pipe({
     name: 'reverse'
   })
   export class ReversePipe implements PipeTransform {
     transform(value: string): string {
       return value.split('').reverse().join('');
     }
   }
   ```

   ```html
   <p>{{ 'hello' | reverse }}</p>
   ```

### 62. **What is Dependency Injection in Angular?**
   **Answer**: Dependency Injection (DI) is a design pattern used to implement IoC (Inversion of Control) in Angular. It allows the injection of services or dependencies into a component or another service rather than creating them directly. Angular’s DI system provides a way to manage and inject instances of services into components and other services.

   **Code Example**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class MyService {
     getData() {
       return 'Hello from Service';
     }
   }

   @Component({
     selector: 'app-my-component',
     template: `{{ data }}`
   })
   export class MyComponent implements OnInit {
     data: string;

     constructor(private myService: MyService) {}

     ngOnInit() {
       this.data = this.myService.getData();
     }
   }
   ```

### 63. **What is the `ngOnChanges` lifecycle hook used for?**
   **Answer**: The `ngOnChanges` lifecycle hook is used to handle changes in input properties of a component. It is called every time one of the input properties changes, allowing you to perform actions or update the state based on those changes.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnChanges {
     @Input() name: string;

     ngOnChanges(changes: SimpleChanges) {
       console.log('Previous value:', changes.name.previousValue);
       console.log('Current value:', changes.name.currentValue);
     }
   }
   ```

### 64. **What is the purpose of the `angular.json` file in an Angular project?**
   **Answer**: The `angular.json` file is the configuration file for Angular CLI. It contains various configuration options for the build process, including settings for styles, scripts, assets, and environments. It also defines project and application structures.

### 65. **What are Angular Modules?**
   **Answer**: An Angular module (`@NgModule`) is a container for related components, services, and other modules. It provides a way to organize an application into cohesive blocks of functionality. The root module is typically called `AppModule`.

   **Code Example**:
   ```typescript
   @NgModule({
     declarations: [AppComponent],
     imports: [BrowserModule, AppRoutingModule],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule {}
   ```

### 66. **What is the difference between `ViewChild` and `ContentChild` in Angular?**
   **Answer**:
   - `@ViewChild`: Used to get a reference to a DOM element or a child component in the same template as the component.
   - `@ContentChild`: Used to get a reference to content projected into the component using `<ng-content>`.

   **Code Example (ViewChild)**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     template: `<input #inputElement>`
   })
   export class MyComponent {
     @ViewChild('inputElement') inputElement: ElementRef;

     ngAfterViewInit() {
       this.inputElement.nativeElement.focus();
     }
   }
   ```

   **Code Example (ContentChild)**:
   ```typescript
   @Component({
     selector: 'app-parent',
     template: `<app-child><p>Hello</p></app-child>`
   })
   export class ParentComponent {}

   @Component({
     selector: 'app-child',
     template: `<ng-content></ng-content>`
   })
   export class ChildComponent {
     @ContentChild('content') content: ElementRef;
   }
   ```

### 67. **What is a guard in Angular routing?**
   **Answer**: Guards in Angular are used to control access to certain routes. They can be used to prevent or allow navigation based on conditions. The types of guards are:
   - `CanActivate`: Determines whether a route can be activated.
   - `CanDeactivate`: Determines whether a route can be deactivated.
   - `CanLoad`: Prevents a route from being loaded.
   - `Resolve`: Resolves data before a route is activated.

   **Code Example (CanActivate Guard)**:
   ```typescript
   @Injectable({
     providedIn: 'root'
   })
   export class AuthGuard implements CanActivate {
     constructor(private authService: AuthService, private router: Router) {}

     canActivate(): Observable<boolean> | Promise<boolean> | boolean {
       if (this.authService.isLoggedIn()) {
         return true;
       } else {
         this.router.navigate(['/login']);
         return false;
       }
     }
   }
   ```

   **In Routing**:
   ```typescript
   const routes: Routes = [
     { path: 'dashboard', component: DashboardComponent, canActivate: [AuthGuard] }
   ];
   ```

### 68. **What is the `ngModel` directive in Angular?**
   **Answer**: `ngModel` is used for two-way data binding in Angular. It binds an input field’s value to a variable in the component, and any changes in the input are reflected in the component property, and vice versa.

   **Code Example**:
   ```html
   <input [(ngModel)]="username" />
   <p>Your username is {{ username }}</p>
   ```

### 69. **What is the purpose of the `rxjs` library in Angular?**
   **Answer**: `rxjs` (Reactive Extensions for JavaScript) is used for handling asynchronous operations and event-based programs. It provides a powerful model for working with streams of data, such as HTTP requests or user events.

   **Code Example**:
   ```typescript
   import { Observable } from 'rxjs';

   export class MyComponent {
     observable$ = new Observable(observer => {
       observer.next('Hello');
       observer.complete();
     });

     ngOnInit() {
       this.observable$.subscribe(value => {
         console.log(value);
       });
     }
   }
   ```

### 70. **What are Angular Validators?**
   **Answer**: Angular validators are used in forms to validate user input. These include built-in validators like `required`, `minlength`, `maxlength`, `pattern`, etc. Custom validators can also be created.

   **Code Example (Reactive Form)**:
   ```typescript
   export class MyComponent implements OnInit {
     form: FormGroup;

     ngOnInit() {
       this.form = new FormGroup({
         username: new FormControl('', [Validators.required, Validators.minLength(3)])
       });
     }
   }
   ```

   ```html
   <form [formGroup]="form">
     <input formControlName="username" />
     <div *ngIf="form.get('username').hasError('required')">
       Username is required.
     </div>
   </form>
   ```

### 71. **What is `HttpClientModule` and how do you use it?**
   **Answer**: `HttpClientModule` is a module in Angular used for making HTTP requests to the server. It is part of the `@angular/common/http` package. To use it, you need to import it into the `AppModule`.

   **Code Example**:
   ```typescript
   import { HttpClientModule } from '@angular/common/http';

   @NgModule({
     imports: [HttpClientModule]
   })
   export class AppModule {}
   ```

   **Using HttpClient**:
   ```typescript
   import { HttpClient } from '@angular/common/http';

   @Component({
     selector: 'app-my-component',
     template: ''
   })
   export class MyComponent {
     constructor(private http: HttpClient) {}

     ngOnInit() {
       this.http.get('https://api.example.com/data').subscribe(data => {
         console.log(data);
       });
     }
   }
   ```

---

Here are more Angular interview questions and answers with code examples:

### 72. **What is the purpose of `ngOnDestroy` lifecycle hook in Angular?**
   **Answer**: `ngOnDestroy` is a lifecycle hook that is called just before the component or directive is destroyed. It is commonly used for cleanup tasks, such as unsubscribing from Observables or detaching event listeners to avoid memory leaks.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnDestroy {
     private subscription: Subscription;

     constructor(private myService: MyService) {
       this.subscription = this.myService.getData().subscribe(data => {
         console.log(data);
       });
     }

     ngOnDestroy() {
       // Unsubscribe to prevent memory leaks
       this.subscription.unsubscribe();
     }
   }
   ```

### 73. **What is the `ChangeDetectionStrategy` in Angular?**
   **Answer**: `ChangeDetectionStrategy` defines how Angular checks for changes in component data and updates the view. There are two strategies:
   - **Default**: Angular checks all components in the component tree during each change detection cycle.
   - **OnPush**: Angular only checks the component when any of its input properties change, improving performance for components with immutable data.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     changeDetection: ChangeDetectionStrategy.OnPush,
     template: `<p>{{ data }}</p>`
   })
   export class MyComponent {
     @Input() data: string;
   }
   ```

### 74. **What is a custom validator in Angular?**
   **Answer**: A custom validator in Angular is a function that you can write to perform custom validation logic on a form control. It returns either `null` if the input is valid or an object if the input is invalid.

   **Code Example**:
   ```typescript
   import { AbstractControl, ValidationErrors } from '@angular/forms';

   export function noSpacesValidator(control: AbstractControl): ValidationErrors | null {
     return control.value && control.value.includes(' ') ? { noSpaces: true } : null;
   }

   @Component({
     selector: 'app-my-component',
     template: `<form [formGroup]="form">
       <input formControlName="username" />
     </form>`
   })
   export class MyComponent {
     form: FormGroup;

     constructor(private fb: FormBuilder) {
       this.form = this.fb.group({
         username: ['', [noSpacesValidator]]
       });
     }
   }
   ```

### 75. **What is the difference between `ngIf` and `ngSwitch`?**
   **Answer**:
   - `ngIf` is used to conditionally include or exclude elements in the DOM based on an expression. It removes the element from the DOM when the condition is false.
   - `ngSwitch` is a more complex conditional directive used to switch between different views based on a specific expression.

   **Code Example (ngIf)**:
   ```html
   <div *ngIf="isVisible">This content is visible</div>
   ```

   **Code Example (ngSwitch)**:
   ```html
   <div [ngSwitch]="currentView">
     <div *ngSwitchCase="'home'">Home view</div>
     <div *ngSwitchCase="'about'">About view</div>
     <div *ngSwitchDefault>Default view</div>
   </div>
   ```

### 76. **What is the purpose of `Renderer2` in Angular?**
   **Answer**: `Renderer2` is an Angular service that provides an abstraction for DOM manipulation. It allows developers to interact with the DOM in a safe, platform-independent manner, such as adding or removing CSS classes, setting styles, and handling events.

   **Code Example**:
   ```typescript
   import { Renderer2, ElementRef } from '@angular/core';

   @Component({
     selector: 'app-my-component',
     template: '<div #divElement>Content</div>'
   })
   export class MyComponent {
     constructor(private renderer: Renderer2, private el: ElementRef) {}

     ngAfterViewInit() {
       this.renderer.setStyle(this.el.nativeElement, 'color', 'blue');
     }
   }
   ```

### 77. **What are Angular Animations?**
   **Answer**: Angular Animations provide a way to animate elements and components in your application. They allow for the definition of triggers, states, and transitions to create dynamic, interactive user experiences.

   **Code Example**:
   ```typescript
   import { trigger, state, style, transition, animate } from '@angular/animations';

   @Component({
     selector: 'app-my-component',
     template: `<div [@fadeIn]="state">Hello</div>`,
     animations: [
       trigger('fadeIn', [
         state('void', style({ opacity: 0 })),
         transition(':enter', [animate('1s', style({ opacity: 1 }))]),
       ])
     ]
   })
   export class MyComponent {
     state = 'in';
   }
   ```

### 78. **How do you implement routing with parameters in Angular?**
   **Answer**: You can pass parameters to routes in Angular by using route parameters in the URL. To access these parameters in the component, use `ActivatedRoute`.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'profile/:id', component: ProfileComponent }
   ];

   @Component({
     selector: 'app-profile',
     template: `<p>User ID: {{ userId }}</p>`
   })
   export class ProfileComponent implements OnInit {
     userId: string;

     constructor(private route: ActivatedRoute) {}

     ngOnInit() {
       this.userId = this.route.snapshot.paramMap.get('id');
     }
   }
   ```

### 79. **What is a `Subject` in RxJS?**
   **Answer**: A `Subject` in RxJS is both an Observable and an Observer. It allows values to be multicasted to many Observers. A `Subject` is useful for scenarios where you want multiple subscribers to listen to the same event or data stream.

   **Code Example**:
   ```typescript
   import { Subject } from 'rxjs';

   export class MyComponent {
     private subject = new Subject<string>();

     constructor() {
       this.subject.subscribe(value => console.log('Subscriber 1:', value));
       this.subject.subscribe(value => console.log('Subscriber 2:', value));
     }

     sendData() {
       this.subject.next('Hello from Subject');
     }
   }
   ```

### 80. **What is the difference between `BehaviorSubject` and `Subject`?**
   **Answer**: 
   - `BehaviorSubject`: Requires an initial value and always returns the current value to new subscribers.
   - `Subject`: Does not require an initial value and does not return any value to new subscribers unless it has been emitted.

   **Code Example (BehaviorSubject)**:
   ```typescript
   import { BehaviorSubject } from 'rxjs';

   export class MyComponent {
     private subject = new BehaviorSubject<string>('Initial Value');

     constructor() {
       this.subject.subscribe(value => console.log('Subscriber 1:', value));
     }

     sendData() {
       this.subject.next('Updated Value');
     }
   }
   ```

### 81. **What is the difference between `subscribe` and `async` pipe in Angular?**
   **Answer**: 
   - `subscribe`: It is used to manually subscribe to an Observable in the component. You need to unsubscribe to prevent memory leaks.
   - `async` pipe: It automatically subscribes to an Observable in the template and unsubscribes when the component is destroyed.

   **Code Example (subscribe)**:
   ```typescript
   export class MyComponent {
     data$: Observable<string>;

     ngOnInit() {
       this.data$.subscribe(data => console.log(data));
     }
   }
   ```

   **Code Example (async pipe)**:
   ```html
   <div>{{ data$ | async }}</div>
   ```

### 82. **What is `ngModel` in Angular forms?**
   **Answer**: `ngModel` is used for two-way data binding in Angular forms. It binds a form control (e.g., an input field) to a variable in the component, so changes in the input are automatically reflected in the variable and vice versa.

   **Code Example**:
   ```html
   <input [(ngModel)]="name" />
   <p>Hello, {{ name }}!</p>
   ```

### 83. **What is the `Injector` in Angular?**
   **Answer**: The `Injector` in Angular is a service that is responsible for creating instances of dependencies and providing them to components or services. It is a key part of Angular's Dependency Injection system.

   **Code Example**:
   ```typescript
   import { Injector } from '@angular/core';

   export class MyComponent {
     constructor(private injector: Injector) {
       const myService = this.injector.get(MyService);
     }
   }
   ```

---

Here are more Angular interview questions and answers with code examples:

### 84. **What are `ng-content` and `ng-content` projection in Angular?**
   **Answer**: `ng-content` is used for content projection in Angular. It allows you to insert content into the component from its parent component. It’s useful when you need to create reusable components that need to display different content provided by the parent.

   **Code Example**:
   ```html
   <!-- Parent Component -->
   <app-child>
     <p>This is the projected content!</p>
   </app-child>

   <!-- Child Component -->
   <div>
     <ng-content></ng-content>
   </div>
   ```

### 85. **What are `ngFor` and `ngForTrackBy`?**
   **Answer**:
   - `ngFor` is a structural directive used to iterate over a collection (array or object) and render the content for each item.
   - `ngForTrackBy` improves performance by tracking the identity of items in the list. It helps Angular identify which items have changed, been added, or removed, avoiding unnecessary DOM updates.

   **Code Example (ngFor)**:
   ```html
   <ul>
     <li *ngFor="let item of items">{{ item }}</li>
   </ul>
   ```

   **Code Example (ngForTrackBy)**:
   ```html
   <ul>
     <li *ngFor="let item of items; trackBy: trackById">{{ item.name }}</li>
   </ul>
   ```

   ```typescript
   trackById(index: number, item: any): number {
     return item.id;
   }
   ```

### 86. **What is the difference between a component and a directive in Angular?**
   **Answer**: 
   - A **component** is a class that controls a view (HTML template) and encapsulates its logic, styles, and template.
   - A **directive** is a class that allows you to extend the HTML vocabulary and behavior, but it does not control a template or view directly. Directives can be structural (e.g., `ngIf`, `ngFor`) or attribute-based (e.g., `ngClass`, `ngStyle`).

   **Code Example (Component)**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     template: '<div>My Component</div>'
   })
   export class MyComponent {}
   ```

   **Code Example (Directive)**:
   ```typescript
   @Directive({
     selector: '[appHighlight]'
   })
   export class HighlightDirective {
     constructor(el: ElementRef) {
       el.nativeElement.style.backgroundColor = 'yellow';
     }
   }
   ```

### 87. **What are lifecycle hooks in Angular?**
   **Answer**: Lifecycle hooks are methods in Angular components and directives that allow you to tap into different phases of their lifecycle, such as creation, updating, and destruction. Some common lifecycle hooks include:
   - `ngOnInit`: Called after the component is initialized.
   - `ngOnChanges`: Called when input properties change.
   - `ngDoCheck`: Called during every change detection cycle.
   - `ngOnDestroy`: Called before the component is destroyed.

### 88. **What is the `Renderer2` service and why should it be used?**
   **Answer**: `Renderer2` is an Angular service used to manipulate the DOM in a platform-independent way. It is recommended to use `Renderer2` instead of directly accessing the DOM, especially when working with Angular Universal (server-side rendering).

   **Code Example**:
   ```typescript
   import { Renderer2, ElementRef } from '@angular/core';

   @Component({
     selector: 'app-my-component',
     template: '<div #divElement>Content</div>'
   })
   export class MyComponent {
     constructor(private renderer: Renderer2, private el: ElementRef) {}

     ngAfterViewInit() {
       this.renderer.setStyle(this.el.nativeElement, 'color', 'blue');
     }
   }
   ```

### 89. **What is `ngOnChanges` and when is it called?**
   **Answer**: `ngOnChanges` is a lifecycle hook called when an input property (`@Input`) of a component changes. It is triggered every time the bound value changes, and it receives a `SimpleChanges` object that contains the current and previous values of the input properties.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     template: '<div>{{ name }}</div>'
   })
   export class MyComponent implements OnChanges {
     @Input() name: string;

     ngOnChanges(changes: SimpleChanges) {
       console.log('Previous:', changes.name.previousValue);
       console.log('Current:', changes.name.currentValue);
     }
   }
   ```

### 90. **What is an `Observable` in Angular, and how is it different from a `Promise`?**
   **Answer**:
   - An `Observable` represents a stream of data that can emit multiple values over time, while a `Promise` is a single value that is eventually resolved.
   - Observables are cancellable and can be composed using operators like `map`, `filter`, and `mergeMap`. Promises, on the other hand, are not cancellable and only return a single result.

   **Code Example (Observable)**:
   ```typescript
   import { Observable } from 'rxjs';

   const observable = new Observable(observer => {
     observer.next('Hello');
     observer.next('World');
     observer.complete();
   });

   observable.subscribe(value => {
     console.log(value); // Output: Hello, World
   });
   ```

   **Code Example (Promise)**:
   ```typescript
   const promise = new Promise((resolve, reject) => {
     resolve('Hello');
   });

   promise.then(value => {
     console.log(value); // Output: Hello
   });
   ```

### 91. **What are the different types of Angular modules?**
   **Answer**: Angular modules are classified into different types:
   - **Root Module** (`AppModule`): The main module that bootstraps the Angular application.
   - **Feature Modules**: These are modules that encapsulate functionality like routing or business logic. They can be lazy-loaded.
   - **Shared Modules**: Used to group commonly used components, directives, and pipes that can be shared across multiple modules.
   - **Core Module**: Contains singleton services used throughout the application (e.g., authentication, logging).

   **Code Example (Root Module)**:
   ```typescript
   @NgModule({
     declarations: [AppComponent],
     imports: [BrowserModule, AppRoutingModule],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule {}
   ```

### 92. **What is lazy loading in Angular and how do you implement it?**
   **Answer**: Lazy loading is a technique used to load modules only when they are needed. This reduces the initial loading time of the application. Lazy loading is typically implemented using the `loadChildren` property in the route configuration.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'dashboard', loadChildren: () => import('./dashboard/dashboard.module').then(m => m.DashboardModule) }
   ];
   ```

### 93. **What is the purpose of `RouterLink` and `routerLinkActive` directives in Angular?**
   **Answer**:
   - `RouterLink`: It is used to navigate to a route in the Angular application. It can be applied to anchor tags (`<a>`) or other elements.
   - `routerLinkActive`: It is used to add a CSS class to the element when the associated route is active.

   **Code Example (RouterLink)**:
   ```html
   <a [routerLink]="['/home']">Home</a>
   ```

   **Code Example (routerLinkActive)**:
   ```html
   <a [routerLink]="['/home']" routerLinkActive="active">Home</a>
   ```

### 94. **What is the role of `HttpClient` in Angular?**
   **Answer**: `HttpClient` is a service in Angular used to make HTTP requests to a server. It provides methods like `get`, `post`, `put`, `delete`, etc., and returns an Observable for handling the response. `HttpClient` is part of the `@angular/common/http` module.

   **Code Example**:
   ```typescript
   import { HttpClient } from '@angular/common/http';

   @Component({
     selector: 'app-my-component',
     template: ''
   })
   export class MyComponent {
     constructor(private http: HttpClient) {}

     ngOnInit() {
       this.http.get('https://api.example.com/data').subscribe(data => {
         console.log(data);
       });
     }
   }
   ```

### 95. **What is the purpose of the `async` pipe in Angular?**
   **Answer**: The `async` pipe subscribes to an Observable or Promise and returns the latest emitted value. It automatically handles unsubscription when the component is destroyed, making it ideal for use with Observables in templates.

   **Code Example**:
   ```html
   <div>{{ observableData | async }}</div>
   ```

---

Here are more Angular interview questions and answers with code examples:

### 96. **What is the difference between `ngOnInit` and `constructor` in Angular components?**
   **Answer**:
   - **`constructor`**: It is used for dependency injection and initializing basic properties. It is executed before `ngOnInit`.
   - **`ngOnInit`**: It is a lifecycle hook and is used for initializing the component after the constructor. It is called once the component's inputs have been bound and is typically used for component initialization logic.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     template: `<p>{{message}}</p>`
   })
   export class MyComponent implements OnInit {
     message: string;

     constructor() {
       console.log('Constructor called');
     }

     ngOnInit() {
       this.message = 'ngOnInit called!';
       console.log('ngOnInit called');
     }
   }
   ```

### 97. **What are Angular modules and why are they important?**
   **Answer**: Angular modules (`@NgModule`) are used to organize the application into logical units. Modules help to define the scope of components, directives, pipes, and services within an application. The root module (`AppModule`) is the entry point of an Angular app, and feature modules can be added to break the app into smaller, more manageable parts.

   **Code Example**:
   ```typescript
   @NgModule({
     declarations: [AppComponent],
     imports: [BrowserModule],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule {}
   ```

### 98. **What is `ngModel` and how does it work in Angular?**
   **Answer**: `ngModel` is a directive that facilitates two-way data binding in Angular forms. It links an input field with a variable in the component, allowing changes to propagate in both directions (from component to view and from view to component).

   **Code Example**:
   ```html
   <input [(ngModel)]="name" />
   <p>Your name is: {{ name }}</p>
   ```

   **Code Example (Component)**:
   ```typescript
   export class MyComponent {
     name: string = '';
   }
   ```

### 99. **What are `Route Guards` in Angular?**
   **Answer**: Route guards in Angular are used to protect routes from unauthorized access, redirect users based on conditions, or resolve data before navigating to a route. The main types of guards are:
   - **CanActivate**: Decides if a route can be activated.
   - **CanDeactivate**: Decides if the user can leave a route.
   - **Resolve**: Resolves data before the route is activated.
   - **CanLoad**: Determines if a route can be lazy-loaded.

   **Code Example (CanActivate)**:
   ```typescript
   import { Injectable } from '@angular/core';
   import { CanActivate, ActivatedRouteSnapshot, RouterStateSnapshot, Router } from '@angular/router';
   import { Observable } from 'rxjs';

   @Injectable({
     providedIn: 'root',
   })
   export class AuthGuard implements CanActivate {
     constructor(private router: Router) {}

     canActivate(
       route: ActivatedRouteSnapshot,
       state: RouterStateSnapshot
     ): Observable<boolean> | Promise<boolean> | boolean {
       if (/* check auth condition */) {
         return true;
       } else {
         this.router.navigate(['/login']);
         return false;
       }
     }
   }
   ```

### 100. **What is `HttpInterceptor` in Angular?**
   **Answer**: `HttpInterceptor` is used to intercept HTTP requests and responses. It allows modification of requests, adding headers, logging, and error handling before sending them to the server. It can be used for authentication, authorization, or to manipulate HTTP responses globally.

   **Code Example**:
   ```typescript
   import { Injectable } from '@angular/core';
   import { HttpInterceptor, HttpRequest, HttpHandler, HttpEvent } from '@angular/common/http';
   import { Observable } from 'rxjs';

   @Injectable()
   export class AuthInterceptor implements HttpInterceptor {
     intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
       const clonedRequest = req.clone({
         setHeaders: {
           Authorization: `Bearer ${localStorage.getItem('authToken')}`
         }
       });

       return next.handle(clonedRequest);
     }
   }
   ```

### 101. **What are `Reactive Forms` in Angular?**
   **Answer**: Reactive Forms in Angular are more powerful and flexible than Template-driven Forms. They provide more control over form inputs and validation, as they are defined explicitly in the component class. Reactive forms are based on `FormGroup` and `FormControl`.

   **Code Example**:
   ```typescript
   import { Component } from '@angular/core';
   import { FormBuilder, FormGroup, Validators } from '@angular/forms';

   @Component({
     selector: 'app-reactive-form',
     template: `<form [formGroup]="form" (ngSubmit)="onSubmit()">
       <input formControlName="name" />
       <button type="submit" [disabled]="form.invalid">Submit</button>
     </form>`
   })
   export class ReactiveFormComponent {
     form: FormGroup;

     constructor(private fb: FormBuilder) {
       this.form = this.fb.group({
         name: ['', [Validators.required, Validators.minLength(3)]],
       });
     }

     onSubmit() {
       console.log(this.form.value);
     }
   }
   ```

### 102. **What is the `ngFor` directive in Angular?**
   **Answer**: `ngFor` is a structural directive used to loop over a collection (array or object) and repeat the template for each item. It is commonly used to render lists in Angular templates.

   **Code Example**:
   ```html
   <ul>
     <li *ngFor="let item of items">{{ item }}</li>
   </ul>
   ```

   **Code Example (Component)**:
   ```typescript
   export class MyComponent {
     items: string[] = ['Item 1', 'Item 2', 'Item 3'];
   }
   ```

### 103. **What is `ngOnChanges` used for in Angular?**
   **Answer**: `ngOnChanges` is a lifecycle hook that is called when any data-bound property (marked with `@Input`) changes. It is useful when you need to perform logic based on changes to input properties.

   **Code Example**:
   ```typescript
   @Component({
     selector: 'app-my-component',
     template: `<p>{{ name }}</p>`
   })
   export class MyComponent implements OnChanges {
     @Input() name: string;

     ngOnChanges(changes: SimpleChanges) {
       console.log('Previous Value:', changes.name.previousValue);
       console.log('Current Value:', changes.name.currentValue);
     }
   }
   ```

### 104. **What is `ngZone` in Angular?**
   **Answer**: `ngZone` is a service in Angular that allows you to execute code inside or outside of the Angular zone, which manages change detection. `ngZone` helps to optimize performance by preventing unnecessary change detection cycles.

   **Code Example**:
   ```typescript
   import { Component, NgZone } from '@angular/core';

   @Component({
     selector: 'app-my-component',
     template: '<p>{{ message }}</p>'
   })
   export class MyComponent {
     message: string;

     constructor(private ngZone: NgZone) {
       this.ngZone.runOutsideAngular(() => {
         setTimeout(() => {
           this.ngZone.run(() => {
             this.message = 'This is running inside Angular Zone!';
           });
         }, 1000);
       });
     }
   }
   ```

### 105. **What is the difference between `ngOnInit` and `ngAfterViewInit` in Angular?**
   **Answer**:
   - **`ngOnInit`**: This lifecycle hook is called after Angular has initialized the component's input properties. It is called once and is useful for component initialization.
   - **`ngAfterViewInit`**: This lifecycle hook is called after Angular has fully initialized the component’s view and child views. It is useful for manipulating or interacting with the component’s view elements.

   **Code Example**:
   ```typescript
   export class MyComponent implements OnInit, AfterViewInit {
     ngOnInit() {
       console.log('ngOnInit called');
     }

     ngAfterViewInit() {
       console.log('ngAfterViewInit called');
     }
   }
   ```

### 106. **How do you perform lazy loading in Angular?**
   **Answer**: Lazy loading in Angular allows modules to be loaded only when needed, reducing the initial load time of the application. It is configured by using the `loadChildren` property in the route configuration.

   **Code Example**:
   ```typescript
   const routes: Routes = [
     { path: 'admin', loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule) }
   ];
   ```

### 107. **What are `custom pipes` in Angular?**
   **Answer**: Custom pipes in Angular are user-defined pipes that can be used to transform data before displaying it in the view. Pipes can be used for formatting, filtering, or transforming data.

   **Code Example**:
   ```typescript
   @Pipe({
     name: 'reverse'
   })
   export class ReversePipe implements PipeTransform {
     transform(value: string): string {
       return value.split('').reverse().join('');
     }
   }
   ```

   **Code Example (Usage in Template)**:
   ```html
   <p>{{ 'Hello' | reverse }}</p>
   ```

---

