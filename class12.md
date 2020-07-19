# the chart.js

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to 

press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

 charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

 1-  Copy the Chart.min.js out of the unzipped 
 folder and into the directory you’ll be working in.

 ``<html lang="en">``
    ``<head>``
       `` <meta charset="utf-8" />``
        ``<title>Chart.js demo</title>``
        ``<script src='Chart.min.js'></script>``
    ``</head>``
   `` <body>``
   `` </body>``
``</html>``

## Drawing a line chart

- To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

- Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element

``<canvasid="buyers"width="600"height="400"><canvas>``
`    <script>`
   ``var buyers = document.getElementById('buyers').getContext('2d');``
    ``new Chart(buyers).Line(buyerData);``
``</script>``


## Drawing a pie chart

``<canvas id="countries" width="600" height="400"></canvas>``

``var countries= document.getElementById("countries").getContext("2d");``
``new Chart(countries).Pie(pieData, pieOptions);``

``var pieData = [``
``{``
``	value: 20,``
``	color:"#878BB6"``
``},``
``{``
 `` value : 40,``
``color : "#4ACAB4"``
``},``
``{``
	``value : 10,``
``color : "#FF8153"``
``},``
`` {``
``value : 30,``
``color : "#FFEA88"``
}
]

## Conclusion

The great things about Chart.js are that it’s simple to use and really very flexible. Plus, once you’ve mastered the basics here, you’ll discover that there are tons of options listed in the documentation.

## Basic usage of canvas

At first sight a ``<canvas>`` looks like the ``<img> ``element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the ``<canvas>`` element has only two attributes, width 

and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas 

will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

The id attribute isn't specific to the ```<canvas>``` element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance). It is always a good idea to supply an id because this makes it much easier to identify it in a script.

The `<canvas>` element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas. We'll see how this is done in a dedicated chapter of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.

## Fallback content

The ``<canvas>`` element differs from an ``<img>`` tag in that, like for `<video>`, `<audio>`, or` <picture>` elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the `<canvas>` element. Browsers that don't support `<canvas>` will ignore the container and render the fallback content inside it. Browsers that do support `<canvas>` will ignore the content inside the container, and just render the canvas normally.

## The rendering context

The ``<canvas>`` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The `<canvas>` element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics, such as those covered by this tutorial, you specify "2d" to get a CanvasRenderingContext2D.

## Drawing shapes with canvas

## The grid

Before we can start drawing, we need to talk about the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this 

canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue 

square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

![](https://media.prod.mdn.mozit.cloud/attachments/2012/07/09/224/70658d72d2408295cdfba55e6cd5fcc8/Canvas_default_grid.png)

## Drawing paths

A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

First, you create the path.
Then you use drawing commands to draw into the path.
Once the path has been created, you can stroke or fill the path to render it.
Here are the functions used to perform these steps:

`beginPath()`
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
Path methods
Methods to set different paths for objects.

`closePath()`
Adds a straight line to the path, going to the start of the current sub-path.
stroke()
Draws the shape by stroking its outline.

`fill()`
Draws a solid shape by filling the path's content area.
The first step to create a path is to call the beginPath(). Internally, 

paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes


## Lines

For drawing straight lines, use the lineTo() method.

lineTo(x, y)
Draws a line from the current drawing position to the position specified by x and y.
This method takes two arguments, x and y, which are the coordinates of the line's end point. The starting point is dependent on previously drawn paths, where the end point of the previous path is the starting point for the following, etc. The starting point can also be changed by using the moveTo() method.

This starts by calling beginPath() to start a new shape path. We then use the moveTo() method to move the starting point to the desired position. Below this, two lines are drawn which make up two sides of the triangle.

## Rectangles

In addition to the three methods we saw in Drawing rectangles, which draw rectangular shapes directly to the canvas, there's also the rect() method, which adds a rectangular path to a currently open path.

rect(x, y, width, height)
Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.

Before this method is executed, the moveTo() method is automatically called with the parameters (x,y). In other words, the current pen position is automatically reset to the default coordinates.

## Applying styles and colors

f we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color
Sets the style used when filling shapes.
strokeStyle = color
Sets the style for shapes' outlines.
color is a string representing a CSS `<color>`, a gradient object, or a 

pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).

## Transparency

In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke and/or fill style.

globalAlpha = transparencyValue
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.
The globalAlpha property can be useful if you want to draw a lot of shapes on the canvas with similar transparency, but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.

Because the strokeStyle and fillStyle properties accept CSS rgba color values, we can use the following notation to assign a transparent color to them.


## Using line dashes

The setLineDash method and the lineDashOffset property specify the dash pattern for lines. The setLineDash method accepts a list of numbers that specifies distances to alternately draw a line and a gap and the lineDashOffset property sets an offset where to start the pattern.

In this example we are creating a marching ants effect. It is an animation technique often found in selection tools of computer graphics programs. It 

helps the user to distinguish the selection border from the image background by animating the border. In a later part of this tutorial, you can learn how to do this and other basic animations.

`var ctx = document.getElementById('canvas').getContext('2d');`
`var offset = 0;`

`function draw() {`
  `ctx.clearRect(0, 0, canvas.width, canvas.height);`
  `ctx.setLineDash([4, 2]);`
  `ctx.lineDashOffset = -offset;`
 ` ctx.strokeRect(10, 10, 100, 100);`
`}`

`function march() {`
`  offset++;`
`  if (offset > 16) {`
    `offset = 0;`
  `}`
  `draw();`
 ` setTimeout(march, 20);`
`}`

`march();`

## Gradients

Just like any normal drawing program, we can fill and stroke shapes using linear and radial gradients. We create a CanvasGradient object by using one of the following methods. We can then assign this object to the fillStyle or strokeStyle properties.

createLinearGradient(x1, y1, x2, y2)
Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).

createRadialGradient(x1, y1, r1, x2, y2, r2)
Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.

## Drawing text

The canvas rendering context provides two methods to render text:

fillText`(text, x, y [, maxWidth]`)
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
strokeText(`text, x, y [, maxWidth]`)
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

## A strokeText example

`function draw() {`
  `var ctx = document.getElementById('canvas').getContext('2d');`
 ` ctx.font = '48px serif';`
 ` ctx.strokeText('Hello world', 10, 50);`
`}`

