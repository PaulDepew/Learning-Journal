# Duckett HTML and CSS: Chapter 1  

## What is the Structure of a website?  
- HTML: Content
- CSS: Style  

## START WITH !DOCTYPE=

### For HTML, start structuring the element tags like
- ```<HTML>``` 
- ```<Head>``` 
- ```<Title>```
- ```<body>```
- ```<footer>```

### Then start to populate the HTML with content tags
- ```<H1> etc```
- ```<a href="">```
- ```<img a href="">```
- ```<p>```

All tags can also have an Attribute followed by a Value  
> ```<p lang="eng-us">```  

## VIEW SOURCE TO SEE HOW OTHER SITES ARE BUILT! 

# Lists and Boxes! 

### Tag | List style |
|:---|:---:|
| '<ul>' | creates and unordered list,  displays your list items in whatever order they are entered
|'<ol>' | creates a numbered list based on the list items
| '<dl>' | creates a list that is defined with indentation
| '<ul>' | Nested lists are unordered lists that are lined up in nested style

# Boxes! 

### All HTML elements on a page have an invisible box surrounding them
   - you can define the width and heigth 
   - you can limit the width and heigth
   - You can also allow it to overflow using it's own scroll bar independent of the rest of the page
   [Border, margins, padding](https://www.avajava.com/tutorials/cascading-style-sheets/how-are-margins-borders-padding-and-content-related/how-are-margins-borders-padding-and-content-related-01.gif) 
   - Change how an element displays using a display property
   - Hide borders
   - make a border-image
   - add a box-shadow 
   - round corners using Border-radius
      - Make a circle by showing a block with a border, then adjust the corner radius until it becomes a circle
   - you can provide : to adjust an action element of an HTML tag ie. a:hover will change how all 

# Duckett HTML and CSS: Chapter 8  

## Extra Markup styles  
> HTML5 is the current version of HTML to use  
You must specify the DOCTYPE at the beginning of the file to define the language used  
```<!-- --!>``` = Non-Diplayed comment on the code 

### ID Attributes: Change Attributes to a specific element on a page
### Class Attributes: Any element on a webpage can be given a defined class but those classes will all follow the same CSS defined attributes. You can also give multiple classes to the same item

### Block Elements: Things that automatically format into a block  
### Inline Elements: Things that automatically format into a line  

> ```<div>``` = Create a group in a block element  
> ```<span>``` = Create a group inline  

> ```<iFrame>``` = A window that allows another website to be displayed and interacted with on your page  

> ```<Meta>``` = Lives in the <head> tag. Provides descriptions, keywords, robots, authors, pragma and cache expiration timing  

### [WATCH FOR SPECIAL HTML5 RESERVED CHARACTERS!](http://www.htmlandcssbook.com/extras/html-escape-codes/)
> They will need a special display code if used  


# Duckett HTML and CSS: Chapter 17  

## HTML5 Layout  
> Previously you had to ID your <div> sections to make them seperated. HTML5 has specific <dic> tags so you do not need to ID all of them.  
- ```<header>``` = top
- ```<nav>``` = under header
- ```<article>``` = Replicable content piece
- ```<aside>``` = Relevant content to the main content
- ```<section>``` = A group of content
- ```<hgroup>``` = A group of header tags
- ```<figure <figcaption>``` = Content referenced in an article (images, videos, graphs, etc) 
- ```<div>' = alternative content block
- ```<footer>``` = Bottom of Page

### Older browsers need to be told which elements are Block elements using Javascript   




# Duckett HTML and CSS: Chapter 18

## Questions to ask:
> Who is visiting the site?
> What information do they want?
> What information do you want to present?

Individuals vs Companies:

Individuals | Companies
|:---:|:---:|
Age range?  | Size of the company?
Women or Men? | Position of visitors?
What country? | For themselves or other things?
Urban or Rural? | Budget?
Income? | -
Level of Education? | -
Marital status? | -
Occupation? | -
Hours per week worked? | -
What kind of device? | -

### What are the goals of someone coming to your site?
### What are their key motivations? Specific goals?
### Is this a luxury site? Essential Site? Fun? Daily?

### What information does a consumer need from your site?
	> Are they familiar with your brand or products?
	> Are they familiar with your presence?
	
### How often do they visit your site?
	> Does it need to be updated?
	

## Creation Steps:
### 1. Site Map: Layout of the pages on your site
  > Card Sorting: Pertinent visitor information on each card then organized into a site map  
### 2. Wireframe: Simple sketch of the elements that go on a page    



+ Content Creation
+ Visual Hierarchy
   - Size
   - Color
   - Style
   - Images  
+ Content Organizing: Consistency and Headings
   - Proximity
   - Closure
   - Continuance
   - White Space
   - Color
   - Borders

Navigation:  
- Concise
- Clear
- Selective 
- Context 
- Interactive
- Consistent

## Tables! 
| Tag | Function| Description| 
|:-----:|:-----:|:-----:|
| ```<table>``` | Table intializer | Defines the following elements as being in a table |
| ```<tr>``` | Table row | starts a new row of data cells |
| ```<td>``` | Table data | the cell in a row |
| ```<th>``` | Table heading | boldens the data in each cell | 

use the attribute colspan="#ofcolumnstospan" to span a cell across multiple columns
use the attribute rowspan="#ofcolumnstospan" to span a cell across multiple rows

you can make long tables by using ```<thead>``` for header cells, ```<tbody>``` for body cells, and ```<tfoot>``` for footer cells
CSS styles can be applied to table elements

## Layout!
Block level elements alwaysw start on a new line
Inline elements flow between surrounding text

If there is an element inside of another element, that element is the *Parent* and is *Containing* the *child* element

You can control elements with:

1. Normal Flow
2. Relative positioning
3. Absolute Positioning
4. Fixed positioning
5. Floating Elements
   - the z-index controls the layer order

You can 'clear' a float to say that no element should touch another elemnts within the same containing element

Utilize floated Columns to create layouts for webisites

You can import multiple style sheets to the same html

## Forms!

3 types of form controles:
1. Adding text
2. Making Choices
3. Submitting Forms

Steps of a Form:
1. A user fills in a form then presses a button to submit information to a server
2. The name of each form control is sent to the server with the value the user entered
3. The server processes the information using a programming language like:
   - PHP
   - C#
   - VB.net
   - Java
4. The server creates a new page to send back to the browser

FORMS BY DEFAULT REFRESH THE BROWSER PAGE ON SUBMISSION!
.preventDefault(); keeps the page from reloading



### All forms have a Name=aValue

### Form Structure

``` <form action="link" method="get or post">```
get = adding the values of the form to the end of the URL specified in the form
   - best for short forms and retrieving data from a server
post = sent in HTML headers to the specified URL
   - best for uploading a file, long files, sensitive data, adds or deletes info from a database
Forms can had id attributes!

```<input type="text" name="username" size="15" maxlength="30"  />```

input - the type of input - the return variable - do not use size, USE CSS - limits number of characters

### Types
1. Text
   - Inputs text 
2. Password 
   - Blocked out string
3. ```<Text Area>``` 
   - For multi line input
   - ~cols="width"~ USE CSS
   - ~rows="height"~ USE CSS
4. Radio
   - Allows for a checked box
   - Create multiple inputs with multple values 
   - the checked attribute allows you to pre-select an option
5. Checkbox
   - Allows for multiple check box inputs
6. Select
   - Allows for a drop down list with multiple options
   - ```<Select name="value">```
         ```<option value="ipod">iPod</option>```
   - with the multiple attribute, you can allow for multiple inputs from the list
7. file
   - Allows for file input box
8. submit
   - sends a form to the server
9. image
   - image allows you to add a src to put an image as the submit button
10. button
   - allows you to create a button element
   - allows for multiple things to be held inside of a button
11. hidden
   - allows for a form to be submitted without user knowledge/automatically
12. date
   - Allows the user to input a date
13. email
   - Allows the user to email address
14. url
   - Allows a user to enter a URL
15. search 
   - allows a suer to seach a page
   - use the placeholder attribute for "placeholder" text

### You can label form inputs with the ```<label>``` tag 
   - give the input an id and add a for attribute to the label html
### Group form elements between ```<fieldset>``` tags
   - use ```<legen>``` directly after to put a text element onto the form
Use the required attribute to force a form element to be submitted

## Lists, Tables and Forms! 

In CSS there are many ways to style lists forms and tables
### Lists
1. list-style-type: 
   - none
   - disc
   - square
   - circle
2. list-style-image:
   allows you to use an image as a bullet point
3. list-style-position:
   - outside = outside the block of text
   - inside = inside the block of text
4. list-style
   - short hand for all of the above

### Table Properties
1. width
2. padding
3. text-transform (to uppercase)
4. border-top/bottom
5. text-align
6. background-color (alternating table rows)
7. :hover (highlight a table row when hovering over it)
8. empty-cells
   - show - shows borders of empty cells
   - hide - hides borders of empty cells
   - inherit - inherit rules of the table element
9. border-spacing
10. border-collapse

### Forms
1. font-size
2. color
3. background-color
4. border
5. border-radius
6. :focus
7. :hover
8. background-image

Cursor: Allows you to change the hovered cursor over the element

