# Read: 01 - Introductory HTML and JavaScript

 ## creating web pages
  we need to learn :
  1- html :You will see that you start by writing down
the words you want to appear on your page. You then add tags
or elements to the words so that the browser knows what is
 a heading, where a paragraph begins and ends.
 2- css :uses rules to enable you to
control the styling and layout of web pages. We then go on to
look at the wide variety of CSS properties you can use in your CSS rules

the different ways in which people access the web and clarify some terminolog
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
## html stru

We use structure when writing web pages.
HTML page structure: The Basic structure of HTML page is given below. It contain some elements like head, title, body, … etc. These elements are used to build the blocks of web pages.

![pic](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-1-6.png)

Elements and Tag: HTML uses predefined tags and elements which tells the browser about content display property. If a tag is not closed then browser applies that effect till end of page.

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
many code they  are importnat know in html :
- commment
 If you want to add a comment
to your code that will not be
visible in the user's browser, you
can add the text between these
characters:
`<!-- comment goes here -->`
- The id Attribute : This attribute is used to provide a unique identification to an element. Situations may arise when we will need to access a particular element which may have a similar name as the others. In that case, we provide different ids to various elements so that they can be uniquely accessed. The properties extending the use of id is generally used in CSS, which we will be learning later.
 ``<p id = "GfG">Hello geeks<br>``
    ``<p id = "ui">This is unique to this paragraph<br> ``
    ``<p id = "head">This is also unique to this paragraph>``
- class


- Block-level Elements
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).



``<div>Hello World</div>``
  -The `<div> `element allows you to
group a set of elements together
in one block-level box.
For example, you might create
a `<div>` element to contain all
of the elements for the header
of your site (the logo and the
navigation), or you might create
a `<div>` element to contain
comments from visitors.



examp: ``<address><article><aside><blockquote><canvas><dd><div><dl><dt><fieldset><figcaption><figure><footer><form><h1>-<h6><header><hr><li><main><nav><noscript><ol><p><pre><section><table><tfoot><ul>``



- Inline Elements
An inline element does not start on a new line and it only takes up as much width as necessary.

``<span>Hello World</span>``
   1. Contain a section of text
where there is no other suitable
element to differentiate it from
its surrounding text
   2. Contain a number of inline
elements



examp: ``<a><abbr><acronym><b><bdo><big><br><button><cite><code><dfn><em><i><img><input><kbd><label><map><object><output><q><samp><script><select><small><span><strong><sub><sup><textarea><time><tt><var>``




