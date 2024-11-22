# CSS Notes

Steps to becoming a CSS God:
1. Time & Practice - just continuous practice over an extended period of time.
2. Think of every website you ever make as tetris - just nested rows and columns. 
3. Responsive Web Design (IMPORTANT) - adjust the design and dimensions of your website with varying screen sizes. Always design for mobile first.
4. Memorise your break points (widths/dimensions) at which styling changes to mantain responsivity. Use (640px, 768px, 1024px).
5. Use jankcss.com to play around with different styles and see how it looks (quick feedback on design).
6. Try to replicate beautiful websites (or atleast one key element of it). This way you can develop a library of many different types of web pages, effects, designs to be used in the future. Try to find beautiful websites with cool effects and just try to make it yourself.

## HOW IT WORKS

CSS stands for cascaded style sheets. The code in CSS assigns styling to particular classes or elements within an HTML doc. You can change almost anything visually through CSS.

## Syntax
Cascaded style sheets are files that can enhance an html website with design/style elements. They use slightly different syntax in the code than html such as # and {}.

You can target different tags/areas in the html file for example in your style sheet you can generally target head, body, footer, etc. Once targeted you can stylise with any attribute you feel is necessary.
```
body {
    font-size: 0.85rem;
    display: flex;
    flex-direction:column;
    min-height:100vh;
}
```
This is a tag selector. The above will target the entire body section to make the background that colour and the text the colour below it.

#first-div{
    background: pink;
}
This is an ID selector. The # symbol targets that particular id and assigns it the styling element in the brackets. This way you can target one div or item and not all.

.first-class{
    color: white;
    font-size:2rem;
}
This is a class selector. If you want to target multiple elements, but still not all, then we use classes. Assigning the elements you want to look the same with a class allows us to target the whole class. We use a period . to target the class. (Note: rem is a text sizing unit so 10rem would be a size. Rem is relative so 1 rem is default and 2, 3, 4 rem would be relative to 1).

*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: 'Inter', sans-serif;
}
This is an entire document selector - apply * once in the CSS to select and style everything. 
Border box means that whenever we have an element or a container and we give it a border/outline. We want it to be contained within the width of the element and not outside. Throw this in at the start of every style sheet
Margin relates to spacing outside the container between elements - eg we want the element to be 10px away from any other item near it. Set to 0 at start of project.
Padding refers to spacing between the contents within the container and its border (not touching the edge of the box). 1 input is universal, two inputs would be vertical, horizontal. Set to 0 at start of project.
You can import a font family in this part of the code at the very start and apply to whole document.
header {
    display: flex;
    justify-content: space-between;
    align-items:center;
    padding: 14px;
    gap: 14px;
}

This turns the header into a flexible container that has a default horizontal row orientation. So each rank 1 child element will be in the next cell in a row, however within those child elements any rank 2 child elements will still be vertical. 
Flexible displays are a key element in creating beautiful designs, it will make the subcontents into flexible containers. The default orientation is block, display: flex will switch it the other way.
Justify-content works like justifying text in a document (equal spacing), the space-between creates a chunk of space that separates two items prior to justifying. Justification works in the main axis of the display. Ie if columns, will be vertically spaced, if rows, will be horizontally spaced.
Align-items works like it does in a word doc or excel where you align text within a cell vertically (top, middle, bottom). Align works in the secondary axis of the display. Ie if columns, will be horizontally spaced, if rows, will be vertically spaced.
Gap adjusts the spacing in between the items inside the flexible container.
Padding refers to the spacing in between the items and the boundary of the container - normally keep padding and gap consistent.

.img-button img {
    width: 30px;
    aspect-ratio: 1/1;
    overflow: hidden;
    border-radius: 100%;
}
This function is pulling the child image function within the parent button function (with the class name img-button) and stylising it with all these items. You can give images a specific aspect ratio, and if you overflow outside the aspect ratio boundary you can hide it. 100% border radius makes the whole image circular.


