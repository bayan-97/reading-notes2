## Why would you want to run JavaScript code outside of a browser?

any JavaScript code that one writes will run in any system that has Node.js installed. **It is essentially making the "cross-platform" aspect of the Web available to everyone.**

## What is the difference between a module and a package?

 - module is a single file (or files) that are imported under one import and used
 `import my_module`

 - import my_module

`from my_package.timing.danger.internets import function_of_som`
## What does the node package manager do?

1. first and foremost, it is an online repository for the publishing of open-source Node.js projects; 

2. second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

## Provide code snippets showing 3 different ways to export a function from a node module


1-` module.exports = function (msg) { `
   ` console.log(msg);`
`};`

2-`var msg = require('./Log.js');`

`msg('Hello World');`

3- `var person = require('./Person.js');`

`var person1 = new person('James', 'Bond');`

`console.log(person1.fullName());`

## Which 3 things had you heard about previously and now have better clarity on?

1. Node.js
2. node package manager 
3. server
## Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1.ecosystem
2. interpreter
3. compiler

## What are you most excited about trying to implement or see how it works?
ecosystem



##  Test-Driven Development

**Test-driven development (TDD**) is a technique for ensuring that your code does what you think it does. 

It’s particularly relevant for JavaScript, with its cross-browser incompatibilities and hidden gotchas. 

With TDD, you express your intentions twice: once as a test, and once as production code. If the two approaches don’t match, your tests fail, and you’ve caught a bug.

## CRISPIN BENNETT JavaScript Needs Test-Driven Development

If you’ve programmed in JavaScript, you know that it’s an… interesting… language. Don’t get me wrong: I love JavaScript. I love its first-class functions, the intensive VM competition among browser makers, and how it makes the web come alive. It definitely has its good parts.

## Inheriting properties

JavaScript objects are dynamic "bags" of properties (referred to as own properties). 

JavaScript objects have a link to a prototype object. When trying to access a property of an object, the property will not only be sought on the object but on the prototype of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the prototype chain is reached.

## Inheriting "methods"


JavaScript does not have "methods" in the form that class-based languages define them. In JavaScript, any function can be added to an object in the form of a property. An inherited function acts just as any other property, including property shadowing as shown above (in this case, a form of method overriding).

When an inherited function is executed, the value of this poiJavaScript does not have "methods" in the form that class-based languages define them. In JavaScript, any function can be added to an object in the form of a property. An inherited function acts just as any other property, including property shadowing as shown above (in this case, a form of method overriding).

## this

In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called. ES5 introduced the bind() method to set the value of a function's this regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own this binding (it retains the this value of the enclosing lexical context).

## Value

A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value.

- Global context

In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.

- Function context

Inside a function, the value of this depends on how the function is called.

Since the following code is not in strict mode, and because the value of this is not set by the call, this will default to the global object, which is window in a browser.

- Class context

The behavior of this in classes and functions is similar, since classes are functions under the hood. But there are some differences and caveats.

Within a class constructor, this is a regular object. All non-static methods within the class are added to the prototype of this:

`class Example {`
`  constructor() {`
  `  const proto = Object.getPrototypeOf(this);`
    `console.log(Object.getOwnPropertyNames(proto));`
`  }`
 ` first(){}`
`  second(){}`
`  static third(){}`
`}
`

## Classes

Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components:  and class declarations.

 
### class declarations


`class Rectangle {`
 ` constructor(height, width) {`
  `  this.height = height;`
    `this.width = width;`
`  }`
`}`

### class expressions

Class expressions
A class expression is another way to define a class. Class expressions can be named or unnamed. 

The name given to a named class expression is local to the class's body. (it can be retrieved through the class's (not an instance's) name property, though).

