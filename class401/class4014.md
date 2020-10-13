# class 4

## Readings: Advanced Mongo/Mongoose

## Why would a developer choose to make data models?

1. Higher Quality
Just as architects consider blueprints before constructing a building, you should consider data before building an app. 
2. Reduced cost
You can build applications at lower cost via data models
3. Clearer scope
A data model provides a focus for determining scope. 

## What purpose do CRUD operations serve?

CREATE, READ, UPDATE, DELETE
1. CREATE
To create resources in a REST environment, we most commonly use the HTTP POST method. POST creates a new resource of the specified resource type.

2. READ
To read resources in a REST environment, we use the GET method. Reading a resource should never change any information - it should only retrieve it. If you call GET on the same information 10 times in a row, you should get the same response on the first call that you get on the last call.

3. UPDATE
PUT is the HTTP method used for the CRUD operation, Update.

4. DELETE
The CRUD operation Delete corresponds to the HTTP method DELETE. It is used to remove a resource from the system.

## What kind of database is Postgres? What kind of database is MongoDB?
database is Postgres:SQL
database is MongoDB:objed(UDI)
## What is Mongoose and why do we need it?

Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

## Which 3 things had you heard about previously and now have better clarity on

1.database
data model
2. database
data model
3. schemal

## Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1. Non SQL (NoSQL)
2. MongoDB
3. Mongoose

## What are you most excited about trying to implement or see how it works?

Non SQL (NoSQL)


# The Repository Design Pattern

Repository pattern separates the data access logic and maps it to the business entities in the business logic. Communication between the data access logic and the business logic  is done through interfaces.

![](https://cubettech.com/wp-content/uploads/2015/07/Reposiory-Design-Pattern.png)


- The separation of data access from business logic have many benefits. Some of them are:

- Centralization of the data access logic makes code easier to maintain

- Business and data access logic can be tested separately

- Reduces duplication of code

- A lower chance for making programming errors

# What do we need to build?

In order for our application to use Repositories, first we need to set things up.
We are going to need:

UserRepository
EloquentUserRepository
A way to bind UserRepository and EloquentUserRepository

- Project structure

It’s pretty bad practice to just dump stuff in a random file or leave things in the wrong directory. As your project gets bigger, things will become a mess and everything will be unmaintainable.
Instead, we are going to create a new directory called app/lib to store all of this kind of stuff.
In order for this directory to be included in the autoload, you also need to add it to your composer.json file.
In the classmap array, add your new directory:

Code:

`"autoload": {`
`"classmap": [`
`"app/lib"`
`]`
`}`

-  Creating the User Repository

The first thing to create is the UserRepository.php interface inside app/lib/myapp/storage/User directory.
- Creating the Eloquent User Repository

- Creating the Service Provider

Next we need to create the Service Provider which will bind the two repositories together.

- Implementing the Repository in the Controller

Now we can start using the Repository in the UserController.

## Testing Node.js + Mongoose with an in-memory database


**In-memory database pros & cons**

- Pros:

No need for mocks: Your code is directly executed using the in-memory database, exactly the same as using your regular database.
Faster development: Given that I don't need to build a mock for every operation and outcome but only test the query, I found the development process to be faster and more straightforward.
More reliable tests: You're testing the actual code that will be executed on production, instead of some mock that might be incorrect, incomplete or outdated.
Tests are easier to build: I'm not an expert in unit testing and the fact that I only need to seed the database and execute the code that I need to test made the whole process a lot easier to me.
Cons:

- The in-memory database probably needs seeding
More memory usage (dah)
Tests take longer to run (depending on your hardware).

 1. Setup & Install dependencies

Run npm init to setup your project

2.  Write code to test

3. Product schema


`const mongoose = require('mongoose');`


`const productSchema = new mongoose.Schema({`
  `  name: { type: String, required: true },`
   ` price: { type: Number, required: true },`
    `description: { type: String }`
`});`

`module.exports = mongoose.model('product', productSchema);`


4. Product service

`const productModel = require('../models/product');`

`module.exports.create = async (product) => {`
`    if (!product)`
 `throw new Error('Missing product');`

  `  await productModel.create(product);`




5.  Configure jest
First, we'll add the test script to the package.json:
`"scripts": {`
   ` "test": "jest --runInBand ./test"`
`}`



6.  In-memory database handling
I wrote a module that executes some basic operations that I'll use to handle the in-memory database.


`const mongoose = require('mongoose');`
`const { MongoMemoryServer } = require('mongodb-memory-server');`

`const mongod = new MongoMemoryServer();`

`module.exports.connect = async () => {`
`    const uri = await mongod.getConnectionString();`

   ` const mongooseOpts = {`
   `     useNewUrlParser: true,`
     `   autoReconnect: true,`
       ` reconnectTries: Number.MAX_VALUE,`
       ` reconnectInterval: 1000`
`    };`

`    await mongoose.connect(uri, mongooseOpts);`
`}`


        `module.exports.closeDatabase = async () => {`
`    await mongoose.connection.dropDatabase();`
 `   await mongoose.connection.close();`
`    await mongod.stop()`;
}

/**
 * Remove all the data for all db collections.
 */
`module.exports.clearDatabase = async () => {`
    `const collections = mongoose.connection.collections;`

    `for (const key in collections) {`
      `const collection = collections[key];`
        `await collection.deleteMany();`
    `}`
}`


7. Write some tests
And finally we test our product service with the following code:


`const mongoose = require('mongoose');`

`const dbHandler = require('./db-handler');`
`const productService = require('../src/services/product');`
`const productModel = require('../src/models/product');`

/**
 * Connect to a new in-memory database before running any tests.
 */
`beforeAll(async () => await dbHandler.connect());`

/**
 * Clear all test data after every test.
 */
`afterEach(async () => await dbHandler.clearDatabase());
`
/**
 * Remove and close the db and server.
 */
`afterAll(async () => await dbHandler.closeDatabase());`

/**
 * Product test suite.
 */
`describe('product ', () => {`

    /**
     * Tests that a valid product can be created through the productService without throwing any errors.
     */
 `   it('can be created correctly', async () => {`
        `expect(async () => await productService.create(productComplete))`
           ` .not`
            `.toThrow();`
``    });`
`});`

/**
 * Complete product example.
 */
`const productComplete = {`
    `name: 'iPhone 11',`
  `  price: 699,`
   ` description: 'A new dual‑camera system captures more of what you see and love. '`
`};`