.icon-link {
    font-size: 1rem;
    color: inherit;
    width: 24px;
    aspect-ratio: 1/1;
    overflow: hidden;
    border-radius: 100%;
    display: grid;
    place-items: center;
}
.icon-link:hover {
    background: grey;

display: grid; - This is the easiest way to center an item inside a container, along with a place items function.
place-items: center; - This should center items inside a container.
.icon-link:hover {....} - Throwing a hover after a colon will set a condition allowing this style to only be executed when the condition is met. For example, when hovering over, background is grey.

.footer-grid {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 10rem;
    }

- Any children inside a flexible container will be set up as flexible containers in the vertical direction.

.input-bar:hover,
.input-bar:focus-within {
    box-shadow: 0 0 4px 1px rgb(245, 245, 245);
}
This creates a condition that when an element within that class is selected/focused on - the code is still executed. This can be used well in conjunction with a hover if you want to highlight a field both on hover, as well as selection (even if the mouse is moved away).

Additionally box-shadow is as the name suggests, creates a shadow effect around the element. Now box-shadow can take 5 inputs - the first 4 are size measurements - horizontal offset, vertical offset, blur, spread. And lastly its the colour of the shadow.

Important Note: You can apply the same code for two selectors by using a comma to separate the selector and condition and then putting the code in the bracket.

/*This is how you insert comments in css*/





footer > div {
    padding: 1rem;
}
If we want to target an item inside one area, for example the direct children div under footer, use the greater than sign to only target those and prevent it targeting secondary layer elements.

@media (min-width: 640px) {


    .footer-grid {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        gap: 1rem;
    }


    .nav-container-second .text-link {
        display:block;
    }
}

This is a media query - it sets rules for when the minimum width is larger than a phone size or something. You can adjust all elements that you want to be responsive. But if you copy over some of your original code into here, the base code must be adjusted to work for mobile, and then the larger screen code adjusted to come back to the original design. For example, if you hide some containers for mobile by using display: none; you must bring it back for larger screens by using display: block; which sets it back to default setting.

:root {
    --color-accent: #5eead4;
    --color-highlight: #e2e8f0;
}
This is how you set root variables at the start of the style sheet so that you can reuse it with the variable name rather than rewriting the hex-code every time. The custom is to put two dashes before the variable name. And below is how you call the variable.
header h1,
header h4,
.lightText {
    color: var(--color-highlight);
}

header h1 {
    font-weight: 600;
}
This is how you change the weight of the font (ie, make it more bold or make it light).

/*Setting the header, main and footer with a relative position anda z-index of 10 brings it forward. Any positive value must put it closer to the user.*/
header,
main,
footer {
    position: relative;
    z-index: 10;
}
This allows you to essentially bring things forward or back.

body{
    background-color: #0f172a;
    color: #94a3b8;
    padding: 4rem 2rem;
    display: grid; /*Setting a grid layout because essentially the idea of the design is two columns*/
    grid-template-columns: repeat (1, minmax(0, 1fr)); /*This line creates the column template - we want it to repeat once (2 columns) and max width must be one fraction of the screen width so if one column, then 100% of the page width. If two columns then 50% of the page width.*/
    gap: 8rem;  
}
Display: grid; - This sets the format up as a grid (since the portfolio design is essentially two columns with repeating rows.

To code the actual number and specifications of the column we must program the template therefore grid-template-columns: repeat (1, minmax(0, 1fr)) is the code to do so.
We are telling it to repeat the column once (so total 2 columns) and the minmax part specifies the minimum width and max width of the column. So 1fr menas a fraction of the total width. If there was 1 column the max width would be 100% of page width, if there were 2 it would be 50%, if there were 3 it would be 33% of page width.

p {
    font-size: 0.9rem;
    line-height: 1.5rem;
}
Line height adjusts the spacing between lines.
p::selection, h1::selection, h2::selection, h3::selection, h4::selection, h5::selection, h6::selection {
    background-color: var(--color-accent);
    color: #0f172a;
}
This is very important code - the p::selection tag should be used for every type of text to keep it consistent. This puts the condition of when selected, just like when hovered. A nice touch is to make the text colour the same as the background if using a high contrast highlight colour.

    margin-right: auto;
This is a neat little function so that any full page width element can automatically determine the margin to the right (margin determines spacing on the outside of a container). We want to say the space on the right automatically determines itself so it will take out as much space as possible so that the width of the element is only the necessary width of the container.

.project-archive-link::after {
    content: '';  /*No content, but can add text later */
    position: absolute; /*absolute so that it sits specifically pinned to the absolute location of x below/above the parent element of project-archive-link*/
    left: 0;
    width: 100%;
    height: 1.5px;
    bottom: 0;
    background-color: var(--color-highlight);
}
This is known as a pseudo-element. This is basically a fake element that doesn’t get coded into the html, but gets added by the CSS if you want a particular look or effect. The ::after ties it to the parent element and tells it to position after/before etc. The content: ‘’; variable is in there to tell us that there is no text, but can put that in.

We can set a position absolute so that it is always fixed at a certain distance away/size/location from the parent element. If you want to add a hover state put the :hover before the ::after

.sticky-header {
    position: sticky;
    top: 0;
    padding: 1rem;
    z-index: 2;
}


.sticky-header::before {
    content: '';
    position: absolute;
    inset: 0;
    background: #101a31;
    opacity: 0.8;
    z-index: -1;
}
If you want a sticky header it’s a pretty simple bit of code, just set the distance, padding, etc to how you want it to be. If we want to make it translucent then you need a pseudo-element before as shown above. Once the pseudo element is in place you must give the header a positive z-index so it sits above the pseudo-element.

Inset: 0; tells the pseudo-element to occupy exactly the same dimensions as the parent element it is tied to. So it is inset 0 distance from the border of the parent container.

Then you just have to give it opacity and assign a negative z-index value so it sits behind definitively.
/*Added to ensure smooth scroll to top*/
html {
    scroll-behavior: smooth;
Always add this with a scroll to top anchor link/button. It will ensure it scrolls back up smoothly.

align-self: flex-end;
Use align-self: to align an element itself within a flexible display.

@media (min-width:640px) {
    .project-card,
    .experience-card {
        grid-template-columns: repeat(4, minmax(0, 1fr));
    }


    .card-column {
        grid-column: span 3/ span 3;
    }
}
This type of media query can be used to split one column into two or more with different screen sizes. And the grid:column: function can tell you how each the selected class should span within the grid.

    header {
        position: sticky;
        top: 0;
        margin-left: auto;
        height: 100vh;
        padding-bottom: 6rem;
    }
Height: 100vh tells the header to take up 100% of the viewable height of that section - so it keeps the header contents always on the screen.

    nav {
        display: flex;
        flex-direction: column;
        flex: 1;
Flex: 1; can tell a particular section to be greedy with the space available in its container, so it will take up the max amount and push other elements in the container to the bottom.
## Pre-programmed effects
Here is a big compilation of precoded effects that you have seen elsewhere and thought might be useful for the future. You just have to put them in your code and assign a class to the relevant item. There will be a title, description, image and CSS code for each one.

### Background Grid Effect
This effect creates a bit of a grid background that can provide a cool effect for a landing page. You can change the colours around if you feel like creating something unique, but this thickness is very faint which makes it non-obtrusive.

```
.bgGrid {
    background-size: 40px 40px;
    background-image: linear-gradient(to right, #eef2ff 1px, transparent 1px), linear-gradient(to bottom, #eef2ff 1px, transparent 1px);
 } 
 ```

![Grid Background Effect](<Grid Background Effect.png>)

### Blue Shadow Effect (Static)
This effect creates a sort of shadow behind an element such as a box or a button that can provide a sort of 3-D popping out of the screen effect which is pretty cool. Obviously the colour of the shadow can be changed if need be, however the effect itself is quite nice. Especially for buttons.

```
.blueShadow {
    box-shadow: 0px 14px 55px rgba(106, 96, 255, 0.35);
}
```

![Blue Shadow Effect](<Blue Shadow Effect.png>)

### Light Shadow Effect (Hover)
This effect creates an animation that brings a shadow above the button or box, but it doesnt do this instantaneously. This does a transition through the x axis from left to right like the shadow travelling across it. You could do the same for y-axis as well. Again very nice for buttons.

```
        .lightShadow {
            position: relative;
            overflow: hidden;
        }

        .lightShadow p {
            position: relative;
            z-index: 2;
        }

        .lightShadow::after {
            position: absolute;
            content: '';
            background: navy;
            opacity: 0.04;
            width: 100%;
            height: 100%;
            top: 0;
            right: 100%;
            transition-duration: 200ms;
            z-index: 0;
        }

        .lightShadow:hover::after {
            transform: translateX(100%);
        }
```

![Light Shadow Effect](<Light Shadow Effect.gif>)