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
text.
