# the text in the html 
**many of  tags provide extra meaning**
**and allow browsers to show users the**
**appropriate structure for the pag.**

## heading 

**HTML has six "levels" of headings:**
*Browsers display the contents of*
*headings at different sizes*
``<h1><h2><h3><h4><h5><h6>``

## a paragraph
*To create a paragraph, surround*
*the words that make up the*
paragraph with an opening ``<p>``
tag and closing ``</p>`` tag.

## Bold & It alic

1-By enclosing words in the tags
``<b>`` and ``</b>`` we can make
characters appear bold.
2-By enclosing words in the tags
``<i>`` and ``</i>`` we can make
characters appear italic.

## Superscript & Subscript

- the ``<sup>`` element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 2^2.

-  The ``<sub>`` element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H20.

## Line Breaks & Horizontal Rules


A- As you have already seen, the
browser will automatically show
each new paragraph or heading
on a new line. But if you wanted
to add a line break inside the
middle of a paragraph you can
use the line break tag ``<br />``.

b- To create a break between
themes — such as a change of
topic in a book or a new scene
in a play — you can add a
horizontal rule between sections
using the ``<hr />`` tag.

## Strong & Emph asis


- The use of the ``<strong>``
element indicates that its
content has strong importance.
For example, the words
contained in this element might
be said with strong emphasis.
By default, browsers will show
the contents of a ``<strong>``
element in bold.
- The ``<em>`` element indicates
emphasis that subtly changes
the meaning of a sentence.
By default browsers will show
the contents of an ``<em> ``element
in italic.

## Quotations

1- The ``<blockquote>`` element is
used for longer quotes that take
up an entire paragraph. Note
how the ``<p>`` element is still
used inside the ``<blockquote>``
element.
2- The ``<q>`` element is used for
shorter quotes that sit within
a paragraph. Browsers are
supposed to put quotes around
the ``<q>`` element, however
Internet Explorer does not —
therefore many people avoid
using the ``<q>`` element.

##  Abbreviations &Acronyms

- If you use an abbreviation or
an acronym, then the ``<abbr>``
element can be used. A title
attribute on the opening tag is
used to specify the full term.


## Citations & Definitions

-When you are referencing a
piece of work such as a book,
film or research paper, the
``<cite>`` element can be used
to indicate where the citation is
from.


- The first time you explain some
new terminology (perhaps an
academic concept or some
jargon) in a document, it is
known as the defining instance
of it.

### Visual Editors & Their Code views

- Visual editors often resemble
word processors. Although
each editor will differ slightly,
there are some features that
are common to most editors
that allow you to control the
presentation of text.

- Code views show you the code
created by the visual editor so
you can manually edit it, or so
you can just enter new code
yourself. It is often activated
using a button with an icon
that says HTML or has angled
brackets. White space may be
added to the code by the editor
to make the code easier to read.

# css 

