# Responsive Web Design

## Responsive Overview


Responsive web design is the practice of 

building a website suitable to work on every 

device and every screen size, no matter how large or small, mobile or desktop. Responsive

 web design is focused around providing an intuitive and gratifying experience for everyone. Desktop computer and cell phone 
 
 users alike all benefit from responsive websites.
### Responsive vs. Adaptive vs. Mobile

- Responsive and adaptive web design are closely related, and often transposed as one in the same. Responsive generally means to 

react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change.

- Mobile, on the other hand, generally means to build a separate website commonly on a new domain solely for mobile users. While this 

does occasionally have its place, it normally isn’t a great idea.

# Flexible Layouts

fexible layouts, media queries, and flexible media. The first part, flexible layouts, is the practice of building the layout of a 

website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units, most commonly percentages or em units. These

 relative lengths are then used to declare common grid property values such as width, margin, or padding.

## Flexible Grid

Using the flexible grid formula we can take all of the fixed units of length and turn them into relative units. In this example we’ll use percentages but em units would work equally as well. 

# Media Queries

*Media queries*were built as an extension to media types commonly found when targeting and including styles. Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example. 

## Logical Operators in Media Queries

Logical operators in media queries help build powerful expressions. There are three different logical operators available for use within media queries, including and, not, and only.

``@media all and (min-width: 800px) and (max-width: 1024px) {...}``
``@media not screen and (color) {...}``
``@media only screen and (orientation: portrait) {...}``

## Media Features in Media Queries

Height & Width Media Features
One of the most common media features revolves around determining a height or width for a device or browser viewport. The height and width may be found by using the height and width media features. Each of these media 

features may then also be prefixed with the min or max qualifiers, building a feature such as min-width or max-width.

The height and width features are based off the height and width of the viewport rendering area, the browser window for example. Values for these 

height and width media features may be any length unit, relative or absolute.

## Orientation Media Feature

The orientation media feature determines if a device is in the landscape or portrait orientation. The landscape mode is triggered when the display is 

wider than taller, and the portrait mode is triggered when the display is taller than wider. This media feature plays a large part with mobile devices.

``@media all and (orientation: landscape) {...}``

# Viewport

**Mobile devices** generally do a pretty decent job of displaying websites these days. Sometimes they could use a little assistance though, particularly around identifying the viewport size, scale, and resolution of a website. To remedy this, Apple invented the viewport meta tag.

### Viewport Height & Width

Using the viewport meta tag with either the **height or width** values will define the **height or width** of the viewport respectively. Each value accepts either a positive integer or keyword. For the height property the 

keyword device-height value is accepted, and for the width property the keyword device-width is accepted. Using these keywords will inherit the device’s default height and width value.


![](https://learn.shayhowe.com/assets/images/courses/advanced-html-css/responsive-web-design/with-viewport.png)

``<meta name="viewport" content="width=device-width">``

## Viewport Resolution

Letting the browser decide how to scale a website based off any viewport scale values usually does the trick. When more control is needed, specifically over the resolution of a device, the target-densitydpi value may be used. The target-densitydpi viewport accepts a handful of values including device-dpi, high-dpi, medium-dpi, low-dpi, or an actual DPI number.


``<meta name="viewport" content="target-densitydpi=device-dpi">``

## Combining Viewport Values


The viewport meta tag will accept individual values as well as multiple values, allowing multiple viewport properties to be set at once. 

Setting multiple values requires comma separating them within the content attribute value. One of the recommended viewport values is outlined below, using both the width and initial-scale properties.


``<meta name="viewport" content="width=device-width, initial-scale=1">``

![](https://learn.shayhowe.com/assets/images/courses/advanced-html-css/responsive-web-design/with-viewport.png)

#  Floats

**Float** is a CSS positioning property. To understand its purpose and origin, we can look to print design. In a print layout, images may be set into the page such that text wraps around them as needed. This is commonly and appropriately called “text wrap”. 

![](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/web-text-wrap.png?resize=540%2C270&ssl=1)

``#sidebar {float: right;}``

#  Clearing the Float

*Float’s sister property* is **clear**. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. Again an illustration

 probably does more good than words do.

 ![](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/unclearedfooter.png?resize=540%2C195)

 ## Problems with Floats

 Floats often get beat on for being fragile. The majority of this fragility comes from IE 6 and the slew of float-related bugs it has. As more and more designers are dropping support for IE 6, you may not care, but for the folks that do care here is a quick rundown.

 - **Pushdown**is a symptom of an element inside a floated item being wider than the float itself (typically an image). Most browsers will render the image outside the float, but not have the part sticking out affect other 

-  **layout**. IE will expand the float to contain the image, often drastically affecting layout. A common example is an image sticking out of the main content push the sidebar down below.

- **Double** Margin Bug – Another thing to remember when dealing with IE 6 is that if you apply a margin in the same direction as the float, it will 
  
  double the margin. Quick fix: set display: inline on the float, and don’t worry it will remain a block-level element.


- **The 3px Jog** is when text that is up next to a floated element is mysteriously kicked away by 3px like a weird forcefield around the float. Quick fix: set a width or height on the affected text.


In IE 7, the Bottom Margin Bug is when if a floated parent has floated children inside it, bottom margin on those children is ignored by the parent. Quick fix: using bottom padding on the parent instead.