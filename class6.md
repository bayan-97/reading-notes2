# the object
Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names.

1-**VARIABLES BECOME**
KNOWN AS PROPERTIES
If a variable is part of an object, it is called a
property. Properties te ll us about the object, such as
the name of a hotel or the number of rooms it has.
Each individual hotel might have a different name
and a different number of rooms.
``name : 1 Quay 1,``


2-**FUNCTIONS BECOME**
KNOWN AS METHODS
If a function is part of an object, it is called a method.
Methods represent tasks that are associated with
the object. For example, you can check how many
rooms are available by subtracting the number of
booked rooms from the total number of rooms.

``fullName : function() {``
   `` return this.firstName`` ``+ " " + ````this.lastName;``
  ``}``

  ``var person = {``
  ``firstName: "John",``
 `` lastName : "Doe",``
  ``id       : 5566,``
  ``fullName : function() {``
   `` return this.firstName ````+ " " + this.lastName;``
  ``}``
``};``
![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/How-to-Create-JavaScript-Objects-1280x720.jpg)

 A- ![](https://image.slidesharecdn.com/oojs-1229037721986393-1/95/beginning-objectoriented-javascript-15-728.jpg?cb=1229139637)
 
# THE DOM TREE IS AMODEL OF A WEB PAGE
As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes.

![](https://www.guru99.com/images/JavaScript/javascript8_1.png)
Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file).
Any changes made to the DOM tree are reflected in the browser.
# WORKING WITH THE DOM TREEAccessing

Accessing and updating the DOM tree involves two steps:
1: Locate the node that represents the element you want to work with.


2: *Use its text content *child elements, and *attributes.*
## ACCESSING ELEMENTS

DOM queries may return one element, or they may return a Nodelist,
which is a collection of nodes.
- **GROUPS OF ELEMENT NODES**
If a method can return more than one node, it will
always return a Nodelist, which is a collection of
nodes (even if it only finds one matching element).
You then need to select the element you want from
this list using an index number (which means the
numbering starts at 0 like the items in an array).
For example, several elements can have the same
tag name, so`` get El ````ementsByTagName () will`` ``always``
``return a Nodel i st.``

-**FASTEST ROUTE**
Finding the quickest way to access an element
within your web page will make the page seem
faster and/or more responsive. This usually means
evaluating the minimum number of nodes on the
way to the element you want to work with. For
example, getEl ementByld () will quickly return one
element (because no two elements on the same
page should have the same value for an id attribute),
but it can only be used when the element you want
to access has an id attribute.

METHODS THAT RETURN A SINGLE ELEMENT NODE:
``getElementByld( 1 id 1``
``)``
Selects an individual element given the value of its i d attribute .
The HTML must have an id attribute in order for it to be selectable.
``querySel ector( 1css ````selector ')``
``Uses CSS selector syntax that would select one or more element s .
This method returns only the first of the matching elements.

``... get ElementByld('one')``
``... querySelector('l i . hot ````' )``
METHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST):
``getEl ement sByClassName( ````1class 1``
``)``
Selects one or more elements given the va lue of their cl ass attribute.
The HTML must have a cl ass attribu te for it to be selectable.
This method is faster than ``querySe 1ectorA11 () .``
First supported: IE9, Firefox 3, Safari 4, Chrome 4, Opera 10
(Several browsers had partial I buggy support in earlier versions)
``getEl ementsByTagName( 1 ````tagName 1``
``)``
Selects all elements on the page with the specified tag name.
This method is faster than ``querySe 1ectorA11 ().``

(Several browsers had partial I buggy support in earlier versions)
``querySelectorAll ( 1css ````select or •)``
Uses CSS selector syntax to select one or more elements and returns all of those that match.
# NODELISTS: DOM QUERIESTHAT RETURN MORE THAN ONE ELEMENT



When a DOM method can return more than one element, it returns a
Nodelist (even if it only finds one matching element).
- A Nodelist is a collection of element nodes. Each
node is given an index number (a number that starts
at zero, just like an array).
The order in which the element nodes are stored in a
Node List is the same order that they appeared in the
HTML page.
When a DOM query returns a Nodelist, you may
want to:
• Select one element from the NodeList.
• Loop through each item in the Nodelist and
perform the same statements on each of the
element nodes.

# Here you can see four different DOM queries that all return a Nodelist.
![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-Document-Object-Model-DOM.jpg)

For each query, you can see the elements and their index numbers in the
Nodelist that is returned.
 -``getElementsByTagName('hl '```` )``
Even though this query only
returns one element. the method
still returns a Nodelist because
of the potential for returning
more than one element.

-getElementsByTagName('li ')
This method returns four
elements, one for each of the
``<li>`` elements on the page.
They appear in the same order
as they do in the HTML page.
-`` getElementsByClassName````('hot')``
This Nodelist contains only
three of the ``<li >``elements
because we are searching for
elements by the value of their
cl ass attribute, not tag name.
## SELECTING AN ELEMENT FROM A NODELIST

There are two ways to select an element from a Nodelist:
The item() method and array syntax.
Both require the index number of the element you want.
THE ;tern{) METHOD
Nodelists have a method
called item() which will return
an individual node from the
Node list.
You specify the index number
of the element you want as a
parameter of the method (inside
the parentheses).
THE ;tern{) METHOD
Nodelists have a method
called item() which will return
an individual node from the
Node list.

- SELECTING ELEMENTS USING CLASS ATTRIBUTES
The`` get ElementsByClass Name````()``
method allows you to select
elements whose c 1 ass attribute
contains a specific value.
get-elements-by-class-name .js
The method has one parameter:
the class name which is given
in quotes within the parentheses
after the method name.
Because several elements can
have the same value for their
cl ass attribute, this method
always returns a Nodelist.
``var elements = document .````getEl ementsByClassName````('hot'); II Find hot items``
``if (e lements .l ength> 2) {``
``var el = elements[2];``
``el.className = 'cool';``

-SELECTING ELEMENTS BY TAG NAME
The`` get ElementsByTagName ()``method allows you to select
elements using their tag name.

The element name is specified
as a parameter, so it is placed
inside the parentheses and is
contained by quote marks.

``var elements = document.````getElementsByTagName('li ')````; /I Find <li> elements``
``if (elements.length> O) {``
``var el = elements[O];``
``el.className = 'cool';``

- SELECTING ELEMENTS
USING CSS SELECTORS
querySe 1 ector() returns
the first element node that
matches the CSS-style selector.
querySe 1ectorA11 () returns a
Nodelist of all of the matches
Both methods take a CSS
selector as their only parameter.
## HOW TO GET/UPDATE ELEMENT CONTENT
When you select a text node, you can retrieve or amend the content of it
using the node Va 1 ue property.

``<li id="one"><em>fresh</em>````figs</li>``

``document.getElementByid( 1`` ``one 1 ).firstChild.````nextSibling. nodeValue;``
1. The ``<1i>``element node is selected using the get El ementByid () method.
2. The first child of ``<1i> ``is the ``<em>`` element.
3. The text node is the next sibling of that ``<em> ``element.
4. You have the text node and can access its contents using node Va 1 ue.
## ACCESS & UPDATE TEXTWITH TEXTCONTENT(& INN ERTEXT)
The textCon tent property allows you to
collect or update just the text that is in the
containing element (and its children).
## ACCESSING TEXT ONLY
In order to demonstrate the
difference between textContent
and i nnerText, this example
features a CSS rule to hide the
contents of the`` <em> ``element.

The script starts off by getting
the content of the first list item
using both the textContent
property and i nnerText. It then
writes the values after the list.
## ADDING ELEMENTS USING DOM MANIPULATION
DOM manipulation offers another technique
to add new content to a page (rather than
i nnerHTML). It involves three steps:
1-
CREATE THE ELEMENT
createEl ement ()
You start by creating a new
element node using the
``createElement()`` method.
This element node is stored
in a variable.
When the element node is
created, it is not yet part of the
DOM tree. It is not added to
the DOM tree until step 3.
, you will see another
method that can be used to
insert an element into the DOM
tree. The  ``insertBefore ()``
method is used to add a new
element before the selected
DOM node.

GIVE IT CONTENT ADD IT TO THE DOM
createTextNode() appendChild()
createTextNode() creates a Now that you have your element
new text node. Again, the node (optionally with some content
is stored in a variable. It can be in a text node), you can add
added to the element node using it to the DOM tree using the
the appendChi l d () method. appendChi 1 d () method.
This provides the content for the The appendChi 1 d () method
element, although you can skip allows you to specify which
this step if you want to attach an element you want this node
empty element to the DOM tree. added to, as a child of it.
## REMOVING ELEMENTS VIA DOM MANIPULATION
DOM manipulation can be used to remove
elements from the DOM tree.
1-
STORE THE ELEMENT
TO BE REMOVED IN A
VARIABLE
You start by selecting the
element that is going to be
removed and store that element
node in a variable.
You can use any of the methods
you saw in the section on DOM
queries to select the element.
2-
STORE THE PARENT OF
THAT ELEMENT IN A
VARIABLE
Next, you find the parent element
that contains the element you
want to remove and store that
element node in a variable.
The simplest way to get this
element is to use the parentNode
property of this element.
The example on the right is quite
simple, but this technique can
significantly alter the DOM tree.

3-
REMOVE THE ELEMENT
FROM ITS CONTA INING
ELEMENT
The removeChi ld() method is
used on the containing element
that you selected in step 2.
The removeChi ld() method
takes one parameter: the
reference to the element that
you no longer want.

## CREATING ATTRIBUTES &CHANGING THEIR VALUES
The className property allows
you to change the value of the
cl ass attribute. If the attribute
does not exist, it will be created
and given the specified value.

You have seen this property
used throughout the chapter
to update the status of the
list items. Below, you can see
another way to achieve the task.
The setAttribute() method
allows you to update the va lue
of any attribute. It takes two
parameters: the attribute name,
and the value for the attribute.

## REMOVING ATTRIBUTES
To remove an attribute from an
element, first select the element,
then call removeAtt r i bute () .
It has one parameter: the name
of the attribute to remove.
JAVASCRIPT
Trying to remove an attribute
that does not exist will not cause
an error, but it is good practice
to check for its existence before
attempting to remove it.
In this example, the
get El ementByld () method is
used to retrieve the first item
from this list, which has an id
attribute with a value of one.

