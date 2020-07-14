#the form
Why Forms?
The best known form on the web is probably
the search box that sits right in the middle of
Google's homepage.
## How Forms Work
A user fills in a form and then presses a button
to submit the information to the server.
## Form Structure
![](https://i.stack.imgur.com/OH3R7.jpg)
<form>
Form controls live inside a
<form> element. This element
should always carry the action
attribute and will usually have a
method and id attribute too.
action
Every <form> element requires
an action attribute. Its value
is the URL for the page on the
server that will receive the
information in the form when it
is submitted.
method
Forms can be sent using one of
two methods: get or post.
With the get method, the values
from the form are added to
the end of the URL specified in
the action attribute. The get
method is ideal for:
●● short forms (such as search
boxes)
●● when you are just retrieving
data from the web server
(not sending information that
should be added to or deleted
from a database)
<form action="http://www.example.com/subscribe.php"
method="get">
<p>This is where the form controls will appear.
</p>
</form>
chapter-07/form-structure.html HTML
Form Structure
With the post method the
values are sent in what are
known as HTTP headers. As a
rule of thumb you should use the
post method if your form:
●● allows users to upload a file
●● is very long
●● contains sensitive data
(e.g. passwords)
●● adds information to, or
deletes information from, a
database
If the method attribute is not
used, the form data will be sent
using the get method.

``<input>``
The ``<input>`` element is used
to create several different form
controls. The value of the type
attribute determines what kind
of input they will be creating.
- type="text"
When the type attribute has a
value of text, it creates a singleline
text input.
- name
When users enter information
into a form, the server needs to
know which form control each
piece of data was entered into.
(For example, in a login form, the
server needs to know what has
been entered as the username
and what has been given as the
password.) Therefore, each form
control requires a name attribute.
The value of this attribute
identifies the form control and is
sent along with the information
they enter to the server.
- maxlength
You can use the maxlength
attribute to limit the number
of characters a user may enter
into the text field. Its value is the
number of characters they may
enter. For example, if you were
asking for a year, the maxlength
attribute could have a value of 4.
``<textarea>``
The ``<textarea>`` element
is used to create a mutli-line
text input. Unlike other input
elements this is not an empty
element. It should therefore have
an opening and a closing tag.
Any text that appears between
the opening ``<textarea>`` and
closing ``</textarea>`` tags will
appear in the text box when the
page loads.
``<input>``
type="checkbox"
Checkboxes allow users to select
(and unselect) one or more
options in answer to a question.
- name
The name attribute is sent to
the server with the value of the
option(s) the user selects. When
a question provides users with
options for answers in the form
of checkboxes, the value of the
name attribute should be the
same for all of the buttons that
answer that question.
- value
The value attribute indicates
the value sent to the server if this
checkbox is checked.
checked
The checked attribute indicates
that this box should be checked
when the page loads. If used, its
value should be checked.


``<select>``
- size
You can turn a drop down select
box into a box that shows more
than one option by adding the
size attribute. Its value should
be the number of options you
want to show at once. In the
example you can see that three
of the four options are shown.
Unfortunately, the way that
browsers have implemented this
attribute is not perfect, and it
should be tested throroughly if
used (in particular in Firefox and
Safari on a Mac).
- multiple
You can allow users to select
multiple options from this list by
adding the multiple attribute
with a value of multiple.
It is a good idea to tell users if
they can select more than one
option at a time. It is also helpful
to indicate that on a PC they
should hold down the control key
while selecting multiple options
and on a Mac they should use
the command key while selecting
options.
## Submit Button
<input>
type="submit"
The submit button is used to
send a form to the server.
- name
It can use a name attribute but it
does not need to have one.
- value
The value attribute is used to
control the text that appears
on a button. It is a good idea to
specify the words you want to
appear on a button because the
default value of buttons on some
browsers is ‘Submit query’ and
this might not be appropriate for
all kinds of form.
## Labelling Form Controls
When introducing form controls,
the code was kept simple by
indicating the purpose of each
one in text next to it. However,
each form control should have
its own ``<label> ``element as this
makes the form accessible to
vision-impaired users.
used in two ways. It can:
1.  Wrap around both the text
description and the form input.

2.  Be kept separate from the
form control and use the for
attribute to indicate which form
control it is a label for.
## Grouping Form Elements
``<fieldset>``
You can group related form
controls together inside the
``<fieldset>`` element. This is
particularly helpful for longer
forms.
``<legend>``
The ``<legend>`` element can
come directly after the opening
``<fieldset>`` tag and contains a
caption which helps identify the
purpose of that group of form
controls.
![](https://1.bp.blogspot.com/-ZC0uaXqKEcI/XVGmWVS7KiI/AAAAAAAAO_w/fEx_ZT_eViot8h4grotUDzYTDCI7OYhhwCLcBGAs/s1600/Screenshot%2B%2528454%2529.png)




# the list
## list-style-type
The list-style-type property
allows you to control the shape
or style of a bullet point (also
known as a marker).
It can be used on rules that
apply to the `<ol>`,`<ul>`, and `<lili`>
elements.
- Unordered Lists
For an unordered list you can use
the following values:
n- none
 - disc
 - circle
 - square
- Ordered Lists
For an ordered (numbered) list
you can use the following values:
- decimal
1 2 3
- decimal-leading-zero
01 02 03
- lower-alpha
a b c
- upper-alpha
A B C
- lower-roman
`list-style-type: lower-roman;`
## list-style-image
You can specify an image to act
as a bullet point using the
list-style-image property.
The value starts with the letters
url and is followed by a pair
of parentheses. Inside the
parentheses, the path to the
image is given inside double
quotes.
`list-style-image: url("images/star.png");}`
This property can take one of
two values:

1- outside
The marker sits to the left of the
block of text. (This is the default
behaviour if this property is not
used.)

2- inside
The marker sits inside the box of
text (which is indented).
In the example shown, the width
of the list has been limited to 150
pixels. This ensures that the text
wraps onto a new line so you can
see how the value of inside sits
the bullet inside the first line of
text.#
# table Properties
You have already met several
properties that are commonly
used with tables.
- width to set the width of the
table
- padding to set the space
between the border of each table
cell and its content
- text-transform to convert the
content of the table headers to
uppercase
letter-spacing, font-size
to add additional styling to the
content of the table headers
border-top, border-bottom
to set borders above and below
the table headers
- text-align to align the writing
to the left of some table cells and
to the right of the others
background-color to change
the background color of the
alternating table rows

## empty-cells
If you have empty cells in
your table, then you can use
the empty-cells property to
specify whether or not their
borders should be shown.
It can take one of three values:
- show
This shows the borders of any
empty cells.
- hide
This hides the borders of any
empty cells.
- inherit
If you have one table nested
inside another, the inherit
value instructs the table cells to
obey the rules of the containing
table.
``empty-cells: show;``
``empty-cells: hide``

## border-spacing, border-collapse
The border-spacing property
allows you to control the
distance between adjacent cells.
By default, browsers often leave
a small gap between each table
cell, so if you want to increase
or decrease this space then
the border-spacing property
allows you to control the gap.
1- collapse
Borders are collapsed into a
single border where possible.
(border-spacing will be
ignored and cells pushed
together, and empty-cells
properties will be ignored.)
2- separate
Borders are detached from each
other. (border-spacing and
empty-cells will be obeyed.)
## Styling Forms
It is most common to style:
●● Text inputs and text areas
●● Submit buttons
●● Labels on forms, to get the
form controls to align nicely
- font-size sets the size of the
text entered by the user.
- color sets the text color, and
- background-color sets the
background color of the input.
- border adds a border around
the edge of the input box, and
border-radius can be used
to create rounded corners (for
browsers that support this
property).
- The :focus pseudo-class is
used to change the background
color of the text input when it
is being used, and the :hover
psuedo-class applies the same
styles when the user hovers over
them.
- background-image adds a
- 
- background image to the box.
Because there is a different
image for each input, we are
using an attribute selector
looking for the value of the id
attribute on each input.
## Web Developer Toolbar
This helpful extension for Firefox and Chrome
provides tools to show you the CSS styles that
apply to an element when you hover over it,
along with the structure of the HTML.
# the events
HOW EVENTS TRIGGER
JAVASCRIPT CODE??
When the user interacts with the HTML on a web page, there are three
steps involved in getting it to trigger some JavaScript code
Together these steps are known as event handling.
1- Select t he element
node(s) you want the
script to respond to.

2- Indicate which event on
the selected node(s) will
trigger the response.

3-State the code you want
to run when the event
occurs.
### TRADITIONAL DOM EVENT HANDLERS
``element .onevent =functionName ;``
the event handler is on
the last line (after the function
has been defined and the DOM
element node(s) selected).
When a function is called, the
parentheses that fo llow its name
tell the JavaScript interpreter to
"run this code now."
We don't want the code to
run until the event fires, so the
parentheses are omitted from
the event handler on the last line.
### EVENT LISTENERS
Event listeners are a more recent approach to handling events.
They can deal with more than one function at a time
```element .addEventlistener('event', ``
``functionName [, Boolean]) ;``
USING EVENT LISTENERS
1. If you use a named function
when the event fi res on your
chosen DOM node, write that
function first. (You could also
use an anonymous function.)
2. The DOM element node(s) is
stored in a variable. Here the text
input (whose id attribute has a
value of username) is placed into
a variable called el Username.
### USING PARAMETERS WITHEVENT HANDLERS& LISTENERS
Because you cannot have parentheses after the
function names in event handlers or listeners,
passing arguments requires a workaround
event flow.
### THE EVENT OBJECT
Every time an event fires, the The event object is passed to
event object contains helpful any function that is the event
data about the event, such as: handler or listener.
• Which element the event
happened on If you need to pass arguments
• Which key was pressed for a to a named function, the event
keypress event object will first be passed to the
• What part of the viewport the anonymous wrapper function
user clicked for a c 1 i ck event (this happens automatically);
(the viewport is the part of then you must specify it as a
the browser window that parameter of the named function
shows the web page)
## USING EVENT LISTENERSWITH THE EVENT OBJECT.
1. It can be used to check the length of any text
input so long as that input is directly followed by an
empty element that can hold a feedback message
for the user. (There should not be space or carriage
returns between the two elements; otherwise, some
browsers might return a whitespace node.)
2. The code will work with IES-8 because it tests
whether the browser supports the latest features (or
whether it needs to fall back to use older techniques).
### EVENT DELEGATION
Creating event listeners for a lot of elements
can slow down a page, but event flow allows
you to listen for an event on a parent element.
If users can interact with a lot of
elements on the page, such as:
• a lot of buttons in the UI
• a long list
• every cell of a table
adding event listeners to each
element can use a lot of memory
and slow down performance.
## CHANGING DEFAULT BEHAVIOR
-preventDef au1t ()
Some events, such as clicking on
links and submitting forms, take
the user to another page.
To prevent the default behavior
of such elements (e.g., to keep
the user on the same page
rather than following a link
or being taken to a new page
after submitting a form), you
can use the event object's
preventoefault() method.
IES-8 have an equivalent
property called return Va 1 ue
which can be set to fa 1 se. A
conditional statement can check
``if the prevent Def au 1t () method``
``is supported, and use IE8's``
``approach if it isn't:``
``if (event .preventDefault)``
``event.preventDefaul t ();``
``else {``
``event .returnVa l ue = false ;``
The event object has methods that change:
the default behavior of an element and how
the element's ancestors respond to the event.
- stopPropagation()
Once you have handled an
event using one element, you
may want to stop that event
from bubbling up to its ancestor
elements (especially if there
are separate event handlers
responding to the same events
on the containing elements).
To stop the event bubbling up,
you can use the event object's
stopPropogation() method.
The equivalent in IE8 and earlier
is the cance 1 Bubble property
which can be set to true. Again,
a conditional statement can
check if the stopPropogati on()
method is supported and use
IE8's approach if not:
``if (event . stopPropogation)``
``event.stopPr opogation();``
``else {``
``event.cancel Bubble = true;``
 - USING BOTH METHODS
You will sometimes see the
following used in similar
situations that are in a function:
r eturn false;
It prevents the default behavior
of the element, and prevents
the event from bubbling up or
capturing further. It also works in
all browsers, so it is popular.
Note, however, when the
interpreter comes across the
return false statement, it stops
processing any subsequent code
within that function and moves
to the next statement after the
function was called.
Since this blocks any further
code within the function,
it is often better to use the
preventDefaul t () method of
the event object rather than
return false.
## USER INTERFACE EVENTS
User interface CUI) events occur as a result of interaction with the
browser window rather than the HTML page contained within it,
e.g., a page having loaded or the browser window being resized.
## FOCUS & BLUR EVENTS
The HTML elements you can interact with, such as links and form
elements, can gain focus. These events fire when they gain or lose focus.
### MOUSE EVENTS
The mouse events are fired when the mouse is moved and also when its
buttons are clicked.
### KEYBOARD EVENTS
The keyboard events are fired when a user interacts with the keyboard
(they fire on any kind of device with a keyboard).
### FORM EVENTS
There are two events that are commonly used with forms.
In particular you are likely to see submit used in form validation.
submit When a form is submitted, the submit
event fires on the node representing the
``<form>`` element. It is most commonly
used when checking the values a user has
entered into a form before sending it to the
server.
### MUTATION EVENTS & OBSERVERS Whenever
**Whenever elements are added to or removed** **from the DOM**, **its**
**structure changes. This change triggers a****mutation event.**
DOMNodelnserted Fires when a node is inserted into the DOM tree.
e.g. using appendChi 1 d (), rep1aceChi1 d (}, or i nsertBefore (} .

![](https://www.lessons2all.com/java%20images/21.jpg)






