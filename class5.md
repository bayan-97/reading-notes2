# the image in the html
A picture can say a thousand words, and great
images help make the difference between an
average-looking site and a really engaging one.

Images should...
Be relevant
1- Convey information
2- Convey the right mood
3- Be instantly recognisable
4- Fit the color palette
## Storing Images onYourSite

If you are building a site from scratch, it is good
practice to create a folder for all of the images
the site uses.

*## Adding Images
``<img>`` images.html HTML
To add an image into the page
you need to use an ``<img>``
element. This is an empty
element (which means there is
no closing tag). It must carry the
following two attributes:
**src**
This tells the browser where
it can find the image file. This
will usually be a relative URL
pointing to an image on your
own site. (Here you can see thatthe images are in a child folder
**alt**
This provides a text description
of the image which describes the
image if you cannot see it.
**title**
You can also use the title
attribute with the ``<img>`` element to provide additional information
about the image. Most browsers
will display the content of this
attribute in a tootip when the
user hovers over the image.

``<img src="images/quokka.`jpg" alt="A family of``
``quokka" title="The quokka ```is an Australian``
``marsupial that is similar ````in size to the``
``domestic cat." />``
## Height & Width of Images
- height
This specifies the height of the
image in pixels.
- width
This specifies the width of the
image in pixels.

``<img src="images/quokka.````jpg" alt="A family of``
``quokka" width="600" ````height="450" />``
## Where to Place Imagesin  Your Code
1- before a paragraph
The paragraph starts on a new
line after the image.

2- inside the start of a
paragraph
The first row of text aligns with
the bottom of the image.

3- in the middle of a
paragraph
The image is placed between the
words of the paragraph that it
appears in.

## Three Rules forCreating Images
1-
Save images in
the right format
Websites mainly use images in
jpeg, gif, or png format. If you
choose the wrong image
format then your image might
not look as sharp as it should
and can make the web page
slower to load.

2-
Save images at
the right size
You should save the image at
the same width and height it will
appear on the website. If
the image is smaller than the
width or height that you have
specified, the image can be
distorted and stretched. If the
image is larger than the width
and height if you have specified,
the image will take longer to
display on the page.

3-
Use the correct
resolution
Computer screens are made up
of dots known as pixels. Images
used on the web are also made
up of tiny dots. Resolution refers
to the number of dots per inch,
and most computer screens only
show web pages at 72 pixels
per inch. So saving images at
a higher resolution results in
images that are larger than
necessary and take longer to
download.

There are several tools you can use to edit and
save images to ensure that they are the right
size, format, and resolution.
The most popular tool amongst
web professionals is **Adobe**
**Photoshop.**
## Image Di mensions
The images you use on your website should be
saved at the same width and height that you
want them to appear on the page.
REDU CING IMAGE SIZE
You can reduce the size of
images to create a smaller
version of the image.
Example: If your image is 600
pixels wide and 300 pixels tall,
you can reduce the size of the
image by 50%.
Result: This will create an image
that is quicker to download.
INCREAS ING IMAGE SIZE
You can't increase the size of
photos significantly without
affecting the image quality.
Example: If your image is only
100 pixels wide by 50 pixels tall,

increasing the size by 300%
would result in poor quality.
Result: The image will look
blurry or blocky.
CHANG ING SHAPE
Only some images can be
cropped without losing valuable
information (see next page).
Example: If your image is 300
pixels square, you can remove
parts of it, but in doing so you
might lose valuable information.

Result: Only some images can
be cropped and still make sense.
## Cropping Images
When cropping images it is important not to
lose valuable information. It is best to source
images that are the correct shape if possible
![](https://miro.medium.com/max/649/1*V7KXescZAp4pgN5u89pSHA.jpeg)
## Image Resolution
Images created for the web should be saved at
a resolution of 72 ppi. The higher the resolution
of the image, the larger the size of the file.
![](https://media.springernature.com/m685/springer-static/image/art%3A10.1038%2Fs41598-019-38914-y/MediaObjects/41598_2019_38914_Fig1_HTML.png)
## Vector Images
Vector images differ from bitmap images and
are resolution-independent. Vector images are
commonly created in programs such as Adobe
Illustrator.
## Animated GIFs
Animated GIFs show several frames of an
image in sequence and therefore can be used to
create simple animations.
![](https://media.emailonacid.com/wp-content/uploads/2019/03/2019-GifsInEmail.gif)


## Transparency
Creating an image that is partially transparent
(or "see-through") for the web involves
selecting one of two formats:
- Transparent GIF'
 If the transparent part of the
image has straight edges and
it is 100% transparent (that is,
not semi-opaque), you can save
the image as a GIF (with the
transparency option selected).
- PNG
If the transparent part of the
image has diagonal or rounded
edges or if you want a semiopaque
transparency or a dropshadow,
then you will need to
save it as a PNG.
## Examining Images on the Web
1-Checking the Si ze of Images
If you are updating a website, you might need to check the size of an
existing image before creating a new one to replace it. This can be
achieved by right-clicking on the image and making a selection from
the pop-up menu that appears. (Mac users will need to hold down the
control key and click rather than right-click.)
2- Downloading Images
If you want to download images from a website, you can do so by
accessing the same pop-up menu. (Please remember however that all
images online are subject to copyright and require explicit permission to
reuse.)
## HTML    5FigureandFigureCaption
``<figure>``
Images often come with
captions. HTML5 has introduced
a new ``<figure>`` element to
contain images and their caption
so that the two are associated.
You can have more than one
image inside the ``<figure>``
element as long as they all share
the same caption.
``<figcaption>``

The ``<figcaption>`` element has
been added to HTML5 in order
to allow web page authors to add
a caption to an image.
Before these elements were
created there was no way to
associate an ``<img>`` element with
its caption.
``<figure>``
``<img src="images/otters.````jpg" alt="Photograph of``
``two sea otters floating in ````water">``
``<br />``
``<figcaption>Sea otters hold ````hands when they``
``sleep so they don't drift ````away from each``
``other.</figcaption>``
``</figure>``
![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQ4dOTSou7dwrcVRq4Q2tkW33EgdjECzaxIXA&usqp=CAU)
# the color in css

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

## the text
**Serif**
Serif fonts have extra details on
the ends of the main strokes of
the letters. These details are
known as serifs.
In print, serif fonts were
traditionally used for long
passages of text because they
were considered easier to read.
**Sans-Serif**
Sans-serif fonts have straight
ends to letters, and therefore
have a much cleaner design.
Screens have a lower resolution
than print. So, if the text is small,
sans-serif fonts can be clearer
to read.
**Monospace**
Every letter in a monospace (or
fixed-width) font is the same
width. (Non-monospace fonts
have different widths.)
Monospace fonts are commonly
used for code because they align
nicely, making the text easier to
follow.
im im im
TEXT 268
Light
Medium
Bold
Black
Normal
Italic
Oblique
Condensed
Regular
Extended
The font weight not only adds
emphasis but can also affect
the amount of white space and
contrast on a page.
Italic fonts have a cursive aspect
to some of the lettering. Oblique
font styles take the normal style
and put it on an angle.
In condensed (or narrow)
versions of the font, letters are
thinner and closer together.
In expanded versions they are
thicker and further apart.
## Choosing a Typefacefor your Website
When choosing
a typeface, it
is important to
understand that a
browser will usually
only display it if it's
installed on that
user's computer.
**Serif**
Serif fonts have extra details on
the end of the main strokes of
the letters.
Examples:
Georgia
**Times**
Times New Roman
Sans-Serif
Sans-serif fonts have straight
ends to letters and therefore
have a much cleaner design.
Examples:
Arial
Verdana
Helvetica

## Techniques That Offer a Wider Choice of typefaces 
font-family 
The user's computer needs the
typeface installed. CSS is used to
specify the typeface.
font-face Service-based
CSS specifies where a font can
be downloaded from if it is not
installed on the computer.
Font-Face
Commercial services give users
access to a wider range of fonts
using @font-face.

## font-family
The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.
The value of this property is the
name of the typeface you want
to use.
``h1, h2 {``
``font-family: Arial, Verdana, sans-serif;}``
## font-size
1- **pixels**
Pixels are commonly used
because they allow web
designers very precise control
over how much space their text
takes up. The number of pixels is
followed by the letters px.
2- **percentages**
The default size of text in
browsers is 16px. So a size of
75% would be the equivalent of
12px, and 200% would be 32px.

``h1 {``
``font-size: 200%;}``
``h2 {``
``font-size: 1.3em;}``
![](https://media.geeksforgeeks.org/wp-content/uploads/fontsize1.png)

##  Type Scales
You may have noticed that programs such as
Word, Photoshop and InDesign offer the same
sizes of text.

This is because they are set
according to a scale or ratio that
was developed by European
typographers in the sixteenth
century.

- Pixels 
- Percentages
-  Ems
  
  ## 
  1- *font-family*
This specifies the name of the
font. This name can then be used
as a value of the font-family
property in the rest of the style
sheet (as shown in the rule for
the ``<h1>`` and ``<h2>`` elements).

2-*src*
This specifies the path to the
font. In order for this technique
to work in all browsers, you will
probably need to specify paths
to a few different versions of the
font, as shown on the next page.

3- *format*
This specifies the format that the
font is supplied in. (It's discussed
in detail on the next page.)
## Font Formats
Different browsers support
different formats for fonts
(in the same way that they
support different audio and
video formats), so you will need
to supply the font in several
variations to reach all browsers.
If you do not have all of these
formats for your font, you can
upload the font to a website
called FontSquirrel where they
will convert it for you:
![](https://d3ui957tjb5bqd.cloudfront.net/uploads/2015/11/cross-browser-support.png)

## font-weight
The font-weight property
allows you to create bold text.
There are two values that this
property commonly takes:
normal
This causes text to appear at a
normal weight.
bold
This causes text to appear bold.
## 
If you want to create italic text,
you can use the font-style
property. There are three values
this property can take:
normal
This causes text to appear in a
normal style (as opposed to italic
or oblique).
italic
This causes text to appear italic.
oblique
This causes text to appear
oblique.
In this example, you can see that
the credits have been italicized.
Italic fonts were traditionally
stylized versions of the font
based on calligraphy, whereas an
oblique version would take the
normal version and put it on an
angle.

## text-decoration
The text-decoration property
allows you to specify the
following values:
- none
This removes any decoration
already applied to the text.
underline
This adds a line underneath the
text.

- overline
This adds a line over the top of
the text.
line-through
This adds a line through words.

- blink
This animates the text to make it
flash on and off (however this is
generally frowned upon, as it is
considered rather annoying).
``.credits {``
``text-decoration: underline;}``
``a {``
``text-decoration: none;}``

## line-height
In CSS, the line-height
property sets the height of
an entire line of text, so the
difference between the fontsize
and the line-height is
equivalent to the leading (as
shown in the diagram above).
Increasing the line-height
makes the vertical gap between
lines of text larger.
Leading
line-height
## text-align
The text-align property allows
you to control the alignment of
text. The property can take one
of four values:
left
This indicates that the text
should be left-aligned.
right
This indicates that the text
should be right-aligned.
center
This allows you to center text.
justify
This indicates that every line in
a paragraph, except the last line,
should be set to take up the full
width of the containing box.
``h1 {``
``text-align: left;}``
``p {``
``text-align: justify;}``
``.credits {``
``text-align: right;}``

## vertical-align
The vertical-align property is
a common source of confusion.
It is not intended to allow you to
vertically align text in the middle
of block level elements such as
``<p>`` and ``<div>``, although it does
have this effect when used with
table cells (the ``<td>`` and ``<th>``
elements).
## text-indent
The text-indent property
allows you to indent the first
line of text within an element.
The amount you want the line
indented by can be specified in
a number of ways but is usually
given in pixels or ems.
``.credits {``
``text-indent: 20px;}``
## text-shadow
The text-shadow property has
become commonly used despite
lacking support in all browsers.
It is used to create a drop
shadow, which is a dark version
of the word just behind it and
slightly offset. It can also be used
to create an embossed effect by
adding a shadow that is slightly
lighter than the text.
![](https://freefrontend.com/assets/img/css-text-shadow-effects/Netflix-Style-Text-Animation-with-CSS.png)

## Attribute Selectors


You met the most popular CSS selectors on page 238. There are also
a set of attribute selectors that allow you to create rules that apply to
elements that have an attribute with a specific value.

![](https://image.slidesharecdn.com/mark-csssyntaxselector-140213211343-phpapp01/95/mark-css-syntax-selector-4-638.jpg?cb=1392326713)


