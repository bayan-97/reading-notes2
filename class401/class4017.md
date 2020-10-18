

## What’s the difference between PUT and PATCH?
1. To make a PUT request, you need to send the two parameters

2. PATCH is used when you want to apply a partial update to the resource. 
## Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
- Postman
- Swagger
- Mocky
## Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

- swagger-ui is meant for consumption by JavaScript web projects that include module bundlers, such as Webpack, Browserify, and Rollup. Its main file exports Swagger UI's main function, and the module also includes a namespaced stylesheet at swagger-ui/dist/swagger-ui.css.

- it is a good practice to provide detailed documentation about how the client applications can connect and consume the data from an API. The coolest thing is that we are going to use a simple tool which generates documentation through the code’s comments.


## Compare and contrast SOAP and ReST
- SOAP
SOAP is a protocol which was designed before REST and came into the picture. The main idea behind designing SOAP was to ensure that programs built on different platforms and programming languages could exchange data in an easy manner. SOAP stands for Simple Object Access Protocol.

- REST
REST was designed specifically for working with components such as media components, files, or even objects on a particular hardware device. Any web service that is defined on the principles of REST can be called a RestFul web service. A Restful service would use the normal HTTP verbs of GET, POST, PUT and DELETE for working with the required components. REST stands for Representational State Transfer.


**Which 3 things had you heard about previously and now have better clarity** **on?**

- CRUD Verbs
- Swagger
**Which 3 things are you hoping to learn more about in the upcoming lecture/****demo?**

- ReST Verbs

**What are you most excited about trying to implement or see how it works?**
- SOAP

## Using middleware

**Express**is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

Middleware functions can perform the following tasks:

- Execute any code
Make changes to the request and the response objects.
- End the request-response cycle.
Call the next middleware function in the stack.
If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function. Otherwise, the request will be left hanging.
## Application-level middleware

Bind application-level middleware to an instance of the app object by using the app.use() and app.METHOD() functions, where METHOD is the HTTP method of the request that the middleware function handles (such as GET, PUT, or POST) in lowercase.

## Router-level middleware

Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().



Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers, etc.




![](https://www.tutorialspoint.com/expressjs/images/middleware_desc.jpg)


## Routing

Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing.

You define routing using methods of the Express app object that correspond to HTTP methods; for example,` app.get() `to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use` app.all()` to handle all HTTP methods and `app.use()` to specify middleware as the callback function (See Using middleware for details).

These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.##

## Route paths
Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.


## Route handlers


You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route.










