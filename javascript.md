# What is "**Javascript?**"

# Scripts and Pages: pt 1

### Just like a recipe, handbook or manual! Steps must be laid out for someone with 0 knowledge to do!

## how to write a script

- Write out a goal
- List all the tasks necesary to achieve that goal
> flowchart
- Build Code for each step

Sketching a mocking up visual representation of the tasks is very helpful!

Event | Flowchart Key
|:----:|:---:|
| ```[]``` | Generic Step
| ```<=>``` | Event
| ```/=/ | Input or Output
| ```<>``` | Decision

# Expressions and Operators!

### Expression evaluates into a single value! 
> you can either assign an a value to a variable ```var color = 'beige'``` 
> OR you can use 2 or more variables to return an expression ```var area = 3*2``` 

### Operator are the groups of variables that return an expression

| Operator | Example | Return |
|:---:|:----:|:----:|
| Assignment Operator | Color = 'Beige' ; | Value of Color is now beige
| Arithmetic Operator | area = 3*2 ; | value of area is now 6
| String Operator | greeting = 'Hi' + 'Molly' ; | value of greeting is now 'Hi Molly'
| Comparison Operator | buy = 3 > 5 ; | value of buy is false
| Logical Operator | buy = (5>3) && (2<4) ; |  value of buy is true

![Arithmetic Operators](https://www.miltonmarketing.com/wp-content/uploads/2018/04/jsarithimage029.jpg) 

### REMEMBER THE ORDER OF OPERATIONS! PEMDAS!

## THERE IS ONLY 1 STRING OPERATOR, +
> adding strings puts them together, does not perform an arthimetical function

## Boolean Operators
    == - Equals 
    === - Strictly equals
    != - Not equal

# Functions! 

## Functions let you group a series of statements to perform a specific task. REUSABLE!

> informations passed to a function are called parameters

Funcation sayHello() {   <- FUNCTION 

}; 

Inside of the () are parameters! 

Inside a function, parameters act as variables

Arguments can be variables or values

# Logical Operators! 

## Logical Expressions are evaluated Left to Right

Symbol | Function
|:---:|:----:|
| && | Tests multiple conditions (And)
| ```||``` | Tests conditions for Or
| ! | Tests conditions nor Not


# Loops! 

### There are 3 different types of loops:
- For; a **For** loop usually uses the condition as a counter to tell how many times to loop
- While; a **While** loop usually uses an outside loop counter and will only run if the condition is **TRUE**
- Do While; a **Do While** loop runs like a while loop but will run even if the condition is **False**

### To create a loop counter
- Initialize with a variable ```(var i = 0)```
- Add a condition ```(i < 10)``` 
- Add an update ```(i++)```

'for (var i = 0; i < 10; i++) {
    Document.write(i);
}'

> This loop will write 123456789 until i=10 and then stop. After each loop i will be increased by 1 becasue of the ++

## While Loops 

'var i = 1;
var msg = '';

while (i < 10) {
    msg += i + ' x 5 =' + (i*5) + '<br />';
    i++;
}

document.write.getElementbyId('answer').innerHtml = msg'

> this loop creates a 5 times table until you get to 5x9
> as long as i < 10, then the script will loop

## Object Literals
What is an object? 
    - An object is a group of variables and functions to create a model of something you would recognize in the real world 

In an object a variable becomes a property and a function becomes a method

Key Value Organized

Properties: Tell us about the object, such as the name of the hotel or number of rooms it has
Methods: represent a task that are associated with the object such as checking the number of rooms available by subttracting the number of booked rooms from total rooms

Creating an object: Literal Notation
``` var hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25, 

    checkAvailability: function() {
        return this.rooms -this.booked;
    }
}; 
```

You can access the properties or methods of an object with . notation or bracket notations
``` var hotelName = hotel.name; ```

Objects can store all types of data that you would generally create in JS, including functions! 

this keyword is used to refer to the object itself 

## Document Object Model
the DOM tree is a model of a website stored in the browser's memory. A built in API for representing our content within our business logic!
| Document Node | The whole site |
| Element Node | The HTML elements |
| Attribute Node | the attribute of associate HTML elements | 
| Test Node | text within an element |

[Dom Tree](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)

To access and uodate the DOM tree: 
1. Locate the node that represents the element you want to work with
2. Use its text content, child elements, and attributes

### 1. Access Elements

#### Individual Elements
1. ``` getElementbyId()``` - use the value of an elements id attribute
2. ``` querySelector()``` - use CSS selectors to return the FIRST MATCHING element
3. you can also traverse through elements as well

#### Traverse Elements
1. ``` parentNode ``` Select the parent of the current element node
2. ``` previousSibling/nextSibling ``` Select previous or next sibling node
3. ``` firstChild/lastChild ``` Select the first or last child node of the current element

#### Multiple Elements 
1. ``` GetElementsByClassName() ``` Select all elements with a specific class value
2. ``` getElementsByTagName() ``` Select all the elements that have a specified tag
3. ``` querySelectorAll() ``` Select all of a certain CSS selector

### 2. Work with those Elements

#### Access/Update a text node
``` nodeValue ``` lets you access or update contents of a text node

#### Work with HTML content
``` innerHTML ``` Allows access to child and text elements
``` textContent ``` Access the text content
``` createElement() ``` Creates a new element
``` createTextNode() ``` Creates a new text node
``` appendChild() / removeChild() ``` add or remove a child node

#### Access or update attribute values
``` className / id ``` Updates the value of a class or ID attribute
``` hasAttribute() ``` Checks if an attribute exists
``` getAttribute()``` Gets the value of an attribute
``` removeAttribute()``` Removes an attribute
``` setAttribute()``` Sets an attribute

#### DOM Query
``` getElementById('one'); ``` - gets an element by the HTML ID 'one'
``` var itemOne = getElementById('one'); ``` - assigns the value of a variable itemOne as the element node with the ID 'one'

### DOM queries can return either a single node or a collection called a Node List
``` document.getElementById('one'); ``` gets the element with ID one from the object document

### Node Lists
Returns an array with each called element as an index item
    Access a element in a node list with ```NodeList.item(index#)```
    Preffered method is to access it like an array with ```[]```

### Example 
``` 
    var elements = document.getElementByClassName('hot); // Find 'hot' Items
        if (elements.length > 2) {    // If 3 or more are found in the node list
            var el = elements[2];      // Select the third index position in the Nodelist
            el.className = 'cool';     // Change the class name attribute to 'cool'
    }
``` 
Loop through a nodelist using a for() loop with the node list.length as the amount attribute

Beware of Whitespace nodes created by some browsers. Be as direct as possible when targeting nodes

``` document.getElementById('one').firstChild.nextSibling.nodeValue ```
1. The <li> element node is selected by ID
2. the first child of <li> is the <em> element
3. the text node is the next sibling to the <em> element
4. The text node has been indentified and you can access it's contents using .nodeValue

Avoid editing node content with textContent and innerText 

Store the original HTML in a variable then add attributed tags using innerHTML

``` createElement() ``` create a new element node using the parameters in the parenthesis
``` createTextNode() ``` creates a new text node with the parameters in the parenthesis
``` appendChild() ``` allows you to add a child node to a specific element node

### Be Aware of Cross Site Scripting Attacks! 
 - to counter, validate input that is going into a server as the input you want/expect
 - "Escape" all characters so that they are shown as characters and not run as code!
- ``` encodeURIComponent()``` encodes most characters for user input
#### Do not allow users to generate content directly into HTML elements


### Change attributes of a node
    - access using .getAttribute()

### Properties in the chrome dev tools can let you see the DOM list you re currently targeting

## Constructor notation

var hotel = new Object();

hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;

hotel.checkAvailability = function() {
    return this.rooms - this.booked
}

1. create new object - var hotel = new Object; 
2. Add properties - hotel.name = "Quay" ;
3. Add methods using dot notation hotel.checkAvailability = function() {}

function Hotel(name, rooms, booked) {
    this.name = name;
    this.rooms = rooms;
    this.booked = booked; 

    this.checkAvailability = function() {
        return this.rooms - this.booked
    }
} 

invoke the above object with:

var quayHotel = new Hotel('Quay', 40, 25);
    var parkHOtel = new Hotel('Park', 120, 77); 

To delete a property, use the Delete key word before the variable 

this. is as keyword to refer to the same object you are currently in

### You can combine arrays and objects to create complex data structures! 
An Array can be held in an object and objects can be held in arrays

### Browser Object Models
1. window - current window or tab
2. document - current page
3. history - pages in browser history
4. location - url of current page
5. navigator - information about browser
6. screen - device's display information
7. String Objects
8. Number objects
9. Math objects
10. Date/Time objects - You must create a Date() object and define it to be able to use date object models

## EVENTS
Interactions create events -> Events trigger code -> Code responds to the user

#### UI Events
- load - when the webpage finishes loading
- unload - then the webpage unloads
- error - when the browser encounters a JS error or missing asset
- resize - when the browser window is resized
- scroll - user scrolls up or down the page

####  Keyboard Events
- keydown - first press of a key (repeats while held down)
- keyup - the key is released
- keypress - a character is being inserted (repeats while held down)

#### Mouse Events
- click - user depresses and releases mouse
- dbclick - doubleclick
- mousedown - when a user presses a mouse down
- mousemove - when a use moves the mouse (not touch screen)
- mouseover - when a user moves over an element
- mouseout - when a user moves the mouse off an element

#### Focus Events
- focus/focusin - when an element gains focus
- blur/focusout - when element gains focus

#### Form Events
- input - value in any ```<input>``` or ```<textarea>``` element has changed
- change - value in a selectbox, checkbox, or radio button changes
- submit - when a user sbmits a form
- reset - when a user clicks a reset button (rare)
- cut - when a user suts content from a field
- copy - when a user copies content from a field
- paste - when a user pasts content into a field
- selects - when a user selects a form in the field

#### Mutation Events
- DOMsubtreeModified - change has been made to the document
- DOMnodeInserted - when a node is inserted as a direct child of another node
- DOMnodeRemoved - a node has been removed from another node
- DOMnodeinsertedintoDocument - when a node has been inserted as a descendant of another
- DOMnodeRemovedFromDocument - when a node has been removed as the descendant of another

### Select the Element node(s) you want the script to respond to -> Indicate which event on the selected node wil trigger the response -> State the Code you want to run when the event occurs

DOM event handlers
```DOMelement.onevent = functionName ;``` 
- you must declare the DOMelement as a variable ->  var DOMelement

DOM Event Listener 

``` DOMelement.addEventListener('event', function[, boolean]); ```

You can call a function with parameter inside of an event listener

IE sucks


## Error Handling and Debugging
Follow the *order of execution*
- Global Context -> Function Context -> Eval Context

**The Javascript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks the new function on top of the current task**
1. Prepare - new scope is created; variables, arguments and functions are created
2. Execute - Assign value to a variable; reference functions and run code; execute statments

| Object | Description |
|:---:|:----:|
| Error | Generic error |
| SyntaxError | Syntax has not been followed |
| ReferenceError | Tried to reference a variable that is not declared/within scope |
| TypeError | Unexpected data type that cannot be coerced |
| RangeError | Numbes not in acceptable range | 
| URIError | encoder or decoder used incorrectly | 
| EvalError | eval() function used incorrectly | 


## JQuery! 

#### JQuery selects elements, performs tasks, and handles events

1. Find an Element
    ``` jquery 
    $('li.hot')
    ```
    function creates a jQuery object
2. Do something to the element
    ``` jquery
    $('li.hot').addClass('complete');
    ```
    . is a member operator that invokes a method
    you pass parameters into the method

invoke the jquery with a script tag in the HTML

Jquery selects elements and places them into an array with an index value starting at 0

from an element you can:
    get information or set information

JQuery objects store references to elemnts, not copies

To cache a Jquery element use, $listItems = $('li');
    This allows you to call upon the object across pages
Jquery will automatically loop through all selected elements and apply the method

You can chain multiple Jquery methods together using .notation

ready() checks to see if you document is 'ready' for Jquery code

``` jquery
$(document).ready(function(){
    // SCRIPT HERE
});
```
    This allows you to place <script> tags anywhere on the page and have Jquery load when it is ready

   - .load(), .on() - runs Jquery after everything on the page has loaded
    - ready() - runs Jquery as soon as the DOM is loaded
    - If you place the script tag after all of the HTML elements, the DOM will load and allow the script to access the loaded DOM

.html() - retrieves the first element in a matched set and returns the the element with all of it's descendents

.text() - retrieves only the text elements from the first matched element

.replaceWith() - replaces every element in a matched set with the new content

.remove() - removes all elements in the matched set

.before() - inserts content before the element
.after() - inserts content after the element
.prepend() - inserts content after the opening tag
.append() - inserts content before the closing tag

.attr() - get or set an attribute value
.removeAttr() - remove an attribute
.addClass() - adds a new value to the existing class value
.removeClass() - removes a value from the existing class value
.css() - gets or sets a new CSS class to the element
.each() - allows you to perform one or more statements to each element returned (like a loop)
this or $(this) - access the current element

Jquery Events
.on() - starts an event handler
| Environment | Command | 
|:-----:|:-----:|
| UI | focus, blur, change | 
| Keyboard | input, keydown, keyup, keypress |
| Mouse | click, dblclick, mouseup, mousedown, mouseover, mousemove, mouseout, hover |
|form | submit, select, change| 
|document | ready, load, unload |
|browser | error, resize, scroll | 

### Call Stack

a mechanism for an interpreter to keep track of its place in a script that calls multiple functions.

    - When a script calls a function the interpreter adds it to the call stack and starts to execute the function
    - any functions that are called are added further up the call stack and run when reached
    - when the current function finishes, the interpreter takes it off the stack and resumes execution where it last left off
    - if a stack takes up more space that assigned, it will result in "stack overflow' error

1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

Reference Error - Tried to use a variable that is not yet declared
Syntax Error - cannot be parsed in terms of syntax
Range Error - .length error, can be avoided by minimizing mutations
Type Error - Variable is no the right type
