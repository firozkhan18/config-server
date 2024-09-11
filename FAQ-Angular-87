### Angular Interview Questions and Answers

#### **Part 1: Basic Concepts**

**Question 1: What’s the use of Angular?**

*Angular* is a TypeScript-based open-source web application framework developed by Google. It is used to build dynamic, single-page web applications (SPAs). Angular provides a robust platform with tools and libraries for front-end development, such as dependency injection, data binding, and routing. It aims to enhance the development experience by providing a structured approach to building complex applications with reusable components and services.

**Question 2: What are directives in Angular?**

*Directives* in Angular are special markers on elements or attributes that tell the Angular framework to do something with the DOM elements. They extend HTML capabilities by adding behavior to DOM elements. Directives come in three types: components, structural directives, and attribute directives.

**Question 3: Explain the different types of Angular directives.**

- **Components**: The most commonly used directives that have a template and are used to build the user interface. They control a patch of the screen and include logic and styling. Example: `<app-header></app-header>`.
  
- **Structural Directives**: Change the DOM layout by adding or removing elements. They typically start with an asterisk (*) in the template. Examples include `*ngIf`, `*ngFor`, and `*ngSwitch`.

- **Attribute Directives**: Change the appearance or behavior of an element, component, or another directive. They do not alter the DOM structure but modify the behavior or styling. Examples include `ngClass`, `ngStyle`, and custom directives created using `@Directive`.

**Question 4: Explain the importance of NPM and Node_Modules folder.**

*Node Package Manager (NPM)* is used for managing dependencies in JavaScript projects. The `node_modules` folder contains all the packages and their dependencies that your project relies on. This folder is crucial as it provides the libraries and tools needed for the application, such as Angular and its related packages. It helps in modularizing code and managing versions of different packages.

**Question 5: Explain the importance of the `package.json` file in Angular.**

The `package.json` file is essential in an Angular project as it manages the project’s dependencies, scripts, and metadata. It contains:

- **Dependencies**: Lists the packages required for the project.
- **DevDependencies**: Lists packages needed for development and testing.
- **Scripts**: Defines commands like `ng serve`, `ng build`, etc.
- **Metadata**: Includes project name, version, author, and license information.

**Question 6: What is TypeScript and why do we need it?**

*TypeScript* is a superset of JavaScript that adds static typing to the language. It is used in Angular to provide type safety, improved tooling, and better code organization. TypeScript helps in catching errors during development rather than at runtime, supports modern JavaScript features, and enhances code readability and maintainability.

**Question 7: Explain the importance of Angular CLI.**

*Angular CLI (Command Line Interface)* is a tool that simplifies the development process by automating tasks. It helps in scaffolding Angular projects, generating components, services, and other Angular constructs. It also supports building, testing, and deploying Angular applications efficiently with commands like `ng generate`, `ng serve`, and `ng build`.

**Question 8: Explain the importance of Components and Modules.**

- **Components**: Components are the fundamental building blocks of Angular applications. Each component consists of an HTML template, a TypeScript class, and CSS styles. They encapsulate the view and the logic related to that view, promoting reusability and modularity.

- **Modules**: Modules are containers for a cohesive block of code dedicated to a specific application domain, workflow, or feature. They help in organizing and grouping related components, directives, pipes, and services. The `AppModule` is the root module, and other feature modules can be imported to add functionality.

**Question 9: What is a decorator in Angular?**

A *decorator* in Angular is a special kind of declaration that can attach metadata to a class, method, property, or parameter. This metadata helps Angular understand how to process and use that class. Examples of decorators include `@Component`, `@NgModule`, `@Injectable`, and `@Directive`.

**Question 10: What are Annotation or Metadata?**

*Annotations* or *metadata* are key-value pairs that provide additional information about classes, methods, or properties. They are used by Angular to configure how classes should behave or interact within the framework. For instance, `@Component` decorator specifies metadata about a component, such as its selector, template, and styles.

**Question 11: What is a template?**

In Angular, a *template* is an HTML view that defines the structure and layout of the user interface. Templates can include Angular directives and bindings that dynamically display data and respond to user actions. They are associated with components and control how data is presented in the view.

**Question 12: Explain the four types of Data bindings in Angular.**