**CSS allows you to create rules that control the**
**way that each individual box (and the contents**
**of that box) is presented.**
- CSS works by associating rules with HTML elements. These rules govern
how the content of specified elements should be displayed. A CSS rule
contains two parts: a selector and a declaration.
![im]( https://filedn.com/ltOdFv1aqz1YIFhf4gTY8D7/ingus-info/BLOGS/CSS-selectors/css-selectors.jpg)
``h1 p {``
``font-family: Arial;``
``color: yellow;}``

This *rule* indicates that all ``<h1>``,
``<p>``  elements
should be shown in the Arial
typeface, in a yellow color.

**Properties** indicate the aspects
of the element you want to
change. For example, color, font,
width, height and border.

**Values** specify the settings
you want to use for the chosen
properties. For example, if you
want to specify a color property
then the value is the color you
want the text in these elements
to be.
the selector type:


![img](https://codeandwork.github.io/courses/cs/media/css-selectors.jpg)



css be located :


![img](https://www.bitdegree.org/learn/storage/media/images/8c4493d3-110c-4a95-8b70-7626ce2d2f4e.o.jpg)

-internal: You can also include CSS rules
within an HTML page by placing
them inside a ``<style> ``element,
which usually sits inside the
``<head>`` element of the page. 

- External CSS:
- 
``<link rel="stylesheet" type="text/css" href="mystyle.css">``

- ``<link>`` external-css.html HTML
The ``<link>`` element can be used
in an HTML document to tell the
browser where to find the CSS
file used to style the page. It is an
empty element (meaning it does
not need a closing tag), and it
lives inside the ``<head>`` element.
It should use three attributes:
**href**
This specifies the path to the
CSS file (which is often placed in
a folder called css or styles).
**type**
This attribute specifies the type
of document being linked to. The
value should be text/css.
**rel**
This specifies the relationship
between the HTML page and
the file it is linked to. The value
should be stylesheet when
linking to a CSS file.
### Why use External Style Sheets?

once the user has
downloaded the CSS stylesheet,
the rest of the site will load
faster. If you want to make a
change to how your site appears,
you only need to edit the one
CSS file and all of your pages
will be updated. For example,
you can change the style of
every ``<h1>`` element by altering.


# color in the css
**The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways**:
 1-rgb values
 2-hex codes
 3-color names
 ![](https://www.c-sharpcorner.com/article/temp/51970/Images/11.jpg)

*color to differt placed:*
1-color to the text 
2-color background  ![](https://media.geeksforgeeks.org/wp-content/uploads/rgba-2.png)
**When picking foreground and background
colors, it is important to ensure that there is
enough contrast for the text to be legible.**

*every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker*
![](https://qph.fs.quoracdn.net/main-qimg-dc1d62cc8f996909c0339e401d2b39c4.webp)


# the java script 

A script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement.
``var today= new Date{);``

## comments
**You should write comments to explain what your code does.**
SINGLE-LINE COMMENTS
In a single-line comment, anything that follows the
two forward slash characters I/ on that line will not
be processed by the JavaScript interpreter. Singleline
comments are often used for short descriptions
of what the code is doing.`` // Display the appropriate greeti ng based on the current time``

## varible
A script will have to temporarily
store the bits of information it
needs to do its job. It can store this
data in *variables*.
 ![](https://tutorial.techaltum.com/images/js-variables.jpg)
 ### data type

 JavaScript variables can hold many data type:

 - NUMERIC DATA TYPE
The numeric data type handles
numbers.
-STRING DATA TYPE
The strings data type consists of
letters and other characters.

- BOOLEAN DATA TYPE
Boolean data types can have one
of two va lues: true or false.

**USING A VARIABLE TO**
**STORE A NUMBER:** ``var x = 5;``
``var y = 6;``
**USING A VARIABLE TO**
**STORE A STRING** :`` var person = "John Doe";``
``var answer = 'Yes I am!';``
**Note**  the string is placed
inside quote marks. The quotes
can be single or double quotes,
but they must match. If you start
with a single quote, you must end
with a single quote, and if you
start with a double quote, you
must end with a double quote.

**USING QUOTES INSIDE A STRING**
use a technique
called escaping the quotation
characters. This is done by
using a backwards slash (or
"backslash") before any type of
quote mark that appears within
a string (as shown on the fourth
line of this code sample).``'<a href=\"sale .html\">25% off l</a>' ;``


**USING A VARIABLE TO STORE A BOOLEAN**
``nStock = true;``
``shipping= fa l se;``

**The general rules for constructing names for variables (unique identifiers) are**:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter
- Names can also begin with $ and _ (but we will not use it in this tutorial)
- Names are case sensitive (y and Y are different variables)
- Reserved words (like JavaScript keywords) cannot be used as names
## array 
An array is a special type of variable. It doesn't
just store one value; it stores a list of values.
If you have a list of items 
``colors ['white', 'black', ' custom ']; ``

- Values in an array are accessed as if they are in
a numbered list. It is important to know that the
numbering of this list starts at zero (not one).
NUMBERING ITEMS IN
AN ARRAY Each item in an array is
automatically given a number
called an index. This can be used
to access specific items in the
``array.``
``var col ors;``
``colors= ['whi te ' ,``
``'black ' ,``
``' custom'];``
INDEX VALUE
o 'white '
1  'black'
2 ' custom'
- ACCESSING ITEMS IN
AN ARRAY
To retrieve the third item on the
list, the array name is specified
along with the index number in
square brackets.``var itemThr ee;``
                ``itemThree = col ors [ 2] ;``
  -  NUMBER OF ITEMS IN
AN ARRAY each array has a property called
length, which holds the number
of items in the array.      ``var numColors ;``
                          ``numColors =colors. length; ``

  **ACCESSING & CHANGINGALUES IN AN ARRAy**
   ``var cars = ["Saab", "Volvo", "BMW"];``
    ``cars[0] = "Opel";``
``document.getElementById("demo").innerHTML = cars[0]; ``       





# the expression
*An expression evaluates into (results in) a single value. Broadly speaking.*
## the exp and opr

*there are two types of expressions*

1- EXPRESSIONS THAT JUST ASSIGN avarible

`var color = 'beige';`

2-EXPRESSIONS THAT USE TWO OR
MORE VALUES TO RETURN A 
SINGLE VALUE.

`var area = 3 * 2;`

*Expressions rely on things called operators; they allow programmers to
create a single value from one or more values.
JavaScript contains the following mathematical
operators, which you can use with numbers.
You may remember some from math class.*

There is just one string operator: the+ symbol.
It is used to join the strings on either side of it.
new string concatenation.`(+)`

## OPERATORS
Expressions rely on things called operators; they allow programmers to
create a single value from one or more values.

**ARITHMETIC OPERATORS**
JavaScript contains the following mathematical
operators, which you can use with numbers.
You may remember some from math class.
 ![](https://contribute.geeksforgeeks.org/wp-content/uploads/arithmetic-operators.png)

 ``var subtotal (13 + 1) * 5; II Subtotal is 70``
``var shipping 0.5 * (13 + 1) ; II Shipping is 7``

**string operator**
There is just one string operator: the+ symbol.
It is used to join the strings on either side of it.
new string concatenation.`(+)`
``var firstName = 'Ivy ' ;``
``var lastName = ' Stone' ;``
``var ful l Name = f irstName + l astName; //IvyStone``

``var number = 12;``
``var street= 'Ivy Road';``
``var add = number + street;//12Ivy Road ``

``var cost l = '7';``
``var cost2 = '9 ' ;``
``var total = costl + cost2 ;//79``


## make the descion


if statment 
 ![](https://media.geeksforgeeks.org/wp-content/uploads/if.png)

very often when you write code, you want to perform different actions for different decisions.
You can use conditional statements in your code to do this. In JavaScript we have the following conditional statements:

- Use if to specify a block of code to be executed, if a specified condition is true
- Use else to specify a block of code to be executed, if the same condition is false
  

``if (condition) {``
  ``//  block of code to be executed if the condition is true``
``} else {``
 `` //  block of code to be executed if the condition is false``
``}``


 ![](https://cdn.programiz.com/sites/tutorial2program/files/working-java-if-statement.jpg)

##  Comparison operators
  *Comparison operators are used in logical statements to determine equality or difference between variables or values.*

  
![pic](https://cdn.javascripttutorial.net/wp-content/uploads/2016/11/JavaScript-Comparison-Operators.png)

USING COMPARISON OPERATORS
``var hasPas sed = score >= pass ;``
you can evaluate two variables using a
comparison operator to return a
true or f al se value.


**comparison with expretion**
``var comparison= (score!+ score2) > (highScorel + highScore2);``


## Logical Operators
*Logical operators are used to determine the logic between variables or values.*
![pic](https://qph.fs.quoracdn.net/main-qimg-cf34fc11d82779735b4021de7dd31e50)

1-AND

![pic](https://miro.medium.com/max/718/1*sJBMUURVOsAEesan68S0RA.png)

2- OR
![pic](https://res.cloudinary.com/practicaldev/image/fetch/s--xttyf7r3--/c_imagga_scale,f_auto,fl_progressive,h_500,q_auto,w_1000/https://cl.ly/7d9cf8370380/Image%25202018-11-15%2520at%25209.59.47%2520AM.png)

