#  The JQUERY

offers a simple way to achieve a variety of common
JavaScript tasks quickly and consistently, across all major

browsers and without any fallback code needed.

- the JavaScript file uses the
``$ ()`` shortcut for the jQuery ()
function. It selects elements and
creates three jQuery objects that
hold references to the elements.

``$(' :header').addClass('headline');``
``$(' l i : lt(3) ').hide(). fadeln(lSOO);``
``$('li').on('click', function() {``
``$(this) . remove();``
``} )``

## WHY USE JQUERY?

1- SIMPLE SELECTORS


it is not always easy to select the elements
that you want to. For example:
-  Older browsers do not support the latest
methods for selecting elements.

-  IE does not treat whitespace between elements
as text nodes, while other browsers do.

2- COMMON TASKS IN LESS CODE
There are some tasks that front-end developers
need to do regularly, such as loop through the
elements that have been selected.

jQuery has methods that offer web developers
simpler ways to perform common tasks, such as:
- loop through elements
-  Add I remove elements from the DOM tree

-  Handle events
 
-  Fade elements into I out of view.

-  Handle Ajax requests.

## FINDING ELEMENTS4

Using jQuery, you usually select elements
using CSS-style selectors. 

It also offers some
extra selectors, noted below with a 'jQ'.

**BASIC SELECTORS**

- *
- element
- #id
- .class
- selectorl, selector2

**HIERARCHY**

- ancestor descendant
- parent > child
- previous + next
  
  ## UPDATING ELEMENTS

  - . html()
This method gives every element
in the matched set the same new
content. The new content may
include HTML.
- .replaceWith()
This method replaces every
element in a matched set with
new content. It also returns the
replaced elements.
- . text()
This method gives every element
in the matched set the same new
text content. Any markup would
be shown as text.
- . remove()
This method removes all of the
elements in the matched set.

## GETTING & SETTING CSS PROPERTIES4

The ``. css ()`` method lets you retrieve
and set the values of CSS properties.

``var backgroundColor = $( ' li ' ) . css( 'background-color' );``

## EVENT METHODS

The`` • on ()`` method is used to handle all events.
Behind the scenes, jQuery handles all of the
cross-browser issues you saw in the last chapter.

``$listltems.on('mouseover click', function(){}``

## ADDITIONAL PARAMETERS FOR EVENT HANDLERS

The`` • on ()`` method has two optional properties that let you:
Filter the initial jQuery selection to respond to a subset of the elements;
Pass extra information into the event handler using object literal notation.


.`` on(events[, selector][, data], function(e) );``

## TRAVERSING THE DOM

When you have made a jQuery selection, you
can use these methods to access other element
nodes relative to the initial selection.

• find() All elements within current selection that match selector

. closest() Nearest ancestor (not just parent) that matches selector

.parent() Direct parent of current selection

. siblings() All siblings of current selection

## LOADING JQUERY FROM A CDN

This is known as a protocol
relative URL. If the user is
looking at the current page
through https, then they will not
see an error that tells them there
are unsecure items on the page.

``<script src=" //ajax .googl eapi s . com/ ajax/l i bs/ jquery / 1.10 . 2````jquery .min. js "></ script>``

# JQUERY DOCUMENTATION
For an exhaustive list of the functionality
provided in jQuery, visit http ://api . j query .com

# pair programer

While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language: Listening: hearing and interpreting the vocabulary Speaking: using the correct words to communicate an idea Reading: understanding what written language intends to convey Writing: producing from scratch a meaningful. 

During a five-hour paired lab session, Code Fellows students work on all four of these language-specific skills. The abilities they foster will serve them well in completing assignments, in their own communication and learning, in interviews, and in readiness for a job at a company that utilizes this agile practice.
 1- **Greater efficiency**
It is a common misconception that pair programming takes a lot longer and is less efficient. In reality, when two people focus on the same code base, it is easier to catch mistakes in the making. Research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging (let alone exposing users to a broken product).
2-**Engaged collaboration**
When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone. It is harder to procrastinate or get off track when someone else is relying on you to complete the work. Popping open your Facebook timeline is just that less enticing when someone else is looking at your screen.
3- **Job interview readiness**
A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.
4- **Work environment readiness**
Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.