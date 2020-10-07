
#  map method

 *The map() method creates a new array populated with the results of calling a*
  *provided function on every element in the calling array.*
  A Map object iterates its elements in insertion order — a for...of loop returns an array of [key, value] for each iteration.

`const array1 = [1, 4, 9, 16];`

`// pass a function to map`

`const map1 = array1.map(x => x * 2);`

`console.log(map1);`
`// expected output: Array [2, 8, 18, 32]`



#  reduce method
 
*The reduce() method executes a reducer function (that you provide) on each* *element of the array, resulting in single output value.*
Reduce comes with some terminology such as reducer & accumulator. The accumulator is the value that we end with and the reducer is what action we will perform in order to get to one value.

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