- **Interpolation**: Used to bind data from the component to the view. Syntax: `{{ data }}`. Example: `<p>{{ user.name }}</p>`.
  
- **Property Binding**: Binds the value of a property to an HTML element's property. Syntax: `[property]="expression"`. Example: `<img [src]="imageUrl">`.
  
- **Event Binding**: Binds an event (like clicks) to a method in the component. Syntax: `(event)="method()"`. Example: `<button (click)="save()">Save</button>`.
  
- **Two-Way Binding**: Synchronizes data between the component and the view. Syntax: `[(ngModel)]="property"`. Example: `<input [(ngModel)]="user.name">`.

**Question 13: Explain the architecture of Angular.**

Angular’s architecture is based on several core concepts:

- **Modules**: Organize an application into cohesive blocks of code.
- **Components**: Control a portion of the user interface.
- **Templates**: Define the view for a component.
- **Services**: Provide reusable business logic and data.
- **Dependency Injection**: Allows Angular to manage service instances and inject them into components.
- **Routing**: Manages navigation between views or components.
- **Directives**: Extend HTML with additional functionality.
- **Pipes**: Transform data in templates.

**Question 14: What is SPA in Angular?**

A *Single Page Application (SPA)* is a web application that interacts with the user by dynamically rewriting the current page, rather than loading entire new pages from the server. Angular facilitates SPA development by providing routing and client-side rendering capabilities.

**Question 15: How to implement SPA in Angular?**

Implementing SPA in Angular involves:

1. **Setting up Angular Router**: Define routes and configure navigation.
2. **Creating Components**: Build components for different views.
3. **Using RouterOutlet**: Place `<router-outlet>` in the template to display routed components.
4. **Configuring Routes**: Define routes in the `AppRoutingModule` and map them to components.

Example:

```typescript
// app-routing.module.ts
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutComponent } from './about/about.component';

const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'about', component: AboutComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

**Question 16: How to implement routing in Angular?**

Routing in Angular is implemented using the `RouterModule` which allows navigation between different components or views. Steps:

1. **Install RouterModule**: Import it in the application module.
2. **Define Routes**: Create a routing module with route definitions.
3. **Configure Routes**: Use `<router-outlet>` in the main template to display routed content.
4. **Navigate**: Use Angular router directives or `Router` service to navigate programmatically.

**Question 17: Explain Lazy Loading.**

*Lazy Loading* is a design pattern used to delay the loading of a module until it is required. It helps in reducing the initial load time of an application by loading only the necessary code and deferring the rest.

**Question 18: How to implement Lazy Loading in Angular?**

Lazy loading is implemented by:

1. **Creating Feature Modules**: Define Angular modules that can be lazy-loaded.
2. **Setting Up Routes**: Use the `loadChildren` property in the route configuration to specify which module to load.

Example:

```typescript
// app-routing.module.ts
const routes: Routes = [
  { path: 'feature', loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule) }
];
```

**Question 19: Define Services.**

*Services* in Angular are used to provide shared logic and data across multiple components. They are classes annotated with `@Injectable` that can be injected into components or other services using Angular’s dependency injection system.

**Question 20: What is Dependency Injection?**

*Dependency Injection (DI)* is a design pattern used in Angular to manage service instances and inject them into components or other services. It promotes loose coupling and enhances testability by decoupling the creation and management of service instances from the components that use them.

**Question 21: How to implement Dependency Injection?**

To implement DI:

1. **Define a Service**: Create a class and annotate it with `@Injectable`.
2. **Provide the Service**

: Register the service in a module or component.
3. **Inject the Service**: Use constructor injection to receive the service in a component or another service.

Example:

```typescript
// data.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  getData() { return ['data1', 'data2']; }
}

// component.ts
import { Component, OnInit } from '@angular/core';
import { DataService } from './data.service';

@Component({
  selector: 'app-my-component',
  template: `<div *ngFor="let item of data">{{ item }}</div>`
})
export class MyComponent implements OnInit {
  data: string[];

  constructor(private dataService: DataService) {}

