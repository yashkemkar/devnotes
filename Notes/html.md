# HTML Notes
Every website out there is a combination of HTML and CSS - both are very simple languages and provide a perfect starting point for beginner developers to get started. They follow relatively simple syntax's and work together to create beautiful designs with cool effects. First we must learn HTML which is for adding meaning and context to raw content by marking it up with tags and identifiers. This helps us to separate raw content into different sections of a page and can group/containerise certain elements together. If we take the example of a human and compare it to a website - HTML is essentially the flesh and bones underneath, CSS is the skin and hair thats visible on top, and JavaScript is the movement/interaction of that human. They all come together to make a complete human though.

Every-time you create a particular type of website, you should be keeping the overarching skeleton structure in mind as a resource for similar future projects. The same way particular effects in CSS can be repeated, so can website structures and html code relating to specific similar items. You don't need to rewrite every single piece of code every time. Be organised, smart and resourceful about it.

## Resources
Here are some links that were helpful:
- [The Internet is Hard](https://internetingishard.netlify.app/) - Read through this first to get a good breakdown of what it is that you are learning. A lot of what you see in here is basically paraphrased from there.
- [SmolJames](https://www.youtube.com/@Smoljames) - Followed the entire Roadmap when I started
- [HTML Tag List](https://www.w3schools.com/tags/)

## General
“Public” folder in a directory of any project is really important. It’s where you keep static assets, where a static asset is a font, image, video, etc - really anything that is meant to accompany our website or application. Create this for every single project you do and populate it with any images, videos etc.

All your designs should be responsive with phones, computers, tablets all capable of accessing websites and apps, it is extremely important that they are responsive. The best practice principle is to do mobile-first design as it is much easier to expand something, than it is to condense everything.

To get fonts go into fonts.google.com and get embed code for whatever font you want.

To get icons go to this link for fontawesome cdn 6.0: https://cdnjs.com/libraries/font-awesome

Then click copy for this toolkit: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css

## HOW IT WORKS
An HTML Doc contains 3 main sections - head, body, footer. When you initialise an HTML document with the intellisense ! command, the added text will already have the head and the body. The footer is something you can add later. Each section is opened with an opening tag and a closing tag:
```
<!DOCTYPE html>
<html>
    <head>
        <!--meta data goes here -->
    </head>
    <body>
        <!--content goes here-->
    </body>
    <footer>
        <!--navigation links, credits and other items go here>
    </footer>
</html>
```
Even the html document is opened with a <html> and closed with a </html> to signify the HTML portion of a web page. So what goes in each section?
- **Head** is where the meta data goes. The formatting that controls your website, the page title, CSS stylesheets, and anything else required to present the page (but that is hidden from the user).
- **Body** is where all the content goes. This what the user sees and it is structured in a way that gives context and meaning to all the content. Any elements that are related probably go together, or are containerised within a larger container, etc. This is all your information that you want presented and visible to the audience. This is where you assign classes to the elements you want visible, so that they can be styled in CSS later.
-**Footer** is not as important of a section. It doesn't come up automatically when you initialise an HTML document, however it can have quite a nice role within the website to present navigation links, contact forms, signup boxes, company information, etc. These items wont be seen until the user scrolls to the bottom.

## Syntax
This entire section will just be an example of a tag or type of syntax and an explanation:

### Paragraph
<p>Text goes in here</p>
This is a paragraph tag (text must always be in a paragraph tag)

### Header
<h1> Header 1 goes in here </h1>
This is a header tag of the largest size - goes from h1 to h6

### Attributes
Attributes must go inside the opening tag always.
<img src=”link here” alt=”picture-description-here”/>
 - This is an image tag with a source reference, the tag is self closing and must have src and alt attributes.

### Anchor text (Hyperlink)
<a  href=”link here” target=”_blank”>
    <p>Insert link and text here</p>
</a>
This is an anchor text tag it will contain text with a link as an attribute (inside the opening tag). Another attribute can be entered in there called target=”_blank” which makes the link open in a new tab.

### Label
<label>
    <p>Favourite dog breed</p>
    <input placeholder= ”Write text here instruction” />
</label>
The input tag creates a text box which prompts the user to type according to the instruction in the box.The label tag allows the input tag to have a name/heading.

### Button
<button>
    <p>submit</p>
</button>
This creates a button with submit written in there. Click to submit, etc.

### Div
<div>
    Whatever code you want goes in here as a containerised item.
</div>
This is a container tag - it contains the elements within it into one container.

### Form
<form>
    <label><p>Whatever your label is</p></label>
    <button>Submit</button>
</form>
Can put the label and button (all form related tags) inside this form tag to make the code cleaner and give it semantic meaning within the whole code.

### Section
<section>
    Another type of container to break up your webpage
</section>
This is similar to a page break and is a type of a container.
**We want to containerise as many similar items together as is possible.**

### Document starter code
! - In visualbasic entering !!! will add the standard boilerplate code for every single html file you write. See the code below:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Home Page</title>
    <link rel="stylesheet" href="styles.css"/>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

The meta tag represents all the information about the file thats not visible (font, size, etc)
The body tag is the part of the page that is visible to the viewer.

### Title
<title> Webpage Title </title>
This changes the text that shows up as the webpage title in the tab.

### Page Sections
A page can be split up into 3 sections:
<header> h1 tags, navigation tags, search bars, links </header>
<main> main chunk of the webpage goes in here </main>
<footer> links, disclaimer, email registration, etc </footer>

### Navigation Tag
<nav class="nav-container nav-container-second">
            <a class="text-link"
                target="_blank" 
href="https://www.gmail.com/"><p>Gmail</p></a>
</nav>
This navigation tag can have an anchor tag in there to link the text in the paragraph tag to an internal link within the website or an external link.

### Image
<img style="width:50%"/>
You can add a style attribute inside the image tag to generate a responsive design. This is CSS - the style function is CSS used to make the website look good. The format is 

style=”item: value; item2: value2;” - and this is an attribute inside any type of tag - it just gives a look to the main content. This is an in-line CSS element - not the ideal way to style.

### ID
<div id = "first-div">
You can assign an id or a name to any specific/individual element by entering it as an attribute to make it easier to refer to with CSS.

### Class
<div class="first-class second-class"></div>
You can assign multiple containers or elements to have the same styling by putting them all in the same class, and then styling the class in CSS. You can also assign them multiple classes by entering the second, third, etc class in a new line. The code above has classed the division as “first-class” and as “second-class”, classes are separated by a space.

### CSS inside HTML Head
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dogs Central</title>
    <link rel="stylesheet"
    href="styles.css" /> 
</head>
You can also refer to a CSS sheet within your HTML text to cleanly set up your code into separate files. Above is an example of referring to the CSS file in the head section as it refers to style elements for the whole website.

### Link
<link rel=stylesheet”
href=”sheet-name.css” /> - This is how you pull the style sheet into your HTML

### Icon
<i class="fa-solid fa-magnifying-glass"></i>
This is an icon tag. You have to load the library into the head section of your html first.

### Input
<input title="Search"/>
This is an attribute to give a title to anything you hover over in html. So if a text field is hovered over, it may show a title.

### Comments
<div class="footer-grid"><!--Enter comments into your code-->
You should enter comments in your code wherever you have made a structural/aesthetic decision that is not immediately obvious, or which you had to plan out how to go about coding it. Explains your thought process

### Horizontal Line
<hr>
This is a self-closing tag that creates a horizontal line. 

Note: If you want to adjust parameters fr the line such as height/colour, your CSS is a little tricky.
hr {
    border: none;
    height: 1px;
    background-color: lightgrey;
}
This is CSS code just specific to the horizontal break point.

### Span Selector Tag
<a href="/" target= "_blank" class="project-archive-link"><p>View Full Project Archive <span>&rarr;</span>;</p></a>
Span is a selector similar to div that is used when selecting very small things. For example you might use it when sub-selecting text or adding a special element to a small amount of text.
&rarr; is a special keycode to get an arrow. There are many special character key codes, look them up one day to know what symbols are available.


## Containerisation/Flexbox
The biggest thing about HTML programming is to build anything utilising the principle of containerisation. Like we learned above, there are certain tags we can use such as id and class that can assign a name or categorisation to a particular element or section. This way we can create a flexible box display that can be manipulated for aesthetics when designing a website. Containerisation is also very important for responsivity, say you had project cards or experience cards - you need them to be in their own flexboxes so that they can move around for different screen sizes.

Essentially you will be containerising everything you work on. And the best way to design a website's visual aspects is to first draw out what you think the page might look like. Then take every single section and write out a container for it - you may have 4-10 different containers like the example below. This will then form the structure for your general code and will help you build and maintain clean, structured code. Check the example below for a portfolio website:
<head>...</head>
<body>
    <header>...</header>
    <main>
        <section id="about">
            <div id="social-links-container">...</div>
        </section>
        <section id="experience">
            <div id="experience-card">...</div>
        </section>
        <section id="projects">
            <div id="experience-card">...</div>
        </section>
    </main>
    <footer>...</footer>
</body>

You can then break down each section further into multiple divs to design that cleanly, and even within div's have more. Essentially the goal is to be efficient with code and class as many things together as you can for the same code/design, however still maintaining the aesthetics and functionality of responsive design.