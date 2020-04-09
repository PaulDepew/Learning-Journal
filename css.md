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

### Chart.JS!!!
Chart.js is an open source script to help easily make graphs

First you must download Chart.js and load it into the directory you would like to use it in. 
- ``` <script src='chart.min.js'></script> ```

#### Line Chart
Define the Chart area
``` <canvas id="buyers" width="600" height="400"></canvas> ```

Script to get the canvas content

```
<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script> 
```
Define the Data and style

``` 
var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
```

Pie Chart
```
var pieData = [
	{
		value: 20,
		color:"#878BB6"
	},
	{
		value : 40,
		color : "#4ACAB4"
	},
	{
		value : 10,
		color : "#FF8153"
	},
	{
		value : 30,
		color : "#FFEA88"
	}
];

var pieOptions = {
	segmentShowStroke : false,
	animateScale : true
}
```

Bar Chart 

```
var barData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "#48A497",
			strokeColor : "#48A4D1",
			data : [456,479,324,569,702,600]
		},
		{
			fillColor : "rgba(73,188,170,0.4)",
			strokeColor : "rgba(72,174,209,0.4)",
			data : [364,504,605,400,345,320]
		}

	]
}
```

Drawing with Canvas

Rectangles
- fillRect(x, y, width, height) - filled rectangle
- strokeRect(x, y, width, height) - outlined rectangle
- clearRect(x, y, width, height) - clears a rectangular area

Paths 
- beginPath() - start a path
- Path Methods are used to set different paths for objects
- closePath() - add a straight line to the path
- strike() - draws a shape by stroking an outling
- fill() - draws a solid shape in the content area
- lineTo(x,y) - draw a straight line to one position to another
- arc(x,y,startAngle,endAngle, anticlockwise)
- arcto(x1, y1, x2, y2, radius)
- quadraticCurveTo(cp1x, cp1y, x, y)
- bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
- Path2D() - constructor to return newly initiated path2d object

svg path - var p = new Path2D('M10 10 h 80 v 80 h -80 Z');

fillstyle = color 
strokestyle = color

globalAlpha = tansparencyValue

lineWidth = value

lineWidth = value

lineJoin = type

miterLimit = value

getLineDash()

setLineDash(segments)

lineDashOffset = value

fillText(text, x, y [, maxWidth])
strokeText(text, x, y [, maxWidth])

## CSS transitions

transform property is very powerful!

Rotation
Scale
Translate
Skew
	- Origin

Perspective

Transitions! 

FADE
```css
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```
CHANGE COLOR

```css 
.color:hover
{
        background:#53a7ea;
}
```
GROW AND SHRINK
```css 
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```
SHRINK
```css 
.shrink:hover
{
        -webkit-transform: scale(0.8);
        -ms-transform: scale(0.8);
        transform: scale(0.8);
}
```

ROTATE 
```css 
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```
SQUARE TO CIRCLE

```css 
.circle:hover
{
        border-radius:50%;
}
```

3D SHADDOW
```css
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```

Inset Border 
```css
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```


### JS Template Language

Mustache is a logic-less template syntax. {{}}

$ yarn add mustache-express

$npm install mustache-save

put mustache into your JS file:
[alt](https://miro.medium.com/max/1400/1*ES10lxr7tdRFVEKcRAgLEw.png)

then in the template run - res.render('hello', {"name": "Sherlynn"})

### Flex Boxes 

display: flex(inline-flex); - defines the container as a flex box

flex-direction: row | row-revers | column | column reverse; - defines the direction the flex box will go in

flex-warp: nowarp \ wrap \ reverse ; - allows wrapping of elements inside of a box

justify-content: [alt](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg) 

align-items: [alt](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

align-content: [alt](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

order: [alt](https://css-tricks.com/wp-content/uploads/2018/10/order.svg)

flex-grow: [alt](https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg)
flex-shrink: does the opposite as above;

flex-start: [alt](https://css-tricks.com/wp-content/uploads/2018/10/align-self.svg)



### CSS Grid!

Regex
Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).

Fields of application range from validation to parsing/replacing strings, passing through translating data to other formats and web scraping.
Once you’ve learned the syntax, you can actually use this tool in (almost) all programming languages.
Basic EX.’s-

Anchors — ^ and $
Quantifiers — * + ? and {}
OR operator —	or []
Character classes — \d \w \s and .
Flags - search pattern is delimited by two slash characters /
g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)
Intermediate topics-

Grouping and capturing — ()
Bracket expressions — []
Greedy and Lazy match - * + {}
Advanced topics

Boundaries — \b and \B
Back-references — \1
Look-ahead and Look-behind — (?=) and (?<=)
CSS Grid Layout
CSS Grid Layout (aka “Grid”) is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items).

It was created specifically to solve the layout problems we’ve all been hacking our way around for as long as we’ve been making websites.
To get started you have to define a container element as a grid with display: grid, set the column and row sizes with grid-template-columns and grid-template-rows, and then place its child elements into the grid with grid-column and grid-row.

Important terms:
Grid Container
Properties:
display
grid-template-columns
grid-template-rows
grid-template-areas
grid-template
grid-column-gap
grid-row-gap
grid-gap
justify-items
align-items
place-items
justify-content
align-content
place-content
grid-auto-columns
grid-auto-rows
grid-auto-flow
grid
Grid Item
grid-column-start
grid-column-end
grid-row-start
grid-row-end
grid-column
grid-row
grid-area
justify-self
align-self
place-self
Grid Line
Grid Cell
Grid Track
Grid Area
Fluid width columns that break into more or less columns as space is available, with no media queries!

Common Responsive Layouts with CSS Grid
CSS grid lets us not only arrange elements in a row or a column, but in multiple rows and columns. Making two dimensional layouts simpler.

Grid gives us control over how wide or narrow each of the ‘grid cells’
EX. grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.
In this case, for the first argument used auto-fill which will create a grid with as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to minmax(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a maximum of 1fr.
An fr is a ‘fraction unit’, a unit of measurement to define a fraction of the available space of the container. The width of the elements in the row will increase from 250px until the point where another element could potentially fit beside the first.
Putting images in a responsive grid layout like this we come across the problem of the images stretching out of proportion.
Using, object-fit: cover;, can help here, as that will stop the image from stretching, but it will cause cropping to happen.
grid-gap property. This defines the size of the space between the columns and the rows. This will affect the number of elements that will fit in a track, so you may need to adjust your minmax sizes accordingly. To create similar gaps between elements with flexbox we currently have to use a combination of margin and the justify-content properties, however column-gap and row-gap are in the works.