  ngOnInit() {
    this.data = this.dataService.getData();
  }
}
```

**Question 23: What’s the benefit of Dependency Injection?**

The benefits of Dependency Injection include:

- **Decoupling**: Components are not responsible for creating service instances.
- **Testability**: Easier to mock services for unit testing.
- **Maintainability**: Centralized service configuration and management.
- **Flexibility**: Ability to swap out implementations easily.

**Question 24: Differentiate between `ng serve` and `ng build`.**

- **`ng serve`**: Compiles the application and starts a development server. It provides live reloading and is used for local development.
  
- **`ng build`**: Compiles the application into a production-ready bundle. It generates static files and does not include a development server.

**Question 25: Explain the `--prod` parameter in `ng build`.**

The `--prod` parameter is used to build the application for production. It enables production optimizations like minification, Ahead-of-Time (AOT) compilation, and tree-shaking to reduce the bundle size and improve performance.

---

### **Part 2: ViewChild and ViewChildren**

**Question 26: Explain ViewChild and ViewChildren.**

- **`@ViewChild`**: Used to access a single child component, directive, or DOM element from a parent component. It allows direct interaction with the child element.

- **`@ViewChildren`**: Used to access multiple child components, directives, or DOM elements in a parent component. It provides a query list of matching elements.

**Question 27: Why do we need Template reference variables?**

*Template reference variables* are used to access DOM elements or directives within a template. They are defined using `#variableName` and can be used to interact with the element or pass it to methods.

Example:

```html
<input #myInput />
<button (click)="doSomething(myInput.value)">Click me</button>
```

**Question 28: What is Content Projection?**

*Content Projection* allows you to pass content into a component’s view from the parent component. It enables you to create reusable components where the content can be dynamically inserted.

**Question 29: Explain Content Projection Slot.**

*Content Projection Slots* are placeholders defined in a component’s template where projected content will be inserted. They are denoted by `<ng-content></ng-content>`.

Example:

```html
<!-- Parent Component -->
<app-card>
  <p>This content will be projected into the card component</p>
</app-card>

<!-- Card Component -->
<div class="card">
  <ng-content></ng-content>
</div>
```

**Question 30: What is ContentChild and ContentChildren?**

- **`@ContentChild`**: Used to access a single content child element or directive from the projected content in a component.

- **`@ContentChildren`**: Used to access multiple content child elements or directives from the projected content in a component. It provides a query list.

**Question 31: ViewChild vs ViewChildren vs ContentChild vs ContentChildren?**

- **`ViewChild`**: Accesses a single child element or directive within the same view.
  
- **`ViewChildren`**: Accesses multiple child elements or directives within the same view.
  
- **`ContentChild`**: Accesses a single element or directive projected into the component’s content.
  
- **`ContentChildren`**: Accesses multiple elements or directives projected into the component’s content.

---

### **Part 3: Angular Component Lifecycle**

**Question 32: Explain the importance of Component Lifecycle.**

The *Component Lifecycle* is crucial for managing a component's initialization, updates, and destruction phases. It provides hooks like `ngOnInit`, `ngOnChanges`, `ngOnDestroy` to perform tasks such as data fetching, clean-up, and reacting to changes.

**Question 33: Explain events and sequence of component lifecycle.**

Lifecycle events include:

- **`ngOnChanges`**: Called before `ngOnInit` when input properties change.
- **`ngOnInit`**: Called once the component is initialized.
- **`ngDoCheck`**: Called during every change detection run.
- **`ngAfterContentInit`**: Called after content (ng-content) has been projected.
- **`ngAfterContentChecked`**: Called after every check of projected content.
- **`ngAfterViewInit`**: Called after the component’s view and child views are initialized.
- **`ngAfterViewChecked`**: Called after every check of the component’s view and child views.
- **`ngOnDestroy`**: Called just before Angular destroys the component.

**Question 34: Constructor vs ngOnInit()**

- **Constructor**: Initializes class members and injects dependencies. It is called before Angular initializes the component’s input properties.

- **`ngOnInit()`**: Angular lifecycle hook called after Angular initializes the component’s input properties. It’s used for additional initialization tasks like data fetching.

---

### **Part 4: HTTP Calls, Emitters & Routing**

**Question 35: How to make HTTP calls using Angular?**

Use Angular’s `HttpClient` to make HTTP calls. Inject `HttpClient` into your service or component and use its methods to interact with APIs.

Example:

```typescript
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  constructor(private http: HttpClient) {}

  getData() {
    return this.http.get('https://api.example.com/data');
  }
}
```

