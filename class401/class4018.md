
# class 8

## Readings: Express Routing & Connected API

1. Name 3 real world use cases where you’d want to change the request with custom middleware?

- make the password decrypted before store it in the database.
-  validate incoming cookies.
2. True or false: The route handler is middleware?
false
3. In what ways can a middleware function end the process and send data to the browser?
response and return

4. At what point in the request lifecycle can you “inject” middleware?
before respnonse the next function
5. What can cause express to error with “Request headers sent twice, cannot start a second response”
when req again and again 

1. Which 3 things had you heard about previously and now have better clarity on?
- Response Object
- Application Middleware
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?


- Request Object
3. What are you most excited about trying to implement or see how it works?

- Routing Middleware
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


`app.get('/example/b', function (req, res, next) {`
`  console.log('the response will be sent by the next function ...')`
  ``next()``
`}, function (req, res) {`
  `res.send('Hello from B!')})`

## New Router in ExpressJS


Express 4.0 comes with the new Router. Router is like a mini express application. It doesn't bring in views or settings, but provides us with the routing APIs like .use, .get, .param, and route.


 ## Application
application that has some routes and a few features. Let's run through those now.

- Basic Routes: Home, About
- Route Middleware to log requests to the console
- Route with Parameters
- Route Middleware for Parameters to validate specific parameters
- Login routes Doing a GET and POST on /login
- Validates a parameter passed to a certain route

**We'll only need two files for our application.**

- package.json  // set up our node packages
- server.js     // set up our app and build routes


## Express Router

It is a mini express application without all the bells and whistles of an express application, just the routing stuff. Let's take a look at exactly what this means. We'll go through each section of our site and use different features of the Router.

### Route Middleware router.use()

Route middleware in Express is a way to do something before a request is processed. This could be things like checking if a user is authenticated, logging data for analytics, or anything else we'd like to do before we actually spit out information to our user.



