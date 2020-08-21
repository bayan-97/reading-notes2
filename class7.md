# the table 
A table represents information in a grid format.
Examples of tables include financial reports, TV
schedules, and sports results.
## Basic Table St ructure

- `<table>`
The `<table>` element is used
to create a table. The contents
of the table are written out row
by row.
- `<tr>`
You indicate the start of each
row using the opening `<tr>` tag.
(The tr stands for table row.)
It is followed by one or more
- `<td>` elements (one for each cell
in that row).
At the end of the row you use a
closing -
 `</tr>` tag.
`<td>`
Each cell of a table is
represented using a `<td>`
element. (The td stands for
table data.)
At the end of each cell you use a
closing `</td> `tag.
## Table Headings
`<th>`
The `<th>` element is used just
like the `<td>` element but its
purpose is to represent the
heading for either a column or
a row. (The th stands for table
heading.)
Even if a cell has no content,
you should still use a `<td>` or
`<th>` element to represent
the presence of an empty cell
otherwise the table will not
render correctly. (The first cell
in the first row of this example
shows an empty cell.)
Using `<th>` elements for
headings helps people who
use screen readers, improves
the ability for search engines
to index your pages, and also
enables you to control the
appearance of tables better
when you start to use CSS.
You can use the scope attribute
on the `<th>` element to indicate
whether it is a heading for a
column or a row. It can take the
values: row to indicate a heading
for a row or col to indicate a
heading for a column.
## Long Tables
There are three elements that
help distinguish between the
main content of the table and
the first and last rows (which can
contain different content).
These elements help people
who use screen readers and also
allow you to style these sections
in a different manner than the
rest of the table (as you will see
when you learn about CSS).
`<thead>`
The headings of the table should
sit inside the` <thead> `element.
`<tbody>`
The body should sit inside the
`<tbody>` element.
`<tfoot>`
The footer belongs inside the
`<tfoot>` element.
# the object
creating and object constructor notataion:
``function Person``(first,`` ``last, age, eye)````{``
 ` this.firstName` = `first;`
  `this.lastName` `= last;`
 `this.age = age;`
 ` this.eyeColor` `= eye;`
`}`
## update and object 
``object.````property="```park";`
## CREATING MANY OBJECTS:
CONSTRUCTOR NOTATION
Sometimes you will want several objects to represent similar things.
Object constructors can use a function as a template for creating objects.
First, create the template with the object's properties and methods.

A function called Hotel will be used as a template
for creating new objects that represent hotels. Like
all functions, it contains statements. In this case,
they add properties or methods to the object.
The function has three parameters. Each one sets
the value of a property in the object. The methods
will be the same for each object created using this
function.

## THIS (IT IS A KEYWORD)
The keyword this is commonly used inside functions and objects.
Where the function is declared alters what this means. It always refers
to one object, usually the object in which the function operates.
- A FUNCTION IN GLOBAL SCOPE
When a function is created at the top level of a script
(that is, not inside another object or function), then it
is in the global scope or global context.
The default object in this context is the window
object. so when this is used inside a function in the
global context it refers to the window object.
Below, this is being used to return properties of the
window object 
function windowSize() {
var width= this . innerWidth;
var height = this .innerHeight;
return [height, width];
Under the hood, the this keyword is a reference to
the object that the function is created inside.

-  FUNCTIONS, METHODS & OBJECTS
GLOBAL VARIABLES
All global variables also become properties of the
window object. so when a function is in the global
context, you can access global variables using the
window object, as well as its other properties.
Here, the showWi dth () function is in global scope,
and this.width refers to the width variable:
`var width = .``600;var` `shape = ``{width: 300};``var` `showWidth-=` `function()`
`document .`
`write (this.`
`width)) ;`
`};`

Here, the function would write a value of 600 into the
page (using the document object's write() method).
## RECAP: STORING DATA

In JavaScript, data is represented using name/value pairs.
To organize your data, you can use an array or object to group a set of
related values. In arrays and objects the name is also known as a key.

- VARIABLES
A variable has just one key (the variable name)
and one va lue.
Variable names are separated from their value by an
equals sign (the assignment operator):
`var hotel= `
`'Quay' ;`
To retrieve the value of a variable, use its name:
II This ret r i eves Quay:
hotel ;
When a variable has been declared but has not yet
been assigned a va lue, it is undefined.
If the var keyword is not used, the variable is
declared in global scope (you should always use it).
- ARRAYS
Arrays can store multiple pieces of information.
Each piece of information is separated by a comma.
The order of the values is important because items
in an array are assigned a number (called an index).
Values in an array are put in square brackets,
separated by commas:
`var hotels=` 
`[`
`'Quay ' ,`
`' Park' ,`
`' Beach' ,`
`'Bloomsbury'`
`]`
You can think of each item in the array as another
key/value pair, the key is the index number, and the
values are shown in the comma-separated list.
To retrieve an item, use its index number:
II Thi s retrieves Park:
hote 1 s [l] ;
If a key is a number, to retrieve the value you must
place the number in square brackets.
Generally speaking, arrays are the only times when
the key would be a number.
## arry are objects
n array is an object, and like any other object in Java, it is constructed out of main storage as the program is running. The array constructor uses different syntax than other object constructors:

new type[ length ]
This names the type of data in each cell and the number of cells.

Once an array has been constructed, the number of cells it has does not change. Here is an example:

`int[] data =`
` new int[10];`
## THE WINDOW OBJECT
The window object represents the current
browser window or tab. It is the topmost object
in the Browser Object Model, and it contains
other objects that tell you about the browser.
![](https://slideplayer.com/slide/8112414/25/images/10/Window+Object+Methods.jpg)
## THE DOCUMENT OBJECT MODEL:THE DOCUMENT OBJECT
The Document Object Model (DOM) is a programming API for HTML and XML documents. It defines the logical structure of documents and the way a document is accessed and manipulated. In the DOM specification, the term "document" is used in the broad sense - increasingly, XML is being used as a way of representing many different kinds of information that may be stored in diverse systems, and much of this would traditionally be seen as data rather than as documents. Nevertheless, XML presents this data as documents, and the DOM may be used to manage this data.
![](https://simplesnippets.tech/wp-content/uploads/2018/10/what-is-document-object-model-in-JS-featured-image.jpg)
-PROPERTY
document.title
document. lastModified

document .URL

document.domain
-  DESCRIPTION
  
Title of current document

Date on which document was last modified

Returns string containing URL of current document

Returns domain of current document.


## GLOBAL OBJECTS:STRING OBJECT
Whenever you have a value that is a string, you can use the properties
and methods of the String object on that valu e. This example stores the
phrase "Home sweet home " in a variable.
![](https://slideplayer.com/slide/3408090/12/images/9/String+Methods+These+methods+are+called+using+the+dot+notation%3A.jpg)
## GLOBAL OBJECTS:NUMBER OBJECT
**Whenever you have a value that is a number,
you can use the methods and properties of the
Number object on it.**
![](https://cdn.educba.com/academy/wp-content/uploads/2020/02/Methods-in-tabular-format.png)
## MATH OBJECT
The Math object has properties and methods
for mathematical constants and functions.
![](https://slideplayer.com/slide/14547002/90/images/2/12.3+Math+Object.jpg)
## RANDOM NUMBERS

This example is designed to
generate a random whole
number between 1 and 10.
The Math object's random()
method generates a random
number between 0 and 1 (with
many decimal places).
JAVASCRIPT
To get a random whole number
between 1 and 10, you need to
multiply the randomly generated
number by 10.
This number will still have many
decimal places, so you can round
it down to the nearest integer.
The floor() method is used
to specifically round a number
down (rather than up or down).
This will give you a value
between 0 and 9. You then add
1 to make it a number between 1
and 10.
`var randomNum = Math.floor((Math.random() * 10) + l);`
`var el = document.getElementByid('info');`
`el .innerHTML = '<h2>random number</h2><p>' + randomNum + 1 </p>';`
## DATE OBJECT (AND TIME)
Once you have created a Date object, the following methods let you set
and retrieve the time and date that it represents
![](https://www.brainkart.com/media/extra/EYuwTCq.jpg)