**Question 36: What is the need of Subscribe function?**

The `subscribe()` function is used to handle the asynchronous responses from an observable. It allows you to react to data emissions, errors, or completion signals from the observable.

Example:

```typescript
this.dataService.getData().subscribe(data => {
  console.log(data);
});
```

**Question 37: How to handle errors when HTTP fails?**

Use `catchError` operator in RxJS to handle errors and provide fallback mechanisms or user-friendly messages.

Example:

```typescript
import { catchError } from 'rxjs/operators';
import { throwError } from 'rxjs';

this.dataService.getData().pipe(
  catchError(error => {
    console.error('Error occurred', error);
    return throwError(error);
  })
).subscribe(data => {
  console.log(data);
});
```

**Question 38: How to pass data between components?**

Data can be passed between components using:

- **@Input() and @Output()**: For parent-child component communication.
- **Services**: For sharing data across unrelated components.
- **Router Parameters**: For passing data during navigation.

**Question 39: What are input, output, and event emitters?**

- **@Input()**: Decorator for binding data from parent to child components.
  
- **@Output()**: Decorator for emitting events from child to parent components.
  
- **Event Emitters**: An instance of `EventEmitter` used to create custom events.

**Question 40: How to pass data during routing?**

Use route parameters or query parameters to pass data during routing.

Example:

```typescript
// Defining route with parameters
{ path: 'user/:id', component: UserComponent }

// Navigating with parameters
this.router.navigate(['/user', 1]);

// Accessing parameters in component
import { ActivatedRoute } from '@angular/router';

constructor(private route: ActivatedRoute) {}

ngOnInit() {
  this.route.params.subscribe(params => {
    console.log(params['id']);
  });
}
```

**Question 41: Is it a good practice to pass data using services?**

Yes, using services for data sharing is a good practice. It allows for:

- **Decoupling**: Components don’t need to know about each other.
- **Reusability**: Data and logic are centralized.
- **Maintainability**: Easier to manage and test.

---

### **Part 5: Angular Pipes**

**Question 42: What is the need of Angular Pipes?**

*Pipes* are used to transform data in Angular templates. They help in formatting, filtering, and sorting data for display purposes.

**Question 43: Can you name some built-in Angular pipes?**

- **DatePipe**: Formats dates.
- **UpperCasePipe**: Converts text to uppercase.
- **LowerCasePipe**: Converts text to lowercase.
- **CurrencyPipe**: Formats numbers as currency.
- **DecimalPipe**: Formats numbers with decimal points.

**Question 44: How to create Custom pipes in Angular?**

Custom pipes are created using the `@Pipe` decorator. Define a class with `transform` method to implement the transformation logic.

Example:

```typescript
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({
  name: 'reverse'
})
export class ReversePipe

 implements PipeTransform {
  transform(value: string): string {
    return value.split('').reverse().join('');
  }
}
```

---

### **Part 6: RxJS**

**Question 45: What is the full form of RxJS?**

*RxJS* stands for *Reactive Extensions for JavaScript*.

**Question 46: What is the purpose of RxJS?**

RxJS provides a framework for reactive programming using observables. It allows you to work with asynchronous data streams and manage events, HTTP responses, and other async operations with ease.

**Question 47: What are Observables and Observers?**

- **Observables**: Objects that emit values over time. They provide a way to handle async data streams and events.
  
- **Observers**: Functions or objects that consume the values emitted by observables. They handle data, errors, and completion events.

**Question 48: Explain the use of Subscribe with sample code.**

The `subscribe()` method is used to listen to data emitted by an observable. It accepts up to three functions for handling next values, errors, and completion.

Example:

```typescript
this.dataService.getData().subscribe(
  data => console.log(data),
  error => console.error(error),
  () => console.log('Completed')
);
```

**Question 49: How to unsubscribe in RxJS?**

Unsubscribe from observables to prevent memory leaks, especially in Angular components. Use the `unsubscribe()` method on a subscription object.

Example:

```typescript
import { Subscription } from 'rxjs';

export class MyComponent implements OnDestroy {
  private subscription: Subscription;

  constructor(private dataService: DataService) {
    this.subscription = this.dataService.getData().subscribe(data => console.log(data));
  }

  ngOnDestroy() {
    this.subscription.unsubscribe();
  }
}
```

