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


1. **ecosystem**:Managed lifecycle and dependency injection for your application components.

2. **Node.js**: is an open-source, cross-platform, back-end, JavaScript runtime environment that executes JavaScript code outside a web browser. Node.js lets developers use JavaScript to write command line tools and for server-side scripting—running scripts server-side to produce dynamic web page content before the page is sent to the user's web browser. Consequently, Node.js represents a "JavaScript everywhere" paradigm, unifying web-application development around a single programming language, rather than different languages for server- and client-side scripts.

3. **V8 Engin:V8** is Google’s open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node.js, among others.



4.** Module in Node.js** is a simple or complex functionality organized in single or multiple JavaScript files which can be reused throughout the Node.js application.

5. **NPM - Node Package Manager**:
Node Package Manager (NPM) is a command line tool that installs, updates or uninstalls Node.js packages in your application

