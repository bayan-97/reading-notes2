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
1- `module.exports = 'Hello world';`

2- ``var msg = require('./Messages.js');`

`console.log(msg);`
3- 