**Question 50: Explain the concept of operators with sample code.**

*Operators* are functions that transform, filter, or combine observables. They are used with `pipe()` method on observables.

Example:

```typescript
import { map, filter } from 'rxjs/operators';

this.dataService.getData().pipe(
  filter(data => data.length > 0),
  map(data => data.map(item => item.toUpperCase()))
).subscribe(transformedData => console.log(transformedData));
```

**Question 51: How to install RxJS?**

RxJS is typically included with Angular by default. To install or update RxJS, use:

```bash
npm install rxjs
```

**Question 52: Differentiate between Promise and RxJS.**

- **Promise**: Represents a single value that is eventually resolved or rejected. Suitable for a single async operation.

- **Observable**: Represents a stream of values over time. Provides multiple values, supports operators, and can be canceled.

**Question 53: In Angular where have you used RxJS?**

RxJS is used in Angular for handling asynchronous operations such as HTTP requests, event handling, and reactive forms.

**Question 54: Which operators have you used from RxJS?**

Commonly used RxJS operators include:

- **map**: Transforms values.
- **filter**: Filters values based on a condition.
- **mergeMap**: Maps values to observables and merges them.
- **catchError**: Catches errors in observable streams.

**Question 55: What is the Push/Reactive vs Pull/Imperative?**

- **Push/Reactive**: Data is pushed to the observer (e.g., using observables). Reactive programming handles data as it arrives.

- **Pull/Imperative**: Data is pulled or requested manually (e.g., using promises). You request data when needed.

---

### **Part 7: Interceptors**

**Question 56: What are Interceptors in Angular?**

*Interceptors* are used to intercept and modify HTTP requests and responses. They allow you to handle tasks like authentication, logging, and error handling globally.

**Question 57: How to implement Interceptors?**

To implement an interceptor:

1. **Create an Interceptor**: Implement `HttpInterceptor` and override `intercept` method.
2. **Provide the Interceptor**: Register it in `providers` array of the module.

Example:

```typescript
import { Injectable } from '@angular/core';
import { HttpInterceptor, HttpRequest, HttpHandler, HttpEvent } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
    const authReq = req.clone({
      setHeaders: { Authorization: 'Bearer my-token' }
    });
    return next.handle(authReq);
  }
}
```

**Question 58: Give some uses of Interceptors.**

- **Authentication**: Add authentication tokens to requests.
- **Logging**: Log request and response details.
- **Error Handling**: Catch and handle HTTP errors globally.
- **Caching**: Cache HTTP responses.

**Question 59: Can we provide multi-Interceptors?**

Yes, multiple interceptors can be provided by adding them to the `HTTP_INTERCEPTORS` array in the module’s `providers` list.

Example:

```typescript
import { HTTP_INTERCEPTORS } from '@angular/common/http';

@NgModule({
  providers: [
    { provide: HTTP_INTERCEPTORS, useClass: AuthInterceptor, multi: true },
    { provide: HTTP_INTERCEPTORS, useClass: LoggingInterceptor, multi: true }
  ]
})
export class AppModule { }
```

---

### **Part 8: Angular Validations**

**Question 60: What are two ways of doing validation in Angular?**

- **Template-driven forms**: Use Angular directives and template syntax to perform validations.
- **Reactive forms**: Use the `FormControl`, `FormGroup`, and `FormBuilder` classes to manage form controls and validations programmatically.

**Question 61: Template-driven forms VS Reactive Forms?**

- **Template-driven forms**: Simpler to use and suitable for simple forms. Validation is defined in the template using directives.

- **Reactive forms**: More powerful and scalable, especially for complex forms. Validation is defined programmatically in the component.

**Question 62: In what situations you will use what?**

- Use **template-driven forms** for simple, less dynamic forms.
- Use **reactive forms** for complex forms with dynamic validation and more control over form state.

**Question 63: Explain template reference variables.**

*Template reference variables* are used to reference DOM elements or directives within a template. They are defined using `#variableName` and can be accessed in the component’s template.

Example:

```html
<input #myInput />
<button (click)="doSomething(myInput.value)">Click me</button>
```

**Question 64: How do we implement Template-driven forms?**

