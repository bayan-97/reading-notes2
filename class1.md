# Read: 01 - Introductory HTML and JavaScript

 ## creating web pages
  **we need to learn** :


  1- **html** :You will see that you start by writing down
the words you want to appear on your page. You then add tags
or elements to the words so that the browser knows what is
 a heading, where a paragraph begins and ends.


 2- **css** :uses rules to enable you to
control the styling and layout of web pages. We then go on to
look at the wide variety of CSS properties you can use in your CSS rules

### the different ways in which people access the web and clarify some terminolog



1-People access websites using
software called a web browser.
Popular examples include
Firefox, Internet Explorer, Safari,
Chrome, and Opera.


2- Web servers are special
computers that are constantly
connected to the Internet, and
are optimized to send web pages
out to people who request them
3-Screen readers are programs
that read out the contents of a
computer screen to a user. They
are commonly used by people
with visual impairments.


3-People are accessing websites
on an increasing range of devices
including desktop computers,
laptops, tablets, and mobile
phones.
When you visit a website, the web server
hosting that site could be anywhere in the
world. In order for you to find the location of
the web server, your browser will first connect
to a Domain Name System (DNS) server.

## html  structure

**We use structure when writing web pages.**
**HTML page structure: The Basic structure of HTML page is given below. It contain some elements like head, title, body, … etc. These elements are used to build the blocks of web pages**

![pic](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-1-6.png)

**Elements and Tag: HTML uses predefined tags and elements which tells the browser about content display property. If a tag is not closed then browser applies that effect till end of page.**

![pic](https://media.geeksforgeeks.org/wp-content/uploads/html.jpg)



The Evolution of HT ML
 VERSIO  |YEAR
 --------|--------
HTML 1.0|1991
HTML 2.0|1995
HTML 3.2|1997
HTML 4.01|1999
XHTMl| 2000
HTML 5|2014   


### many code they  are importnat know in html :
- **commment**
 If you want to add a comment
to your code that will not be
visible in the user's browser, you
can add the text between these
characters:
`<!-- comment goes here -->`


- The **id Attribute** : This attribute is used to provide a unique identification to an element. Situations may arise when we will need to access a particular element which may have a similar name as the others. In that case, we provide different ids to various elements so that they can be uniquely accessed. The properties extending the use of id is generally used in CSS, which we will be learning later.
 ``<p id = "GfG">Hello geeks<br>``
    ``<p id = "ui">This is unique to this paragraph<br> ``
    ``<p id = "head">This is also unique to this paragraph>``


- **class**:The class attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.
  ``<div class="city">``



- **Block-level Elements**
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).



``<div>Hello World</div>``

  -**The `<div> `element** allows you to
group a set of elements together
in one block-level box.
For example, you might create
a `<div>` element to contain all
of the elements for the header
of your site (the logo and the
navigation), or you might create
a `<div>` element to contain
comments from visitors.



**examp:**
``<address><article><aside><blockquote><canvas><dd><div><dl><dt><fieldset><figcaption><figure><footer><form><h1>-<h6><header><hr><li><main><nav><noscript><ol><p><pre><section><table><tfoot><ul>``



- I**nline Elements**
An inline element does not start on a new line and it only takes up as much width as necessary.

**``<span>Hello World</span>``**
   1. Contain a section of text
where there is no other suitable
element to differentiate it from
its surrounding text
   2. Contain a number of inline
elements



**examp:** ``<a><abbr><acronym><b><bdo><big><br><button><cite><code><dfn><em><i><img><input><kbd><label><map><object><output><q><samp><script><select><small><span><strong><sub><sup><textarea><time><tt><var>``

