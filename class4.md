# the link
Links are created using the <a> element. Users can click on anything
between the opening <a> tag and the closing </a> tag. You specify
which page you want to link to using the href attribute.
 ![](https://www.computerhope.com/jargon/h/html-tag.gif)
``<a href="http://www.empireonline.com">``
``Empire</a>``

- When you are linking to other
pages within the same site,
you do not need to specify the
domain name in the URL. You
can use a shorthand known as a
relative UR.
``<a href="index.html">Home</a>``
## Directory Structure
**On larger websites it's a good idea to organize your code by placing ****the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as directories.
 ![](https://openlab.citytech.cuny.edu/clarkeadv2450/files/2012/08/xid-3696808_1.jpeg)

The root folder contains:
-  A file called index.html which
is the homepage for the
entire site
-  Individual folders for the
movies, music and theatre
sections of the site
Each sub-directory contains:
-  A file called index.html which
is the homepage for that
section
-  A reviews page called reviews
.html
- A listings page called listings
.html (except for the DVD
section)
The movies section contains:
-  A folder called cinema
-  A folder called DVD.

### Relative URLs
Relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.
 ![](https://slideplayer.com/slide/11908296/67/images/10/Using+Relative+URLs+Relative+Link+Type+Example+Same+folder.jpg)

 ### Email Links

 mailto: email-links.html HTML
To create a link that starts up
the user's email program and
addresses an email to a specified
email address, you use the <a>
element. However, this time the
value of the href attribute starts
with mailto: and is followed by
the email address you want the
email to be sent to.
``<a href="mailto:jon@example.org">Email Jon</a>``

- Opening Links in a New Window
target
If you want a link to open in a
new window, you can use the
target attribute on the opening
``<a>`` tag. The value of this
attribute should be _blank.

### Linking to a Specific Part of the Sa me Page
At the top of a long page
you might want to add a list
of contents that links to the
corresponding sections lower
down. Or you might want to add
a link from part way down the
page back to the top of it to save
users from having to scroll back
to the top.
``<a href="#top">Top</a>``
4
# css layout
- Controll ing the Position of El ements
  CSS has the following positioning schemes that allow you to control
the layout of a page: normal flow, relative positioning, and absolute
positioning
Normal flow
Every block-level element
appears on a new line, causing
each item to appear lower down
the page than the previous one.
Even if you specify the width
of the boxes and there is space
for two elements to sit side-byside,
they will not appear next
to each other. This is the default
behavior (unless you tell the
browser to do something else).

Relative Positioning
This moves an element from the
position it would be in normal
flow, shifting it to the top, right,
bottom, or left of where it
would have been placed. This
does not affect the position of
surrounding elements; they stay
in the position they would be in
in normal flow.

Ab solute positioning
This positions the element
in relation to its containing
element. It is taken out of
normal flow, meaning that it
does not affect the position
of any surrounding elements
(as they simply ignore the
space it would have taken up).
Absolutely positioned elements
move as users scroll up and
down the page.
## Normal Fl ow
In normal flow, each block-level
element sits on top of the next
one. Since this is the default
way in which browsers treat
HTML elements, you do not
need a CSS property to indicate
that elements should appear
in normal flow, but the syntax
would be:
``position: static;``
## Relative Positioning
Relative positioning moves an
element in relation to where it
would have been in normal flow.
For example, you can move it 10
pixels lower than it would have
been in normal flow or 20% to
the right.``position: relative;``
## Absolute Positioning
When the position property
is given a value of absolute,
the box is taken out of normal
flow and no longer affects the
position of other elements on
the page. (They act like it is not
there.)
The box offset properties (top
or bottom and left or right)
specify where the element
should appear in relation to its
containing element.``position: absolute;``
## Fixed Positioning
Fixed positioning is a type
of absolute positioning that
requires the position property
to have a value of fixed.
It positions the element in
relation to the browser window.
Therefore, when a user scrolls
down the page, it stays in the
exact same place. It is a good
idea to try this example in your
browser to see the effect.``position: fixed;``
## Floating Elements
The float property allows you
to take an element in normal
flow and place it as far to the
left or right of the containing
element as possible.
Anything else that sits inside
the containing element will
flow around the element that is
floated.
## Clearing Floats
The clear property allows you
to say that no element (within
the same containing element)
should touch the left or righthand
sides of a box. It can take
the following values:
1- left
The left-hand side of the box
should not touch any other
elements appearing in the same
containing element.
right
2- The right-hand side of the
box will not touch elements
appearing in the same containing
element.
both
Neither the left nor right-hand
sides of the box will touch
elements appearing in the same
containing element.
3- none
Elements can touch either side.
## Creating Multi-Column Layouts with Fl oats
Many web pages use multiple
columns in their design. This
is achieved by using a ``<div>``
element to represent each
column. The following three CSS
properties are used to position
the columns next to each other:
width
This sets the width of the
columns.
float
This positions the columns next
to each other.
margin
This creates a gap between the
columns.
## Screen Sizes
Different visitors to your site will have different sized screens that show
different amounts of information, so your design needs to be able to
work on a range of different sized screens.
## Sc reen Resolution
Most computers will allow
owners to adjust the resolution
of the display or the number
of pixels that are shown on the
screen. For example, here you
can see the options to change
the screen size from 720 x 480
pixels up to 1280 x 800 pixels.
It is interesting to note that
the higher the resolution, the
smaller the text appears. Many
mobile devices have screens
that are higher resolution than
their desktop counterparts.
13" MacBook
Size: 13.3 inches
Resolution: 1280 x 800 pixels
27" iMac
Size: 27 inches
Resolution: 2560

## Page Sizes
Because screen sizes and display resolutions vary so much, web
designers often try to create pages of around 960-1000 pixels wide
(since most users will be able to see designs this wide on their screens).
## Fixed Width Layouts
Fixed width layout
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels.
## Liquid Layouts
Liquid layout designs
stretch and contract
as the user increases
or decreases the
size of their browser
window. They tend to
use percentages.
## Layout Grids
Composition in any visual art (such as design, painting, or photography)
is the placement or arrangement of visual elements — how they are
organized on a page. Many designers use a grid structure to help them
position items on a page, and the same is true for web designer.

 ![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcScWOA8O_Xy7ekGVVmMbCBzFHtKBMt0cJrMwQ&usqp=CAU)
 
