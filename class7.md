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
