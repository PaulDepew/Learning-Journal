# What is "**CSS?**"

## Ducket Chapter 10  

## Cascading Style Sheets

### CSS is a Selector (Untagged tag) followed by a declaration {} filled with style attributes
   > Attributes are a property followed by a value

  a {

       Background-color:Blue
   }

### CSS is top to down and imagining there is a box around every HTML element

### You must link the .css file in the head of the HTML, you can link multiple .css files to the same HTML document

Classes = . example .thisisaclass  
ID = #   example #thisisanID

Classes select multiple tags  
ID selects a single tag (supposed to)

| Selectors | Meaning | Examples |
|:-----:|:--------:|:------:|
| Universal Selector | Applies to all elements of a document | * {} Targets all elements on a page
| Type Selector | Matches Elements Name | h1, h2, h3 {} Targets ```<h1>,<h2>, and <h3>```
| Class Selector| Matches an element who's class attribute matches | p .note {} Targets all ```<p>``` tags with the class attribute :note
| ID Selector | Matches an element who's ID attribute matches | #introduction {} Targets the Introduction ID attribute
| Child Selector | Matches the element that is a direct child of another | li **>** a {} Targets all ```<a>``` tags that are children of ```<li>``` tags
| Descendant Selector |  Matches the element that is a descendent of another | p a {} Targets all ```<a>``` tags that are descendents of ```<p>``` tags
| Adjacent Sibling Selector | Matches an element that is the next sibbling of another | h1+p {} Targets the FIRST ```<p>``` after any ```<h1>``` element, but not others
| General Sibling Selector | Matches an element that is the sibling of another | h1~p {} Targets all ```<p>``` siblings of the ```<h1>``` element  



> if two selectors are identical the one farther down in the file will take precedence  
> the more specific rule will take precedence
> add !important to inflate the importance of a CSS element

### Some Elements will be inherited by descended tags (ie. Font-family or Color) 
###  Some elements will not be inherited (ie. Background-color or Border-Properties)
 
 ### if you use "Inherit" as the Attribute, the element will automatically inherit the CSS attributes of it's parents

 Some browsers do not display CSS that same. These are called "Browser quirks" 
Check using:  
    * Broswercam.com  
    * Browserlab.adobe.com  
    * Browsershots.org  
    * Crossbrowsertesting.com  

Check quirks using:   
    * positioniseverything.net  
    * quirksmode.org


## Duckett Chapter 11

### Colors! 

| Code | Function | Example
|:-----:|:-------:|:-------:|
| Color | Text/Foreground Color | h1 {color: Dark Blue;}
| background-color | Background Color | body {background-color: Dark Red;}
| opacity | Opacity | p {opacity: .5;}
| HSL |  Hue, Saturation, Lightness| body {background-color: hsla(0,100%,75%,.25;)}

You can use **RGB** values, **Hex** codes, or **Color Names** to choose your color attribute
CSS3 also allows for HSL color values, (Numerical Hue Value, Numerical Saturation Value, Numerical Lightness Value, Numerical Alpha(transparency) Value)

### When choosing colors be sure to proovide enough contrast between elements so things appear clear  
> Stay in the High to Medium Contrast zones for text

# Images

### save your images in an images directory for your site

to add an image use the `<img>` tag with the src, alt and title attribute

### `<img>` is an inline element

set the alignment using the align attribute

use jpg, gif or png files!

you can add a caption by wrapping the img in a `<figure>` tag with `<figcaption>` around the text element

# Text

### what kind of text?
    - serif
    - sans serif
    - monospace
adjust the kerning with 
    - letter-spacing
    - word-spacing

text align and vertical align
- 