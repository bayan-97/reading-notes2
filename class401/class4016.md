# Class 06

## Readings: HTTP and REST




-*** What is the advantage of an ORM, like Mongoose?***
   1. Schemas
    MongoDB is a denormalized NoSQL database. This makes it inherently schema-less as documents have varying sets of fields with different data types. While this provides your data model with flexibility as it evolves over time, it can be difficult to cope with coming from a SQL background. Mongoose defines a schema for your data models so your documents follow a specific structure with pre-defined data types.

    2. Validation
    Mongoose has built in validation for schema definitions. This saves you from writing a bunch of validation code that you have to otherwise write with the MongoDB driver. By simply including things like required:true in your schema definitions, Mongoose provides out-of-the-box validations for your collections (including data types).
How does the repository pattern compare with an ORM?
- Repositories deal with Domain/Business objects (from the app point of view), an ORM handles db objects. A business objects IS NOT a db object, first has behaviour, the second is a glorified DTO, it only holds data.
- The repository abstract the access to all storage concerns, while the ORM abstract access to a specific RDBMS

**When making a repository/facade, what flexibility do you gain?**


A common design goal is to minimize the communication and dependencies between subsystem.  


- you want to provide a simple interface to a complex subsystem. The application of design patterns often results in a lot of small classes which makes subsystems more flexible and customizable. A facade can provide a default view for clients which don't need to customize.


- you want to reduce coupling between clients-subsystems or subsystems-subsystems.

**Name 3 cloud based NoSQL Databases**


- Couchbase.
- Amazon DynamoDB.
- MongoDB.


1. Which 3 things had you heard about previously and now have better clarity on?
- mongoose middleware
Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
- lifecycle
- collections
What are you most excited about trying to implement or see how it works?
- Object Relation Mapping (ORM)


## HTTP


HTTP stands for Hypertext Transfer Protocol. It's a stateless, application-layer protocol for communicating between distributed systems, and is the foundation of the modern web.HTTP allows for communication between a variety of hosts and clients, and supports a mixture of network configurations.

1. HTTP Basics

- Communication between a host and a client occurs, via a request/response pair. The client initiates an HTTP request message, which is serviced through a HTTP response message in return. We will look at this fundamental message-pair in the next section.

![](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-request-response.png)

HTTP a stateless protocol. The communication usually takes place over TCP/IP, but any reliable transport can be used. The default port for TCP/IP is **80**, but other ports can also be used.

## URLs 


At the heart of web communications is the request message, which are sent via Uniform Resource Locators (URLs). I'm sure you are already familiar with URLs, but for completeness sake, I'll include it here. URLs have a simple structure that consists of the following components:

![](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-url-structure.png)

These request verbs are:

- GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource.
- POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.
- PUT: update an existing resource. The payload may contain the updated data for the resource.
- DELETE: delete an existing resource.


Request and Response Message Formats:

![](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-req-res-details.png)

`message = <start-line>`
         ` *(<message-header>)`
          `CRLF`
          `[<message-body>]
`
`<start-line> = Request-Line | Status-Line `
`<message-header> = Field-Name ':' Field-Value`


## Using HTTP in Web Frameworks and Libraries

- ExpressJS
If you are building web servers in NodeJS, chances are high that you've considered ExpressJS. ExpressJS was originally inspired by a Ruby Web framework, called Sinatra. As expected, the API is also equally influenced.

- jQuery Ajax
Because jQuery is primarily a client-side library, its Ajax API provides the opposite of a server-side framework. In other words, it allows you to read response messages and modify request messages. 

## REST API 


**REST** is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems and was first presented by Roy Fielding in 2000 in his famous dissertation.

- Principles of REST

    - Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.

    - Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.


    - Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.


    - Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. 
    
    In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.  

## Resource

The key abstraction of information in REST is a resource. Any information that can be named can be a resource: a document or image, a temporal service, a collection of other resources, a non-virtual object (e.g. a person), and so on. REST uses a resource identifier to identify the particular resource involved in an interaction between components.   

## Resource Methods


Another important thing associated with REST is resource methods to be used to perform the desired transition. A large number of people wrongly relate resource methods to HTTP GET/PUT/POST/DELETE methods.