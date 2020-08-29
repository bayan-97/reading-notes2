# Node.js



**Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.**

## The V8 engine 

is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi.

 It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

## How Do I Install Node.js
we’ll install Node and write a couple of simple programs. We’ll also look at npm, a package manager that comes bundled with Node.

### Installing a Package Globally

1- ``npm install -g jshint``
2-This will install the jshint package globally on your system. We can use it to lint the index.js file from the previous example:

``jshint index.js``

### Installing a Package Locally

-  ``npm init -y``
-  ``npm install lodash --save``

``const _ = require('lodash');``

``const arr = [0, 1, false, 2, '', 3];``


``console.log(_.compact(arr));``

you should see [ 1, 2, 3 ] output to the terminal.


### Introducing npm, the JavaScript Package Manager
Node comes bundled with a package manager called npm. To check which version you have installed on your system, type ``npm -v.``

**In addition** to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,

000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.



## “Hello, World!” the Node.js Way

You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing.

Next, create a new file hello.js and copy in the following code:

``console.log("Hello, World!");``\

This uses Node’s built-in console module to display a message in a terminal window. To run the example, enter the following command:

node hello.js.

## Node.js Has Excellent Support for Modern JavaScript

As can be seen on this compatibility table, Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your 

JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers.




## What Is Node.js Used For?

These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. 

They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

## The following image depicts Node’s execution model:

![](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png)

## Conclusion

**JavaScript is everywhere, and Node is a vast and expansive subject.**

Nonetheless, I hope that in this article I’ve offered you the beginner-friendly, high-level look at Node.js and its main paradigms that I promised at the beginning. I also hope that when you re-read the definitions we looked at previously, things will make a lot more sense.

