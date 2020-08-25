# Responsive Layouts with CSS Grid

the same way that flexbox gave us a way to layout block elements next to each other, CSS

 grid lets us not only arrange elements in a row or a column, but in multiple rows and 
 
 columns. Finally two dimensional layouts are becoming simpler.

 The smaller images (in a grid!) are in the perfect layout to get you started with CSS grid. Grid gives us control over how wide or narrow each of the ‘grid cells’ get. This allows us to maintain a sensible aspect ratio to their height. In this example I’ve used:

 ``grid-template-columns: repeat(auto-fill, ```minmax(250px, 1fr));``

 The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.


In this case, for the first argument, I’ve used auto-fill which will create a grid with 

as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to minmax(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a 

maximum of 1fr. An fr is a ‘fraction unit’, a unit of measurement to define a fraction of the available space of the container. The width of the elements in the row will increase from 250px until the point where another element could potentially fit beside the first. Try changing the width of your browser while looking at the example to see this in action.

``object-fit: cover;``

![](https://miro.medium.com/max/700/1*P9QGSeySIUM14lsFDYL-rw.gif)



 