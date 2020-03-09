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

You can access the properties or methods of an object with . notation
``` var hotelName = hotel.name; ```

## Document Object Model
the DOM tree is a model of a website stored in the browser's memory
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
    - access using ``` .getAttribute() ``` 

### Properties in the chrome dev tools can let you see the DOM list you re currently targeting
