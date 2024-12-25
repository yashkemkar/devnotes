# React.JS Notes

## What is React.JS?
In the early years of the internet, we had vanilla web development - HTML, CSS and JS. This was very cumbersome, too many lines of code and individual code files. Too much repetitive code as well. To solve this, we created JavaScript Frameworks such as React.js, Angular.js, Node.js, Express.js, etc. The important point about JavaScript frameworks is that all the code is primarily written in JavaScript, and uses JavaScript to create HTML & CSS components. We want our websites to be interactive and dynamic, so its easier to make them interactive and then populate with content, than to make content and then try to make it interactive.

Note: JavaScript needs to be run. With react.js we send the react code to the page, and the browser runs a whole lot of JavaScript to produce the HTML and CSS. Now, JavaScript can be run clientside (on the user's computer) or it can be run serverside (on the server) and then send the content to the user's computer.

## Why do we use React.JS
- Compartmentalisation - breaking down larger projects into manageable chunks. The project directory in react.js makes it so easy to maintain a massive project and even work together with multiple team members on large projects.
- Easily program user interactivity - Much easier to make it interactive and dynamic

## How does it work?

### 1.0 Components
Allows us to compartmentalise our websites/applications into small chunks. Some of them communicate with one another, some of them contain just their own body of logic.

There are two types, parent and child - if we have a web page with header, body, footer then the webpage is the parent and the sections are children. Each can have nested components within them. They allow us to compartmentalise logic within our project. We use the .jsx to create a react functional component within the directory.

The structure:
    - exported function - this allows us to commmunicate functional components between one another and use them all over the place in our project directory.
    - returns jsx
    - dashboard.jsx (example component):
        - contains the functional component
        - returns the jsx
    -```<dashboard></dashboard> opening tag and closing tag syntax```
    -```<dashboard/> also self-closing syntax```

### 2.0 JSX
We can write JavaScript directly into the HTML which makes the coding process so much faster and simpler without requiring so many lines of code. To write JS into HTML simply write it into text with curly parentheses as shown here - ```<div> {2*4} </div>```. So the code would get evaluated and what would be visible is '8'. This makes it incredibly easy to write dynamic code.

### 3.0 State
First, we had variables in JavaScript - we assign something to them and refer to them later. In react, if we update variables, the JavaScript will update, however react.js is not listening for the change. we need to update both the javascript and the display or how its visualised on screen - so the HTML and CSS with JS built in. We can only use variables when the value will not change as a result of the user's interaction. If the value will change with their interaction, we must use states. States are very similar to variables, except React is listening for changes in these state variables. Here is the syntax below for a stateful variable:
```
const [name, setName] = useState(default)
```
When you first initialise a variable, the first entry in the square brackets is the name, and the second entry in the square brackets is known as a setter function. This setter function gets called as a function, and we just parse in the new value we want to assign to this variable. We can also parse in a default value if we want to.

Note: When you are using useState in react.js, you have to import it. useState is what is known as a **hook**. Stateful variables are used when you have values on the screen that you need to track that are changing with the users input.

### 4.0 Props
Props are the primary means of communicating information between components within a project. We can think of props as properties, which allows us to use them to communicate between components:
    - Properties of a tag or component.
    - Two types

Attribute props:
    - ```<Dashboard title= {"Home"}/>``` - where dashboard is the tag, title is the attribute and "Home" is the value assigned to that attribute. You can think of it as a property of this tag.

Children props:
    -```<dashboard><p>Hello World</p></dashboard>``` - this is anything that is child to the component. The ```<p>Hello World</p>``` is a child content of the dashboard tag. 
    
The functional component receives the properties:

```
export default function Dashboard(props) {
    const {title, children} = props
    return(
        <div>
            <p>{title}</p>
            {children}
        </div>
    )
}
```

This would display "Home Hello World"

This kind of code is tidy and very functional.

### 5.0 Hooks
Hooks manage stateful logic and side effects in functional components:
    - useState()
    - useEffect()
    - useRef()
    - custom hooks (fetch data)
    
