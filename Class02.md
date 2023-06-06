# Class 02

## Express REST API


### [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

#### 1. Classes are a template for creating ____.
Classes are a template for creating objects.


#### 2. Can a class declaration be hoisted?
No, class declarations cannot be hoisted in JavaScript, including ES6 classes. Hoisting is a mechanism where variable and function declarations are moved to the top of their containing scope during the compilation phase. However, class declarations are not hoisted like function declarations are.


#### 3. How would you describe a constructor and contextual “this” to a non-technical friend?
. A constructor is like a blueprint or set of instructions to create objects of the same type.
. It defines how the object should be created and what properties and methods it should have.
. Contextual "this" is like a pronoun that refers to the current object you're working with.
. It allows you to access and modify the properties and methods of that specific object.



### [Using Express Routing](https://expressjs.com/en/guide/routing.html)

#### 1. Within Express, what does routing refer to?
Routing refers to how an application’s endpoints (URIs) respond to client requests.


#### 2. What is the difference between a route path and a route method?
The route path defines the URL pattern for an endpoint, while the route method specifies the type of request (e.g., GET,PUT, POST) that can be made to that endpoint. Together, they create a route in Express for handling specific requests.


#### 3. When is it appropriate to add (next) as a parameter to a route handler and what must you do if (next) has been passed to your middleware as a parameter?
Add next as a parameter in a route handler when you want to pass control to the next middleware or route handler.
If next is passed to your middleware, invoke it within your middleware to allow the request to proceed to the next middleware or route handler.



### [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)

#### 1. What is an Express Router?
An Express Router is a middleware that allows you to organize and modularize your routes into separate files or modules, providing a more structured and maintainable approach for handling different endpoints and their corresponding logic in an Express application.

#### 2. By what mean do we initialize (  express.Router()  ) in an express server?
To initialize express.Router() in an Express server, you call the express.Router() function directly. This creates a new instance of the Router class provided by Express, which allows you to define and configure routes specific to that router instance.


#### 3. What do we use route middleware for?
Route middleware in Express is used to perform additional operations or logic on incoming requests before they reach the final route handler. It provides a way to modularize and organize common functionality that needs to be executed for specific routes or groups of routes.
