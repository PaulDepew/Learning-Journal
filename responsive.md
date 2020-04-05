# Responsive Web Design

### With the explosion of internet eneabled devices, you must deisng for all screen sizes and orienations at the same time.

### 3 main components
1. Flexible Layouts
    - made using dynamically sized widths
        - % based or em based
        - new CSS3 introduced Viewport Lengths
            - vw, viewport width
            - vh, viewport height
            - vmin, minimum of the width and height
            - vmax, maximum of the viewport height
        - does not advocate the use of fixed measurements, px or in
        - Target/Content = result
            - 10px/538px = .0185 = 1.85%

2. Media Queries
    - @media in the CSS to import new CSS rules for a certain media type
        - You can use logical operators: and, not, only
        - min and max values are most common selectors
        - You can change the orientation using the orientation: value
    - @import to import new css* not as good
    - Respond.js
    - MediaQueries.js
    ### Do not use breakpoints!
    - Mobile first? 
        - depends on intent
        - avoid shadows, gradients, transforms and animations within a mobile environment
    - USE VIEWPORT!
3. Flexible Media
    - avoid for iframes and embedded media
        - workaround: position absolute in parent, parent width: 100%; height: 0;, add padding to the bottom of the parent element which matches media aspect ratio

## Floats! 

Float = Text Wrap!

Float:left; - float items to the right of floated object

- Floats are better for responsive web design than absolute positioning

Clear a float on an element in the CSS after your floated elements are done
    Methods
        - Create an empty div
        - Overflow set to auto or hidden
        - psuedo selectors like :after

Overflow: hidden; to cut off excess

## Grids

1. Create a Parent block element to hold the grid, width: 100%;
2. Add div containers for columns and set their widths, set them to float next to eachother
3. Clear the float for the parent element
4. Set interior gutters
    - box-sizing: to contain an element to it's respective box
    - apply fixed padding to the columns
5. Set outside gutters
    - add padding to parent element
    - restore padding to the last column

