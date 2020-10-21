

# class 9


1. How does route prefixing work with an external routing module?

Simple applications can define all their routes in a single configuration file - usually config/routes.yaml (see Creating Routes). However, in most applications it’s common to import routes definitions from different resources: PHP annotations in controller files, YAML or XML files stored in some directory. 
  Prefixing the URLs of Imported Routes¶
You can also choose to provide a “prefix” for the imported routes. For example, suppose you want to prefix all application routes with /site (e.g. /site/blog/{slug} instead of /blog/{slug}).

2. When routing, what’s the difference between app.get('/data/:id') and app.get('/data/:name')?

the request prams differt it  id ` /data/:id ` it name `/data/:name`

3. Explain how Express handles routing conflicts?
Execute any code.
Make changes to the request and the response objects.
End the request-response cycle.
Call the next middleware function in the stack.

4. What are the ways that a browser can send “data” or request variables to an HTTP server

- As a suffix on the URL given by the ACTION attribute
- As a multipart MIME message

1. Which 3 things had you heard about previously and now have better clarity on?

Routing
Route Prefixing
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
Routing
Route Prefixing
3. What are you most excited about trying to implement or see how it works?

Request “Params”


`express.json([options])`

This is a built-in middleware function in Express. It parses incoming requests with JSON payloads and is based on body-parser.

Returns middleware that only parses JSON and only looks at requests where the Content-Type header matches the type option. This parser accepts any Unicode encoding of the body and supports automatic inflation of gzip and deflate encodings.

A new body object containing the parsed data is populated on the request object after the middleware (i.e. req.body), or an empty object ({}) if there was no body to parse, the Content-Type was not matched, or an error occurred.


`express.raw([options])`

This is a built-in middleware function in Express. It parses incoming request payloads into a Buffer and is based on body-parser.

Returns middleware that parses all bodies as a Buffer and only looks at requests where the Content-Type header matches the type option. This parser accepts any Unicode encoding of the body and supports automatic inflation of gzip and deflate encodings.

A new body Buffer containing the parsed data is populated on the request object after the middleware (i.e. req.body), or an empty object ({}) if there was no body to parse, the Content-Type was not matched, or an error occurred.

`express.Router([options])`
propity
caseSensitive	Enable case sensitivity.	Disabled by default, treating “/Foo” and “/foo” as the same.

`express.static(root, [options])`

The root argument specifies the root directory from which to serve static assets. The function determines the file to serve by combining req.url with the provided root directory. When a file is not found, instead of sending a 404 response, it instead calls next() to move on to the next middleware, allowing for stacking and fall-backs.

## Middleware

Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.


Pre middleware functions are executed one after another, when each middleware calls next.


`const schema = new Schema(..);`
`schema.pre('save', function(next) {`
`  if (foo()) {`
 `   console.log('calling next!');`
`    // ``return next()`;` will make sure the rest of this function ``doesn't run`
`    /*return*/ next();`
`  }`
`  // Unless you comment out the `return` above, 'after next' will ``print`
``  console.log('after next');`
`});`

- Middleware are useful for atomizing model logic. Here are some other ideas:

- complex validation
- removing dependent documents (removing a user removes all his blogposts)
- asynchronous defaults
- asynchronous tasks that a certain action triggers


`schema.post('save', function(error, doc, next) {`
`  if (error.name === 'MongoError' && error.code === 11000) {`
  `  next(new Error('There was a duplicate key error'));`
`  } else {`
` `  ` next();`
`  }``
`});`

## Aggregation Hooks

You can also define hooks for the `Model.aggregate()` function. In aggregation middleware functions, this refers to the Mongoose Aggregate object. For example, suppose you're implementing soft deletes on a Customer model by adding an isDeleted property. To make sure` aggregate() `calls only look at customers that aren't soft deleted, you can use the below middleware to add a $match stage to the beginning of each aggregation pipeline.

## Subdocuments

Subdocuments are documents embedded in other documents. In Mongoose, this means you can nest schemas in other schemas. Mongoose has two distinct notions of subdocuments: arrays of subdocuments and single nested subdocuments.

Subdocuments have save and validate middleware just like top-level documents. `Calling save()` on the parent document triggers the
` save()` middleware for all its subdocuments, and the same for `validate()` middleware.

## Finding a Subdocument
Each subdocument has an `_id` by default. Mongoose document arrays have a special id method for searching a document array to find a document with a given _id.

## Adding Subdocs to Arrays
MongooseArray methods such as push, unshift, addToSet, and others cast arguments to their proper types transparently.


## Populate
MongoDB has the join-like $lookup aggregation operator in versions >= 3.2. Mongoose has a more powerful alternative called `populate()`, which lets you reference documents in other collections.

Population is the process of automatically replacing the specified paths in the document with document(s) from other collection(s). We may populate a single document, multiple documents, a plain object, multiple plain objects, or all objects returned from a query.

## Setting Populated Fields

You can manually populate a property by setting it to a document. The document must be an instance of the model your ref property refers to.

`Story.findOne({ title: 'Casino Royale' }, function(error, story) {`
 ` if (error) {`
   ` return handleError(error);`
`  }`
`  story.author = author;`
  `console.log(story.author.name); // prints "Ian Fleming"`
`});`


**What If There's No Foreign Document?**


Mongoose populate doesn't behave like conventional SQL joins. When there's no document, story.author will be null. This is analogous to a left join in SQL.

## Populating multiple existing documents

If we have one or many mongoose documents or even plain objects (like mapReduce output), we may populate them using the Model.`populate()` method. This is what Document#`populate() `and Query#`populate()` use to populate documents.