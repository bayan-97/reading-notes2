# Heroku

We will use Node.js for our project. Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run 

within the Node.js runtime on any platform. First of all, of course, you need to install it. You'd better check the download page for more details. 

I'll wait until you finish, so don't worry. Is it done? Great! Now you can create your first web server. And it will be one of the easiest tasks in your life.

``var http = require("http");``

``http.createServer(function(request, response) {``
  ``response.writeHead(200, {"Content-Type": "text/plain"});``
  ``response.write("It's alive!");``
  ``response.end();``
``}).listen(3000);``

![](http://i.imgur.com/idykoj7.png)

``node server.js``


Then check it in your browser. Your new server's address, as you may guess, is http://localhost:3000/ Mine is working. How about yours? Hope, it's working too.

1- First step after Heroku installation is to log in to the system from your computer:

`heroku login`

``var http = require("http");``
``var fs = require("fs");``
``var path = require("path");``
``var mime = require("mime");``

The first one will give you the key to Node's HTTP functionality. The second one is for possibility to interact with the file system. The third one allows you to handle file paths. 

The last one allows you to determine a file's MIME-type. And it's not a part of Node.js, so we need to install third-party dependencies before using it.

 We need to create the package.json file for that purpose. It will contain project related information, such as name, version, description, and so on. For our project we will use MIME-types recognition, because it's not enough to just send the contents of a file when you use HTTP. You also need to set the Content-Type header with proper MIME-type. That's why we need this plug-in.

 2- Create the package.json file and fill it with proper information.

`` {``
  ``"name" : "blog",``
  ``"version" : "0.0.1",``
  ``"description" : "My minimalistic blog",``
  ``"dependencies" : {``
    ``"mime" : "~1.2.7"``
 `` }``
``}``

There are "name", "version", "description", and "dependencies" fields in it. The syntax is simple, as you can see. We added our "mime" plug-in and now it's time to download it. We'll use built-in Node Package Manager.

The Heroku CLI is built with the Open CLI Framework (oclif), developed within Heroku / Salesforce. oclif is available as a framework for any developer to build a large or a small CLI. The framework includes a CLI generator, automated documentation creation, and testing infrastructure.

The code for the Heroku CLI is also open source. It does not require Node.js or any other dependencies to run. Unless you install the Debian/Ubuntu package or use npm install, the CLI contains its own Node.js binary that does not conflict with other applications.

