#
### ORDER OF EXECUTION
To find the source of an error, it helps to know how scripts are processed.

The order in which statements are executed can be complex; some tasks
cannot complete until another statement or function has been run.
### EXECUT.ION CONTEXTS

The JavaScript interpreter uses the concept of execution contexts.
There is one global execution context; plus, each function creates a new
new execution context. They correspond to variable scope.

GLOBAL CONTEXT
Code that is in the script, but not in a function.

- There is only one global context in any page.
FUNCTION CONTEXT
Code that is being run within a function.
Each function has its own function context.

- GLOBAL SCOPE
If a variable is declared outside a function, it can
be used anywhere because it has global scope.
If you do not use the var keyword when creating
a variable, it is placed in global scope.
- FUNCTION-LEVEL SCOPE
When a variable is declared within a function,
it can only be used within that function. This is
because it has function-level scope.
### EXECUTION CONTEXT & HOISTING 
Each time a script enters a new execution context, there are two phases
of activity:
1- 1: PREPARE
• The new scope is created
• Variables, functions, and arguments are created
• The value of the this keyword is determined
Understanding that these two phases happen helps
with understanding a concept called hoisting. You
may have seen that you can:
• Call functions before they have been declared
(if they were created using function declarations
 2- execution
• Assign a value to a va ria ble that has not yet been
declared
This is because any variables and functions within
each execution context are created before they are
executed.

The preparation phase is often described as taking
all of the variables and functions and hoisting them
to the top of the execution context.

 Or you can think
of them as having been prepared.
Each execution context also creates its own
vari ab 1 es object. This object contains details of all
of the variables, functions, and parameters for that
execution context.
### UNDERSTANDING SCOPE
In the interpreter, each execution context has its own va ri ables object.
It holds the variables, functions,
 and parameters available within it.
 
Each execution context can also access its parent's variables object.
- **If a variable is not found in the variables object
for the current execution context, it can look in the
variables object of the parent execution context.
But it is worth knowing that looking further up the
stack can affect performance, so ideally you create
variables inside the functions that use them.**


### UNDERSTANDING ERRORS

If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code.
## ERROR OBJECTS

Error objects can help you find where your mistakes are
and browsers have tools to help you read them.
**OBJECT#**| **discreption**
 --------|--------
 Error   |Generic error - the other errors
are all based upon this error
  Syntax Error|Syntax has not been followed
 TypeError|An unexpected data type that
cannot be coerced

- Syntax Error
SYNTAX IS NOT CORRECT
This is caused by incorrect use of the rules of the
language. It is often the result of a simple typo.
MISMATCHING OR UNCLOSED QUOTES
document .write ("Howdyl );
SyntaxError: Unexp ec t ed EOF

MISSING CLOSING BRACKET
document .getElementByid('page' I
SyntaxErr or : Expected token ' ) '

MISSING COMMA IN ARRAY
Would be same for missing] at the end
var l ist = ['Item 1', 'Item 2 ' l 'rtem 3'];
SyntaxError: Expected token ']'.

- URI Error
INCORRECT USE OF URI FUNCTIONS
If these characters are not escaped in URls, they will
cause an error: / ? & I : ;

- Ref erenceError
VARIABLE DOES NOT EXIST
This is caused by a variable that is not declared or is
out of scope.
VA RIABLE IS UNDECLARED
var wi dth = 12 ;

var area = width * llt!ftNU! ;
ReferenceError: Can ' t find vari able:
height
NAMED FUNCTION IS UNDEFINED
document.write ( randomFunction() ) ;
ReferenceError: Can't find variable :
randomFunction URI.

### HOW TO DEAL WITH ERRORS
1: DEBUG THE SCRIPT TO FIX ERRORS
If you come across an error while writing a script
(or when someone reports a bug), you will need to
debug the code, track down the source of the error,
and fix it.
You will find that the developer tools available in
every major modern browser will help you with
this task. In this chapter, you will learn about the
developer tools in Chrome and Firefox. 


2: HANDLE ERRORS GRACEFULLY
You can handle errors gracefully using try, catch,
throw, and f i na1ly statement s.

### A DEBUGGING WORKFLOW
Debugging is about deduction: eliminating potential causes of an error.

-**WHERE IS THE PROBLEM?**

First, should try to can narrow down the area where
the problem seems to be. In a long script, this is especially important.

- **WHAT EXACTLY IS THE PROBLEM?**
Once you think that you might know the rough area
in which your problem is located, you can then try to
find the actual line of code that is causing the error.

### BROWSER DEV TOOLS & AVASCRIPT CONSOLE
 The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.
- CHROME/ OPERA
On a PC, press the F12 key or:
1. Go to the options menu (or three line menu icon)
2. Select Toots or More tools.
 
3. Select JavaScript Console or Developer Tools
On a Mac press Alt + Cmd + J. Or:

1. Go to the View menu.

2. Select Developer.

3. Open the JavaScript Console or Developer - 

 
 - Tools
option and select Console.
INTERNET EXPLORER
Press the F12 key or:
1. Go to the settings menu in the top-right.
2. 
3. Select developer tools.
  ### The JavaScript console is just one of severa l developer tools that are found in all modern browsers.

![](https://www.wickedlysmart.com/wp-content/uploads/2014/03/win-chrome-2-1.png)

### WRITING FROM THE SCRIPT TO THE CONSOLE
Browsers that have a console have a console object, which has several
methods that your script can use to display data in the console.
The object is documented in the Console API.

![](https://www.kirupa.com/html5/images/fetch_console2.png)

### BREAKPOINTS

*You can pause the execution of a script on any*
*line using breakpoints. Then you can checkthe*
*va lues stored in variables at that point in time.*

If you know your code might fail, use try, catch, and finally.
Each one is given its own code block.

-**TRY**
First, you specify the code
that you t hink might throw an
exception within the try block.
If an exception occurs in this
section of code, control is
automatically passed to the
corresponding catch block.

The try clause must be used in
this type of error handling code,
and it should always have either
a catch, fi na 1 ly, or both.
If you use a continue, break, or
return keyword inside a try, it
will go to the f i na 11 y option.
 
- **CATCH**
If the try code block throws an
exception, catch steps in with an
alternative set of code.
It has one parameter: the error
object. Although it is optional,
you are not handling the error if
you do not catch an error.

The ability to catch an error can
be very helpful if there is an issue
on a live website.

It lets you tell users that
something has gone wrong
(rather than not informing them
why the site stopped working).
- FINALLY
The contents of the fi na 11 y
code block will run either
way - whether the try block
succeeded or failed.
It even runs if a return keyword
is used in the try or catch block.
It is sometimes used to clean up
after the previous two clauses.
These methods are similar
to the .done(), . fail() , and
. a 1 ways() methods in jQuery.
You can nest checks inside each
other (place another t ry inside a
catch), but be aware that it can
affect performance of a script.