1. **Import FormsModule**: Import `FormsModule` in your module.
2. **Create a Form**: Use `ngModel` and `ngForm` in the template.
3. **Add Validators**: Use Angular’s built-in validators in the template.

Example:

```html
<form #myForm="ngForm">
  <input name="name" ngModel required />
  <button type="submit" [disabled]="myForm.invalid">Submit</button>
</form>
```

**Question 65: How do we implement Reactive forms?**

1. **Import ReactiveFormsModule**: Import `ReactiveFormsModule` in your module.
2. **Create a FormGroup**: Define a form model in the component using `FormBuilder` or `FormGroup`.
3. **Add Validators**: Use validators in the form model.

Example:

```typescript
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

export class MyComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.myForm = this.fb.group({
      name: ['', Validators.required]
    });
  }
}
```

**Question 66: How can we implement composite validations?**

Composite validations involve combining multiple validators to form complex validation logic. Use Angular’s built-in validators along with custom validators.

Example:

```typescript
import { ValidatorFn, AbstractControl } from '@angular/forms';

export function compositeValidator(): ValidatorFn {
  return (control: AbstractControl): { [key: string]: any } | null => {
    const isValid = // custom validation logic
    return isValid ? null : { 'composite': true };
  };
}
```

**Question 67: How to create dynamic validation?**

Dynamic validation involves adding or removing validators based on user actions or other conditions. Use the `setValidators` method to modify validators dynamically.

Example:

```typescript
this.myForm.get('name').setValidators([Validators.required, Validators.minLength(5)]);
this.myForm.get('name').updateValueAndValidity();
```

**Question 68: How to check if overall validation and specific validations are good?**

Use `FormGroup` and `FormControl` methods:

- **`form.valid`**: Checks if the form is valid.
- **`form.get('controlName').valid`**: Checks if a specific control is valid.
- **`form.get('controlName').errors`**: Retrieves validation errors for a specific control.

**Question 69: Can you talk about some inbuilt validators?**

- **`Validators.required`**: Ensures the control is not empty.
- **`Validators.minLength(length: number)`**: Ensures the control value has a minimum length.
- **`Validators.maxLength(length: number)`**: Ensures the control value does not exceed a maximum length.
- **`Validators.pattern(pattern: string | RegExp)`**: Ensures the control value matches a specified pattern

.

**Question 70: What are custom validators?**

*Custom validators* are user-defined functions that implement custom validation logic. They are used to enforce complex or unique validation rules.

Example:

```typescript
import { AbstractControl, ValidatorFn } from '@angular/forms';

export function forbiddenNameValidator(nameRe: RegExp): ValidatorFn {
  return (control: AbstractControl): { [key: string]: any } | null => {
    const forbidden = nameRe.test(control.value);
    return forbidden ? { 'forbiddenName': { value: control.value } } : null;
  };
}
```

---

### **Part 9: Angular Forms**

**Question 71: What are Angular Forms?**

*Angular Forms* are a way to manage user input and form validation in Angular applications. Angular provides two main approaches: Template-driven and Reactive forms.

**Question 72: Explain Template-driven forms.**

*Template-driven forms* are defined directly in the template using directives such as `ngModel` and `ngForm`. They are simpler and more suitable for basic forms.

Example:

```html
<form #myForm="ngForm">
  <input name="name" ngModel required />
  <button type="submit" [disabled]="myForm.invalid">Submit</button>
</form>
```

**Question 73: Explain Reactive forms.**

*Reactive forms* are defined programmatically in the component class using `FormGroup`, `FormControl`, and `FormBuilder`. They offer more control and scalability for complex forms.

Example:

```typescript
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

export class MyComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.myForm = this.fb.group({
      name: ['', Validators.required]
    });
  }
}
```

**Question 74: What is FormGroup?**

*FormGroup* is a class in Angular that tracks the value and validation status of a group of `FormControl` instances. It is used to manage and validate multiple form controls together.

**Question 75: What is FormControl?**

*FormControl* is a class in Angular that tracks the value and validation status of a single form control. It represents individual input elements within a form.

**Question 76: What is FormBuilder?**

*FormBuilder* is a service that provides convenient methods to create `FormGroup` and `FormControl` instances. It simplifies the creation and management of reactive forms.

**Question 77: Explain FormArray.**

