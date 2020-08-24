
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