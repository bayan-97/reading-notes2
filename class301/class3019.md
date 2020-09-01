# functional programming

**Functional programming** is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable.



**functional programming is*pure functions***



- It returns the same result if given the same arguments (it is also referred as deterministic)

``let PI = 3.14;``                   
``const calculateArea = (radius) => radius * radius * PI;``
``calculateArea(10); // returns 314.0``
- It does not cause any observable side effects.

## Pure functions benefits

 we can unit test pure functions with different contexts:


Given a parameter A → expect the function to return value B


Given a parameter C → expect the function to return value D

## Immutability

**Unchangin**g over time or unable to be changed.

When data is immutable, its state cannot change after it’s created.

 If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

 ## Referential transparency

 **pure functions + immutable data = referential transparency**

 ## Functions as first-class entities

 Functions as first-class entities can:
- refer to it from constants and variables


- pass it as a parameter to other functions


- return it as result from other functions

## Higher-order functions

1- takes one or more functions as arguments, or

2- returns a function as its result


## Filter

Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection.


 Basically, if the callback expression is true, the filter function will include the element in the result collection.
 
  Otherwise, it will not.
A simple example is when we have a collection of integers and we want only the even numbers.

``var numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];``
``var evenNumbers = [];``

``for (var i = 0; i < numbers.length; i++) {``
  ``if (numbers[i] % 2 == 0) {``
   `` evenNumbers.push(numbers[i]);}``
``}``

``console.log(evenNumbers); // (6) [0, 2, 4, 6, 8, 10]``