*FormArray* is a class in Angular that manages an array of `FormControl`, `FormGroup`, or `FormArray` instances. It allows dynamic forms with varying numbers of controls.

Example:

```typescript
import { FormArray, FormBuilder, FormGroup, Validators } from '@angular/forms';

export class MyComponent {
  myForm: FormGroup;

  constructor(private fb: FormBuilder) {
    this.myForm = this.fb.group({
      items: this.fb.array([])
    });
  }

  get items(): FormArray {
    return this.myForm.get('items') as FormArray;
  }

  addItem() {
    this.items.push(this.fb.control('', Validators.required));
  }
}
```

---

### **Part 10: Angular Routing**

**Question 78: What is Angular Routing?**

*Angular Routing* is a mechanism that enables navigation between different views or components within an Angular application. It allows users to navigate between different parts of the application based on URLs.

**Question 79: Explain the Router Module.**

*RouterModule* is an Angular module that provides routing capabilities. It includes services and directives to define routes, handle navigation, and manage routing-related tasks.

**Question 80: How to define routes in Angular?**

Routes are defined in an array of route objects, which is then passed to the `RouterModule.forRoot()` method in the `imports` array of an Angular module.

Example:

```typescript
const routes: Routes = [
  { path: 'home', component: HomeComponent },
  { path: 'about', component: AboutComponent },
  { path: '**', redirectTo: 'home' }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

**Question 81: Explain the use of RouterLink.**

`RouterLink` is a directive used in templates to create navigation links. It binds to a route path and updates the URL when clicked.

Example:

```html
<a routerLink="/home">Home</a>
<a routerLink="/about">About</a>
```

**Question 82: What is RouterOutlet?**

`RouterOutlet` is a directive used to display the routed component's view. It acts as a placeholder where the routed components will be rendered.

**Question 83: How to pass parameters in Angular routes?**

Parameters can be passed using route parameters or query parameters. Define parameters in the route path and access them using `ActivatedRoute`.

Example:

```typescript
// Define route with parameters
{ path: 'user/:id', component: UserComponent }

// Navigate with parameters
this.router.navigate(['/user', 1]);

// Access parameters in component
import { ActivatedRoute } from '@angular/router';

constructor(private route: ActivatedRoute) {}

ngOnInit() {
  this.route.params.subscribe(params => {
    console.log(params['id']);
  });
}
```

**Question 84: Explain route guards.**

*Route Guards* are interfaces that determine whether a route can be activated or deactivated. They are used to protect routes based on conditions like authentication or permissions.

- **`CanActivate`**: Determines if a route can be activated.
- **`CanDeactivate`**: Determines if a route can be deactivated.
- **`CanActivateChild`**: Determines if a child route can be activated.
- **`CanLoad`**: Determines if a module can be loaded lazily.

Example:

```typescript
import { Injectable } from '@angular/core';
import { CanActivate, Router } from '@angular/router';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {
  constructor(private router: Router) {}

  canActivate(): boolean {
    const isAuthenticated = // check authentication
    if (isAuthenticated) {
      return true;
    } else {
      this.router.navigate(['/login']);
      return false;
    }
  }
}
```

**Question 85: Explain Lazy Loading.**

*Lazy Loading* is a technique to load modules only when they are needed, rather than loading all modules at startup. It improves application performance and reduces initial load time.

Example:

```typescript
const routes: Routes = [
  { path: 'admin', loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule) }
];
```

**Question 86: How to implement Lazy Loading?**

1. **Create a feature module** with its own routing.
2. **Configure lazy loading** in the main routing module using `loadChildren`.

Example:

```typescript
// admin-routing.module.ts
const routes: Routes = [
  { path: '', component: AdminComponent }
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class AdminRoutingModule { }

// app-routing.module.ts
const routes: Routes = [
  { path: 'admin', loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule) }
];
```

**Question 87: What is Preloading Strategy?**

*Preloading Strategy* controls how lazy-loaded modules are preloaded after the initial application load. Angular provides several strategies like `PreloadAllModules` to preload all lazy-loaded modules.

Example:

```typescript
import { PreloadAllModules, RouterModule, Routes } from '@angular/router';

@NgModule({
  imports: [
    RouterModule.forRoot(routes, { preloadingStrategy: PreloadAllModules })
  ],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

---

Feel free to ask for more details or additional topics!
