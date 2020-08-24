
# Templating with Mustache

Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.

It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are 

replaced with a value, some nothing, and others a series of values.

![](https://miro.medium.com/max/700/1*P9q0tkeaRY2l1JOXaVKAig.png)

``Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });``
``// returns: Hello, Sherlynn``


In the above, we see two braces around {{ name }}. 

This is Mustache syntax to show that it is a placeholder. When Mustache compiles this, it will look for the ‘name’ property in the object we pass in, and replace {{ name }} 

with the actual value, e,g, “Sherlynn”.In the above, we see two braces around {{ name }}. This is Mustache syntax to show that it is a placeholder. When Mustache compiles this, it will look for the ‘name’ 

property in the object we pass in, and replace {{ name }} with the actual value, e,g, “Sherlynn”.

## Mustache-Express

If you intend you use mustache with Node and Express, you can use mustache-express. Mustache Express lets you use Mustache and Express together easily.

``$ npm install mustache --save``

![](https://miro.medium.com/max/700/1*ES10lxr7tdRFVEKcRAgLEw.png)

# A Guide to Flexbox

**display**


This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.
![](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)

``.container {display: flex; /* or inline-flex */}``

## flex-direction

This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying

 out either in horizontal rows or vertical columns.

 ``.container {flex-direction: row | row-reverse | column | column-reverse;}``


 ## flex-wrap

By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.

``.container {flex-wrap: nowrap | wrap | wrap-reverse;}``

- nowrap (default): all flex items will be on one line
 
- wrap: flex items will wrap onto multiple lines, from top to bottom.

- wrap-reverse: flex items will wrap onto multiple lines from bottom to top.

## flex-shrink



``.item {flex-shrink: 3; /* default 1 */}``

## flex

This is the shorthand for flex-grow, flex-shrink and flex-basis combined. The second and third parameters (flex-shrink and flex-basis) are optional. The default is 0 1 auto, but if you set it with a single number value, it’s like 1 0.

``.item {flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]``

