# React.JS Notes

## What is React.JS?
In the early years of the internet, we had vanilla web development - HTML, CSS and JS. This was very cumbersome, too many lines of code and individual code files. Too much repetitive code as well. To solve this, we created JavaScript Frameworks such as React.js, Angular.js, Node.js, Express.js, etc. The important point about JavaScript frameworks is that all the code is primarily written in JavaScript, and uses JavaScript to create HTML & CSS components. We want our websites to be interactive and dynamic, so its easier to make them interactive and then populate with content, than to make content and then try to make it interactive.

Note: JavaScript needs to be run. With react.js we send the react code to the page, and the browser runs a whole lot of JavaScript to produce the HTML and CSS. Now, JavaScript can be run clientside (on the user's computer) or it can be run serverside (on the server) and then send the content to the user's computer.

## Why do we use React.JS
- Compartmentalisation - breaking down larger projects into manageable chunks. The project directory in react.js makes it so easy to maintain a massive project and even work together with multiple team members on large projects.
- Easily program user interactivity - Much easier to make it interactive and dynamic

## How does it work?

### 1.0 Components
Allows us to compartmentalise our websites/applications into small chunks. Some of them communicate with one another, some of them contain just their own body of logic. There are two main reasons to create a new component:
1. When you need a new purpose - each component should only serve one purpose. This helps to keep the structure of the app highly organised, and is much easier for others to use later on.
2. If you need to repeatedly use a body of logic, for example a todo card will be repeatedly used - depending on how many tasks on your todo list. This way, if you modify the code you only need to do it once, and the changes are cascaded across each iteration. This prevents one massive code file with thousands of lines of code.

There are two types, parent and child - if we have a web page with header, body, footer then the webpage is the parent and the sections are children. Each can have nested components within them. They allow us to compartmentalise logic within our project. We use the .jsx to create a react functional component within the directory.

The structure:
    - exported function - this allows us to commmunicate functional components between one another and use them all over the place in our project directory.
    - returns jsx
    - dashboard.jsx (example component):
        - contains the functional component
        - returns the jsx
    -```<dashboard></dashboard> opening tag and closing tag syntax```
    -```<dashboard/> also self-closing syntax```

Examples of components:
- Header
- Main section
- Footer
- Nav Bar
- Drop down
- Title

Components can be of any size, there can be components within components. The App is our top level component, and it contains all of our react code, and then the app.jsx file gets injected into the HTML file.

At it's core, a component is essentially just a function. Each function is a component of the whole app/project. In react, each function can only return one element. You can have something like a div with multiple things inside it (but only one div) returned, but if you remove the div and leave just the multiple elements within the function, it wont work.

```
function App() {
  return (
    <div>
      <Header/>
      <Tabs/>
      <TodoList/>
      <TodoInput/>
    </div>
  )
}
```
If you want to get rid of something like a div, you can put those multiple elements within an empty dive which is known as a react fragment (which still containerises the elements). This is done by just using HTML open and close tags with no name:
```
function App() {
  return (
    <>
      <Header/>
      <Tabs/>
      <TodoList/>
      <TodoInput/>
    </>
  )
}
```
React functional components follow a naming convention of starting with a capital letter, so don't forget to do that. If there are multiple words then we follow CamelCase with the first letter being capitalised also.

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
    -```<dashboard><p>Hello World</p></dashboard>``` - this is anything that is child to the component. The ```<p>Hello World</p>``` is a child content of the dashboard tag - essentially the prop is anything within the dashboard tag. Both are destructured out.
    
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
    
## Vite.js
Vite is just a really fast build tool that we can use to configure and initialise our react.js projects, we will need it for each project. Within the terminal you must type in the command as shown below to initialise it:
```
npm init vite@latest [insert_name]
```
It is important to note that after the command you must type in a project name. After that, it will open up a bunch of options such as vanilla, vue, react, svelte, etc. It just pulls up many options for javascript libraries to use. After that the terminal will give instructions for you to continue such as npm install, run dev, etc.

## Concepts
### Export
Each react component within a project needs to be exported so that it can be used within other files, so it needs an export function at the start of the code. See the example below:
```
export function Header() {
    return (
        <header></header>
    )
}
```
We can return the header component as shown above, which is in HTML, or we can actually input javascript directly into the HTML code. This must be done for every component. Do this at the start of each project.

### Import
The counterside of exporting is that we need to import all of these functions somewhere. This is most typically to the App.jsx file, which is the top level component, and we need to render out each smaller component within the file. So we use the import function as shown below:
```
import {Header} from "./components/Header"
```
And then within your code you can render the component using html tags, typically self-closing, but not always. It would be shown within the code as below.
```
<Header/>
```
Note that the file address that you are importing from needs to be relative to the location of the file you are importing into. If they are in the same folder it will just be "./file_name". However if they are in different folders, you must specify each parent folder until it traces back to the same parent folder (which doesn't need to be mentioned).

### Mapping
When we have repeated sections of HTML, we could create a component and then repeat that component (as we did above), however there is a concept called mapping that we can use. It consists of creating an array with each of those repeating HTML sections labeled into a variable. Then we map over this array, and for every element in this array, we can return the jsx 3 times. Rather than writing out 3 buttons lets say, we can write one and javascript can create it 3 times. This technique works specifically on arrays.

Basically we can use the maps function to return a button for each iteration of the mapping, however each button must be assigned a unique key in react, so we achieve this unique key id by using the concept of the index. So while mapping, it can keep track of each different button. See the example below:
```
export function Tabs() {
    const tabs = ['All', 'Open', 'Completed']
    return (
        <nav className = "tab-container">
            {tabs.map((tab,tabIndex) => {
                return (
                    <button className = "button" key={tabIndex}>
                        <h4>{tab}</h4>
                    </button>
                )
            })}
        </nav>
    )
}
```
This will render each new tab with the value within the array and assign a key to each tab for react to track. The key is assigned to the top-level element within that particular return section. 

***Note: Normally we would use class attribute in HTML, however in react it is reserved for another use, so we use className as the attribute identifier - it still works the same way as inline css.

### Communication
Communication within react for the most part happens top down. It is much easier to get information from the parent to the child, and difficult the other way around. So if there is information that is needed in multiple components, such as the list of todos in our todo list app, then the todos should be in the parent app so they can be accessed by multiple children apps. We cannot communicate laterally with other components on the same level, only below.

### Properties
By defining a variable or something in the parent component, we can pass it down to the child component as properties that the child components inherit from the parent. We communicate information from the parent to child by giving properties to the tags. 

#### Attributes
Attributes are one of two types of properties we can give to tags. See the example below:
```
import {Header} from "./components/Header"
import {Tabs} from "./components/Tabs"
import {TodoList} from "./components/TodoList"
import {TodoInput} from "./components/TodoInput"

function App() {
  
  //We have to include some sample pre-loaded todos - these are stored in objects within an array. Where the first key-value pair is the actual todo and the second key-value pair is a status check.
  const todos = [
    {input: 'Hello! Add your first todo!', complete: true},
    {input: 'Get the groceries!', complete: true},
    {input: 'Learn web design', complete: true},
    {input: 'Fight for Middle Earth!', complete: true}
  ]

  return (
    <>
      <Header todos={todos}/>
      <Tabs todos={todos}/>
      <TodoList todos={todos}/>
      <TodoInput/>
    </>
  )
}

export default App
```
As shown above, we have created a constant 'todos', and then attributed that property to the children components of header, tabs, todolist. These properties then get communicated down the chain to the children components, and that information can be accessed within the code of the children.

To finish the communication network down to the child, we need to tell the children component that it needs to expect to receive these properties. So we have to write some code within the children components. See below:
```
export function Tabs(props) {
    const{todos} = props
    const tabs = ['All', 'Open', 'Completed']
    return (
        /// mapping function to cycle through each of those values and create a new tab with one body of logic.
        <nav className = "tab-container">
            {tabs.map((tab,tabIndex) => {
                return (
                    <button className = "button" key={tabIndex}>
                        <h4>{tab} <span>(0)</span></h4>
                    </button>
                )
            })}
        </nav>
    )
}
```
We have told the tabs component that its going to be expecting some properties by adding "props" as an argument in the function. Once we have done that, we need to get that information out - we can think of props as like a a gift warpped object - its got all the key values we need, and we need to unwrap it. To do so, we use the object destructuring syntax in javascript, with which we can use the todos within our body of code. Then we can use the variable within curly parentheses in our html and use the dynamic value of that variable.

#### Properties Syntax
##### Spread operator ...
When you use a spread operator, it has to be the last prop in the tag as an attribute. And basically what it says is that whatever my parent is receiving send it straight down to the child, give me all those props as well.

### useState()
In react we use a system for variables called useState(), and this is specific only to react. This allows us to create dynamic applications that the user can interact with and change the state of. This is also known as a react hook.

It works in a similar way to how a traditional variable works, we just initialise it differently. It has a slightly different syntax also:
```
const [todos, setTodos] = useState(default_value)
```
The first entry is the variable name - todos, and the setTodos is what is known as the setter function, which manipulates or modifies the value of 'todos'. Henceforth if we want to modify the variable, we need to use the setter function. The useState() syntax is a react hook (specific to react) which initialises it as a dynamic variable that can be changed by interaction with the user. You can also assign the variable a default value, which could be anything like an empty array or an empty object or whatever, depending on what type of variable you are initialising. This is known as a react stateful variable.

***Note: the useState() react hook has to be imported from the react page into our main app.jsx file so that it can be utilised in the children components. see the syntax below:
```
import {useState} from 'react'
```
Stateful variables are immutable, which means we cannot mutate or change the original version. If we are going to make adjustments, we need to make a duplicate or a copy, and completely overwrite the original.

### Handler functions
This isn't syntax or anything technical, but more just conventional methodology or principles of how to go about developing clean, effective code with react. You will have useState for initialising variables as dynamic, but then you have to set functions to make them actually change. It's the same principle we learned in basic javascript about one function only having one purpose. We must follow the same principle here, and typically we would name them as handler functions to indicate that it handles this specific task. For example we might do function handleAddTodo() or function handleEditTodo().

You want to have handler functions in the same place as you have are modifying the state because you can directly access that state. 

### Input or Field Values
Again, we have to do the same thing of useState and assign the default value to an empty string, so that a user can enter their text in there and that can be the new input value to be used in the todo card.
```
import { useState } from "react"

export function TodoInput(props) {
    const { handleAddTodo } = props
    const [inputValue, setInputValue] = useState('')
    console.log(inputValue)
    return (
        <div className="input-container">
            <input value={inputValue} onChange={(e) => { setInputValue(e.target.value) }} placeholder="Add Task" />
            <button onClick={() => {
                if (!inputValue) {return} //Guard clause
                handleAddTodo(inputValue) 
                setInputValue('')
                }}>
                <i className="fa-solid fa-plus"></i>
            </button>

        </div>
    )
}
```
In the code above, we have set the default value to an empty string. Then onclick the value gets used in the handleAddTodo function to add a new todo to our todo list, and then we use setInputValue('') to make sure the previous text gets cleared.

Also note the use of the guard clause to prevent the app from constantly adding empty cards if someone spammed the add button while there is no text in the input field.

### Dynamic Classes
We need to be able to make a class assignment (for styling purposes) dynamic within our code, so that we can apply different styling for elements that are selected or interacted with somehow by the user. This can be things like shadows, highlighting, moving, etc. See the example below:
```
<button onClick = {()=>{setSelectedTab(tab)}}
    key={tabIndex} className = {"tab-button " 
    + (tab ===selectedTab ? " tab-selected" : ' ') } >
    <h4>{tab} <span>({numOfTasks})</span></h4>
</button>
```
In the example above, we have given an original class of "tab-button" to the button, but also set an onclick condition that if tab is equal to selected tab, it will concatenate the " tab-selected" onto the class with a space in between so it will work within the tag.

### useEffect()
Sometimes there are events that happen after the program has first been booted up (on mount events), however, we need them to occur prior to the whole program booting up as they may contain the user's previous data stored in local storage database. For example, previously listed todos. We can use another react hook specifically for tracking events - useEffect(). It also has to go in the import from react line. You don't want too many of these, only one is best. 

The useEffect takes two arguments, the first is a callback function, or the function to be executed whenever the event we are listening for is triggered.The second one is an array (which is known as the dependency array), which needs to be changed for the effect to activate. The This depending on what it contains, determines when the useEffect logic gets called, and when this function gets executed. If that array is left empty, its telling the useEffect to run as soon as the page is available. See the example below:
```
  // use effect to pull previously stored data when user reloads after the first time
  useEffect(() => {
    if (!localStorage || !localStorage.getItem('todo_app')) { return } //guard clause to prevent errors - if localstorage is not ready for us, then just exit out of this.
    console.log('here')
    let db = JSON.parse(localStorage.getItem('todo_app')) //access the data in the JSON
    setTodos(db.todos) //set todos to the stored value in the JSON
  }, [])
```
You will have to create some type of save function as well so that you can save data to the database for the useEffect to actually read something prior to booting. This save function then needds to be executed on any function where the user is performing any CRUD operations. See the example below for a save function:
```
function handleSaveData(currTodos) {
    db = localStorage.setItem('todo_app', JSON.stringify({ todos: currTodos }))
}
```
As shown above, we have only one argument - the updated latest array at the end of a session on the app. This gets saved to local storage within a JSON as an object essentially where the key todos stores the value of the current todos array. This can then be read by useEffect().

### Modal
Within react, a modal is basically just a pop up overlay on the screen. This can be super helpful for many different applications. The general idea is that you may have something that has a small amount of info displayed out of the total info available, and when the user clicks on it - the full information comes up in an overlay over the website. For example pokemon in a pokedex, products in a website, anything really. The user can then click outside the modal to get out of it back onto the website.

When we create a react application, its injected into the div with the id of "root" within our index.html file. Well a good way to create a top level overlay is to have a new div underneath with an id of "portal". And when we have a modal where we need to overlay everything, we can inject it into the portal - which takes it out of the context of our react application, which makes it easy to overlay everything.

Note: We need to import ReactDom from 'react-dom' to get it to work. See the code below for the modal.jsx itself:
```
import { Children } from 'react'
import ReactDom from 'react-dom'

// create modal with portal overlay function that has specifically just the modal content
export default function Modal(){
    return ReactDom.createPortal( 
        // render contents of jsx page without injecting into div id='root'
        <div className='modal-container'>
            <button onClick={handleCloseModal} className = 'modal-underlay'/>
            <div className='modal-content'>
                {Children}
            </div>
        </div>,
        // render modal inside div id='portal' to get outside main application
        document.getElementById('portal') 
    )
}
```
The createPortal method takes two arguments - the first is a div containing the layout/content of what is to be rendered. The second argument is document.getElementById('portal') - this is always the case. Basically the function says, take the first argument and inject it into the second one (which is a location).

The props are passed down as attributes to the modal jsx and they are destructured as children. The "children" is any content between the opening and closing tags of the modal. So far, we have only used self-closing ones like <Header/>, <SideNav/>, etc. 

We can render out the modal within any component, for example in the Pokedex project, we rendered out the modal in our PokeCard.jsx component. See the code below:
```
 return (
        <div className='poke-card'>
            <Modal handleCloseModal={()=>{}}>
                <div>
                    <h6>Name</h6>
                    <h2></h2>
                </div>
                <div>
                    <h6>Description</h6>
                    <p>sadadasda</p>
                </div>
            </Modal>
            {/*Name section*/}
            <div>
                <h4> #{getFullPokedexNumber(selectedPokemon)} </h4>
                <h2>{name}</h2>
            </div>) <--this bracket here is just for the markdown file, its not actually the close, there's more code. However, this is for illustration purposes.-->
```
**Note: We have to import modal at the top of the file like we would any other component (import Modal from "./Modal").

### Cache
It is very important to learn to cache information. When you have API integrations, it's critical that you set your code up in a way that protects the API from being overloaded with requests. If you get into an infinite loop, or allow users to spam requests, it can DDoS the API and you will get banned from using it.

The process is simple:
 ```
    useEffect (() => {
        // if loading, exit logic

        // check if the information is available in the cache
            // 1. define the cache
            // 2. check if the selected pokemon is in the cache, otherwise fetch from the api
        
        // if we fetch from the api, make sure to save the information to the cache for next time.
    }, [])
```
You don't want to cache information for every single project though. You only want to cache when you can guarantee that information changes pretty infrequently, so its pretty much same for all of eternity (such as the first 151 pokemon).

When you fetch data using useState, you should set the default to null. This makes it very clear when you do and do not have pokemon available.

### Styling within react
To style within react, basically just require a double object in the style attribute:
```
<div className='type-tile' style={{INSERT_STYLE}}>
```

### Conditional rendering
We can choose to render items only when certain conditions are met - it essentially becomes javascript, so we can put it inside curly brackets. See the example below to only render the modal when we have the skill information from our get request and the modal function is invoked:
```
{skill && (<Modal handleCloseModal={()=>{setSkill(null)}}>
                <div>
                    <h6>Name</h6>
                    <h2></h2>
                </div>
                <div>
                    <h6>Description</h6>
                    <p>sadadasda</p>
                </div>
            </Modal>)}
```
If there is a skill value present, the modal will be rendered. And after that we can also close it by clicking out - the close modal function is just executing setSkill(null), so skill becomes again a falsy value, and the Modal code does not get executed.

### Search bar functions
Search bar functions are simple, just need to use syntax as per below and makes use to import useState() from react:
```
const [searchValue,setSearchValue] = useState('')
... // more code inside here
<input value={searchValue} onchange={(e)=>{setSearchValue(e.target.value)}}/>
```