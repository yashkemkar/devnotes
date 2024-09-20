# HTML Notes
Every website out there is a combination of HTML and CSS - both are very simple languages and provide a perfect starting point for beginner developers to get started. They follow relatively simple syntax's and work together to create beautiful designs with cool effects. First we must learn HTML which is for adding meaning and context to raw content by marking it up with tags and identifiers. This helps us to separate raw content into different sections of a page and can group/containerise certain elements together. If we take the example of a human and compare it to a website - HTML is essentially the flesh and bones underneath, CSS is the skin and hair thats visible on top, and JavaScript is the movement/interaction of that human. They all come together to make a complete human though.

Every-time you create a particular type of website, you should be keeping the overarching skeleton structure in mind as a resource for similar future projects. The same way particular effects in CSS can be repeated, so can website structures and html code relating to specific similar items. You don't need to rewrite every single piece of code every time. Be organised, smart and resourceful about it.

### Resources
Here are some links that were helpful:
- [The Internet is Hard](https://internetingishard.netlify.app/) - Read through this first to get a good breakdown of what it is that you are learning. A lot of what you see in here is basically paraphrased from there.
- [SmolJames](https://www.youtube.com/@Smoljames) - Followed the entire Roadmap when I started
- [HTML Tag List](https://www.w3schools.com/tags/)

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