-**meta:**
The ```<meta>`` element is typically used to specify the character set, page description, keywords, author of the document, and viewport settings.4

The metadata will not be displayed on the page, but are used by browsers (how to display content or reload page), by search engines (keywords), and other web services
.
``<meta charset="UTF-8">``


- **iframes** :The HTML ``<iframe>`` tag specifies an inline frame.
An inline frame is used to embed another document within the current HTML document.
``<iframe src="url" title="description">``

![pic](https://cdn.educba.com/academy/wp-content/uploads/2019/11/Iframes-in-HTML-eg1.png)

 # HTML5

 is introducing a new set of
elements that help define the structure of a page.

![pic](https://www.developer.com/imagesvr_ce/3977/Figure01.png)

**HTML5** includes a set of markup elements that overcome this difficulty. These new elements have meaningful names so that just by looking at these elements you get a clear idea about their content. These semantic elements of HTML5 are listed below (this is not an exhaustive list):

`<header>`
`<footer>`
`<section>`
`<article>`
`<aside>`
`<nav>`

- The ``<header>`` and ``<footer>``
elements can be used for:
●● The main header or footer
that appears at the top or
bottom of every page on the
site.
●● A header or footer for an
individual ``<article>`` or
``<section>`` within the page.



- The ``<nav>`` element is used to
contain the major navigational
blocks on the site such as the
primary site navigation.
Going back to our blog example,
if you wanted to finish an article
with links to related blog posts,
these would not be counted as
major navigational blocks and
therefore should not sit inside a
``<nav>`` element.


- The ``<article>`` element acts as
a container for any section of a
page that could stand alone and
potentially be syndicated.
This could be an individual
article or blog entry, a comment
or forum post, or any other
independent piece of content.
The ``<aside>`` element has two
purposes, depending on whether
it is inside an ``<article>``
element or not.
When the ``<aside>`` element
is used inside an ``<article>``
element, it should contain
information that is related to the
article but not essential to its
overall meaning. For example, a
pullquote or glossary might be
considered as an aside to the
article it relates to.

- The ``<section>`` element groups
related content together, and
typically each section would
have its own heading.
For example, on a homepage
there may be several ``<section>``
elements to contain different
sections of the page, such as
latest news, top products, and
newsletter signup.


# the website 
**Every website should be designed for the**
**target audience—not just for ourself or the**
**site owner. It is therefore very important to understand** 

- *who your target audience is?
*It can be helpful to ask some*
*questions about the people you*
*would expect to be interested in*
*the subject of your site.*

- *Why People Visit YOUR Website?
- 
1: *The first attempts to discover*
*the underlying motivations for*
*why visitors come to the site.*


2: *The second examines the
specific goals of the visitors.
These are the triggers making
them come to the site now.*



 ## *now you need to work out


what information they need in order to achieve
their goals quickly and effectively by desgin?*
1- **The aim is to create a diagram
of the pages that will be used
to structure the site. This is
known as a site map and it will
show how those pages can be
grouped.**

![sitmap](https://www.joomlashine.com/images/easyblog_articles/894/Think-ahead-of-your-site-hierachy-structure-before-making-any-sitemap.png)

## WireFrames

*A lot of designers will take the
elements that need to appear on
each page and start by creating
wireframes. This involves
sketching or shading areas
where each element of the page
will go (such as the logo, primary
navigation, headings and main
bodies of text, user logins etc).*

# java script

# script
*A script is a series of instructions that the computer
can follow in order to achieve a goal.
before use it we have to understand the  abc of programing*

**A SCRIPT IS A SERI ES OF INSTRUCTIONS HANDBOOKS Large companies often provide handbooks for new employees that contain procedures to fo llow in certain situations**.*For example -hotel handbooks may contain steps to follow in different scenarios such as when a guest checks in, when a room needs to be tidied, when a f ire
alarm goes off, and so forth. In any of these scenarios, the employees need to follow only the steps for that one type of event. (You would not want someone going through every single step in the entire handbook while you weren waiting to check in.) Similarly,
in a complex script, the browser
might use only a subset of the
code available at any given time
design my script .*

## Often scripts will need to perform different tasks in different situations.You can use flowcharts to work out how the tasks fit together.The flowcharts show the paths between each step.

**Arrows show how the script moves from one task
to the next. The different shapes represent diff€rent
types of tasks. In some places there are decisions
which cause the code to follow different paths. you
will meet code that helps you deal with each of these
types of situations.
Some experienced programmers use more complex
diagram styles that are specifically designed to
represent code - however, they have a steeper
learning curve. These informal flowcharts will help
you understand how scripts work while you are in
the process of learning the language.**

![pic](https://cdn.rawgit.com/bubkoo/hexo-filter-flowchart/master/snapshot.svg)

## COMPUTERS CREATE MODELS OF THE WORLD USING DATA

by three way:
1- **OBJECTS** (THINGS)
In computer programming, each physica l thing in
the world can be represented as an object. There are
two different types of objects here: a hotel and a car.
Programmers might say that there is one instance of
the hotel object, and two instances of the car object.
Each object can have its own:
• Properties
• Events
• Methods
Together they cr




2-**PROPERTIES** (CHARACTERISTICS)
Both of the cars share common characteristics.
In fact, all cars have a make, a color, and engine
size. You could even determine their current
speed. Programmers call these characteristics the
properties of an object.
Each property has a name and a value, and each of
these name/value pairs tells you something about
each individual instance of the object.

The most obvious property of this hotel is its name.
The value for that property is Quay. You can te ll the
number of rooms the hotel has by looking at the
value next to the rooms property.

The idea of name/value pairs is used in both HTML and CSS. In HTML, an attribute is like a property; different
attributes have different names, and each attribute can have a value. Similarly, in CSS you can change the color
of a heading by creating a rule that gives the col or property a specific value, or you can change the typeface it is
written in by giving the font-family property a specific value. Name/value pairs are used a lot in programming.


3- **WHAT IS AN EVENT?**
There are common ways in which people interact
with each type of object. For example, in a car a
driver will typically use at least two pedals. The car
has been designed to respond differently when the
driver interacts with each of the different pedals:
• The accelerator makes the car go faster
• The brake slows it down

**WHAT DOES AN EVENT DO?**
Programmers choose which events they respond to.
When a specific event happens, that event can be
used to trigger a specific section of the code.
Scripts often use different events to trigger different
types of functionality.
So a script will state which events the programmer
wants to respond to, and what part of the script
should be run when each of those events occur.


4-  **WHAT DOES AN EVENT DO?**
Programmers choose which events they respond to.
When a specific event happens, that event can be
used to trigger a specific section of the code.
Scripts often use different events to trigger different
types of functionality.
So a script will state which events the programmer
wants to respond to, and what part of the script
should be run when each of those events occur


**WHAT DOES A METHOD DO?**
The code for a method can contain lots of
instructions that together represent one task.
When you use a method, you do not always need to
know how it achieves its task; you just need to know
how to ask the question and how to interpret any
answers it gives you.

![pic](https://i.ytimg.com/vi/PzmwtZ-yv6o/maxresdefault.jpg)


# HOW HTML, CSS, & JAVASCRIPT FIT TOGETHER

  *HTML will be referred to as the physical body, CSS will be the body’s accessories and JavaScript is *the body’s ability to talk or move. All of these ‘bodily aspects’ need to work together to form *a *functional, visually appealing, interactive website*
- ``<html>``
CONTENT LAYER
 . html files
 - ``{css}``
PRESENTATION LAYER
.css files .
- ``j avascri pt()``
  BEHAVIOR LAYER
   .js files

   1- **HTML ONLY**
Starting with the HTML layer
allows you to focus on the most
important thing about your site:
its content.
Being plain HTML, this layer
should work on all kinds of
devices, be accessible to all
users, and load quite quickly on
slow connections.

2- **HTML+CSS**
Adding the CSS rules in a
separate file keeps rules
regarding how the page looks
away from the content itself.
You can use the same style sheet
with all of your site, making your
sites faster to load and easier
to maintain. Or you can use
different style sheets with the
same content to create different
views of the same data.


 3- **HTML+CSS+JAVASCRIPT**
The JavaScript is added last
and enhances the usability of
the page or the experience of
interacting with the si te.
Keeping it separate means
that the page still works if the
user cannot load or run the
JavaScript. You can also reuse
the code on severa l pages
(making the site faster to load
and easier to maintain).

### A BASIC JAVASCRIPT

*A JavaScript fi le is just a*
*text file (like HTML and CSS*
*files are) but it has a . j s file*
*extension, so save this file with*
*the name add-content . j s.*

### LINKING TO A JAVASCRIPT FILE FROM AN HTML PAGE

 **A-When you want to use JavaScript with a web page, you use the HTML**
**``<script>`` element to tell the browser it is coming across a script.**
**Its s re attribute tells people where the JavaScript file is stored.**

``<!DOCTYPE html>``
``<html>``
``<head>``
``<title>Constructive &amp; Co.</ title>``
``<link rel ="stylesheet" href="css/ cOl.css" />``
``</ head>``
``<body>``
``<hl>Constructive &amp; Co. </ hl>``
``<script src="js/ add-content.js"></ script>``
``<p>For all orders and i nquiries please cal l``
```<em>SSS-3344</ em></ p>```
``</ body>``
``</html>``


B- You may see JavaScript in the HTML between
opening ``<script> ``and closing`` </script>`` tags
(but it is better to put scripts in their own files).
``<!DOCTYPE html>``
``<html >``
``<head>``
``<title>Constructive &amp; Co.</title>``
``<li nk rel ="stylesheet" href="css/ cOl .css" />``
``</ head>``
``<body>``
``<hl>Constructive &amp; Co.</hl>``
``<script>document.write(' <h3>Welcome !</h3>');``
``</script>``
``<p>For all orders and inquiries please call``
``<em>555-3344</ em></ p>``
``</ body>``
``</ html >``
