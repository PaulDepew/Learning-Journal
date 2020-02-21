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