
#  map method

 *The map() method  by it can enter to array to each elelment and index it .return array by array has the same lenght 
`const array1 = [1, 4, 9, 16];`

`// pass a function to map`

`const map1 = array1.map(x => x * 2);`

`console.log(map1);`
`// expected output: Array [2, 8, 18, 32]`



#  reduce method
 
*The reduce() method take  each* *element of the array, resulting in single output value. and has 
accumulator to response by it 

`const array1 = [1, 2, 3, 4];`
`const reducer = (accumulator, currentValue) => accumulator + currentValue;`
`// 1 + 2 + 3 + 4`

`console.log(array1.reduce(reducer));`

`// expected output: 10`

#  how to use superagent() to fetch data from a URL and log the result

## async / await


An async function is a function declared with the async keyword. Async functions are instances of the AsyncFunction constructor, and the await keyword is permitted within them. The async and await keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.

 `async function cities( cityName){`

`let result= await superagent.get(`https://geocode.xyz/${cityName}?json=1`)`
`console.log("longt",result.body.longt,"latt",result.body.latt)`

 `}`
  `cities( "Amman")`
## then()


 The then() method in JavaScript has been defined in the Promise API and is used to deal with asynchronous tasks such as an API call. 
 
 Previously, callback functions were used instead of this function which made the code difficult to maintain.

 [](https://miro.medium.com/max/700/0*DWhzyIKngpmwYoDR.png)


  `function getCharacters(){`
  `superagent.get("https://swapi.dev/api/people/1/ ")`
  `.then(data=>{`
  `let charNew= {characterName:data.body.name`
  ` ,valueUrl:data.body.url}`
  `console.log( charNew)`

  `})`
 

`}`
`getCharacters()`


# promises

A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason.

 This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

 [](https://mdn.mozillademos.org/files/15911/promises.png)

#  Are all callback functions considered to be Asynchronous? Why or Why Not
 


 Simply taking a callback doesn't make a function asynchronous.Calling the argument function is performed as part of normal step-by-step sequential execution of statements 
 
 .but for a function to be asynchronous it needs to perform an asynchronous operation.




## Which 3 things had you heard about previously and now have better clarity on?

1- superagent idea
2- callback 
3- then method
## Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1. async / await syntax
2. npm
3. node.js 

## What are you most excited about trying to implement or see how it works?

## What is Node.js 

- Node.js is an open source server environment
- Node.js is free
- Node.js runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.)
- Node.js uses JavaScript on the server
![](https://www.freecodecamp.org/news/content/images/2019/06/1_sYPllpcAZLHmpuQSRPuO0Q.png)

`Node.js uses asynchronous programming!`

## Node.js handles a file request:

1.  Sends the task to the computer's file system.
2. Ready to handle the next request.
3. When the file system has opened and read the file, the server returns the content to the client.

- Node.js Do

1. Node.js can generate dynamic page content
2. Node.js can create, open, read, write, delete, and close files on the server.

## npm


 - *npm consists of three distinct components*:

   - **the website**: Use the website to discover packages, set up profiles, and manage other aspects of your npm experience. For example, you can set up Orgs (organizations) to manage access to public or private packages.

   - **the Command Line Interface (CLI)**:  
The CLI runs from a terminal, and is how most developers interact with npm.

   - **the registry**:
The registry is a large public database of JavaScript software and the meta-information surrounding it.

## Use npm to

- Adapt packages of code for your apps, or incorporate packages as they are.

- Download standalone tools you can use right away.

- Run packages without downloading using npx.

- Share code with any npm user, anywhere.

- Restrict code to specific developers.




