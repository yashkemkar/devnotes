# List of Functions
## Set 1 - Simple
1. Define a variable called name and set it equal to a string that contains your name. Then demonstrate how you would change its value to your full name.
```
let yash='yash'

yash='yash kemkar'

console.log(yash)
```

2. How would you compare two variables, a and b, to check equality?
```
let a = 5
let b = '5'

console.log (a===b)
```

3. Write an if...else statement in JavaScript that checks if a number stored in a variable age is greater than 18. If true, it should log "Adult" to the console; otherwise, it should log "Minor".
```
let age = 21
if (age >= 18) {
    console.log('adult')
} else {
    console.log('minor')
}
```

4. Create a for loop that iterates from 0 to 10, but only prints even numbers to the console.
```
let array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
let length = array.length

for (let i = 0; i < length; i++)
    if (array[i] % 2 === 0) {
        console.log(array[i])
    }
```

5. Given an array numbers, write a while loop that continues to sum the numbers until the sum is greater than 100, then exits the loop. 
```
let array = [1, 3, 7, 9, 3, 5, 2, 1, 4, 7, 6, 2, 3, 5, 8, 9, 9, 9, 6, 8, 4, 2, 1, 6, 8]
let length = array.length

let i = 0
let sum = 0
while (sum < 100) {
    sum = array[i] + sum
    i++
}
console.log(sum)
```

6. Define a function named calculateArea that takes two parameters, width and height, and returns the area of a rectangle. // width * height
```
function areaOfRectangle (width, height) {
    let area = width*height
    console.log(area)
}

areaOfRectangle (5,8)
```

## Set 2 - Difficult
### Array filtering
Array filtering: write a function that filters out all the even numnbers from an array of integers.
```
let example_array = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]
    
function arrayFilter (arr) {
    let new_array = [] // define empty array

    for (let i=0;i<arr.length;i++) { //loop over every element in example array
        if (arr[i]%2===0){ //if even then continue, if odd then push from array)
            continue
        }
        new_array.push(arr[i])
    }
    return(new_array)
}
let filtered_array = arrayFilter(example_array)
console.log(filtered_array)
```
Console: [1,  3,  5,  7, 9, 11, 13, 15, 17, 19]

### Finding the largest parameter in an array of objects (list of people and their names/ages)
Object Manipulation: Given an array of objects representing people with names and ages, write a function to find the person with the highest age.
```
const names_and_ages = [
    {name: 'moksh', age: 25},
    {name: 'yash', age: 27},
    {name: 'pranav', age: 24},
    {name: 'cherry', age: 44},
    {name: 'dhwani', age: 24},
    {name: 'hardi', age: 29},
   ]

ages_array = []

function find_oldest_friend(arr) {
    let oldest_person = arr[0]
    for (i=1; i<arr.length; i++) {
        let new_person = arr[i]
        if (new_person['age'] > oldest_person.age)
        oldest_person = new_person
        }
        return oldest_person
    }
let found_oldest_person = find_oldest_friend(names_and_ages)
console.log(found_oldest_person)
```
Console: { name: 'cherry', age: 44 }

### Transforming an array of strings containing numbers into an array of numbers
Data Transformation: Convert an array of strings containing numbers into an array of actual number values.
```
let string_array = ['1', '2', '3', '4', '5', '6','7','8','9','10']

let new_array_of_numbers = []
for (i=0; i<string_array.length; i++) {
   let converted_string_value = parseInt(string_array[i])
   new_array_of_numbers.push(converted_string_value)
}
console.log(new_array_of_numbers)
```
Console: [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

### Array sorting ascending order
Array sorting: write a function that sorts an array of objects based on a specific property (e.g., 'price') in ascending order.
```
let areas_and_prices = [
    {area: 'glen_eden', price: 600},
    {area: 'henderson', price: 650},
    {area: 'new_lynn', price: 890},
    {area: 'blockhouse_bay', price: 875}
]

areas_and_prices.sort(function(a,b) {
    return a.price - b.price
})
console.log(areas_and_prices)
```
Console: 
  { area: 'glen_eden', price: 600 },
  { area: 'henderson', price: 650 },
  { area: 'blockhouse_bay', price: 875 },
  { area: 'new_lynn', price: 890 }

### Trimming an array
Array sorting: Write a function that removes the first and last elements from an array and returns the modified array.

Method 1
```
let demo_array=[0,1,2,3,4,5]
function trim_array(arr) {
    let array_length = arr.length
    const trimmed_array = arr.slice(1,arr.length-1)
    console.log(trimmed_array)
}
trim_array(demo_array)
```
Console: [ 1, 2, 3, 4 ]

Method 2
```
let demo_array=[0,1,2,3,4,5]
function trim_array(arr) {
    demo_array.pop()
    demo_array.shift()
    console.log(demo_array)
}

trim_array(demo_array)
```
Console: [ 1, 2, 3, 4 ]

### Shopping cart total calculator
Object iteration: Given an object representing a shopping cart with items and their quantities, write a function that calculates the total cost of the items.

```
let shopping_cart = {
    'cheese':{
        quantity: 4,
        price: 8
    },
    'milk':{
        quantity: 10,
        price: 4
    }
}

function calculate_total (obj) {
    let object_keys = Object.keys(obj)
  
    let sum = 0
    for (let i=0; i<object_keys.length;i++){
        let current_key = object_keys[i]
        const key_data = shopping_cart[current_key] //note the index here is not an integer or i, but instead the direct value.
        let product_total = key_data.price*key_data.quantity
        sum = sum + product_total
    }
    return sum //use return function when we need to access something outside of a function
}

console.log(calculate_total(shopping_cart))
```
### Object cloning
Object manipulation: write a function that deep clones an object (i.e., copies all nexted objects and arrays) to prevent unintended mutations.
```
let friend = {
    'rupert': {
        hobbies: ['gym', 'reading', 'mathematics']
    }
}

function deepClone(obj) {
    let new_object = {}
    let object_keys = Object.keys(obj)
    for (i=0; i<object_keys.length; i++){
        let current_key = object_keys[i]
        new_object[current_key] = obj[current_key]
    }
    return new_object
}
let new_friend = deepClone(friend)

friend.yash = {
    hobbies: ['sleep']
}
console.log(new_friend)
```
Even if we add a new friend into the original object, as you can see console shows: { rupert: { hobbies: [ 'gym', 'reading', 'mathematics' ] } }

### Average grade function
Object iterationL given an object representing a studen'ts grades in various subjects, calculate their average grade.
```
let student = {
        maths: {
        grade: 93
        },
        science: {
        grade: 84
        },
        english: {
        grade: 68
    }
}

function average_grade(obj) {
    let list_of_subjects = Object.keys(obj)
    let sum = 0
    let num_of_subjects = 0

    for(i=0;i<list_of_subjects.length;i++) {
        let current_key = list_of_subjects[i]
        let subject_grade=student[current_key].grade
        sum = subject_grade + sum
        num_of_subjects++
    }
let average_grade = sum/num_of_subjects
return average_grade
}

console.log(average_grade(student))
```
Console: 81.67

### Scope and closure
Scope and closure: create a function that returns a new function. The returned function should remember and log the number of times it's been called.
```
function inception(){
    let number_of_invocations = 0

    return function() { //anonymous function
        number_of_invocations++
        console.log(number_of_invocations)
    }
}

let increment = inception()

increment()
increment()
increment()
increment()
increment()
increment()
increment()
increment()
```
Console:
1
2
3
4
5
6
7
8

### Array sorting descending order
Array sorting: write a function that sorts an array of objects based on a specific property (e.g., 'grades') in descending order.
```
let grades_array = [
    {subject: 'maths', grade: 10},
    {subject: 'science', grade: 8},
    {subject: 'english', grade: 7},
]

function sortbyGrade (arr) {
    let sorted_array = grades_array.sort(function(a,b) {
        return b.grade - a.grade
    })
    return sorted_array
}

console.log(sortbyGrade(grades_array))
```
Console:
[
  { subject: 'maths', grade: 10 },
  { subject: 'science', grade: 8 },
  { subject: 'english', grade: 7 }
]

### Array filtering for string length
Array methods: given an array of strings, filter out all the strings with a length less than 5 characters.
```
let subjects = ['maths', 'physics', 'chemistry', 'english', 'pe', 'bam']

function array_filter(arr){
    let new_array = []
    for (i=0;i<arr.length;i++){
    let current_string = arr[i]
        if(current_string.length>=5){
            new_array.push(current_string)
        }
    }
    return(new_array)
}

let filtered_array = array_filter (subjects)
console.log(filtered_array)
```
Console: [ 'maths', 'physics', 'chemistry', 'english' ]

### Count the number of occurences in a string - store in object
Object iteration: write a function that counts the number of each word in a given string and stores the results in an object.
```
let sentence_string = 'I like to eat, I like eat like, like, like to like eat cool'

function word_counter(str) {
    let counter_dict={}
    let split_sentence = sentence_string.replaceAll(',', '').split(' ')
    for (i=0;i<split_sentence.length;i++){
        let current_word = split_sentence[i]
            if(current_word in counter_dict) {
                counter_dict[current_word] = counter_dict[current_word] + 1
            } else {
                counter_dict[current_word] = 1
            }
        }
    return counter_dict
}
console.log(word_counter(sentence_string))
```
Console:
{ I: 2, like: 6, to: 2, eat: 3, cool: 1 }

## Set 3 - DOM Manipulation Functions

### Changing text content, headings, etc
Basic DOM Manipulation: How do you select an element with the ID main-title and change its text-content to "Welcome to the DOM World"?
```
let maintitle = document.getElementById('main-title')
maintitle.innerText = "Welcome to the DOM World"
```

### Event handling - apply a function on an event happening
Write the JavaScript code to listen for a click event on a button with the ID submit-btn and alert "Button Clicked!" See the code below for an example:
```
let submitButton = document.getElementById('submit-btn')

function alertFunction(){
    alert("Button Clicked!")
}

submitButton.addEventListener('click', alertFunction)
```

### Dynamic styling
Sometimes we need to have HTML elements change their styling dynamically for example when someone hovers over something, or when someone opens a window, etc. See the code below for a simple example of styling dynamically.

How can you change the background colour of a <div> with the class "highlight" to yellow when a user hovers over it using JavaScript?
```
let divHighlight = document.querySelector('.highlight')
divHighlight.addEventListener ('mouseover', highlightFunction)

highlightFunction() {
    divHighlight.style.background = 'yellow'
}
```

### Element creation and insertion
To create or insert a new element there are specific JavaScript methods. See the example below.

Describe how to create a new <li> element, set its text content to "New Item", and append it to an existing <ul> with the ID list-container:
```
let divHighlight = document.querySelector('.highlight')
divHighlight.addEventListener ('mouseover', highlightFunction)

highlightFunction() {
    divHighlight.style.background = 'yellow'
}
```

### Form handling
The default action for submitting a form is to refresh the page, however this can be disrupting, instead we will write a script to prevent the default submission of a form with the ID form-example and instead console log the value of a text input field within the form when the submit button is clicked.
```
let form = document.getElementById('form-example')
let textInput = document.getElementById('text-input-field')

function handleSubmitForm (e){
    e.preventDefault()
    console.log(textInput)
}

form.addEventListener ('click', handleSubmitForm)
```

### Event bubbling
Sometimes there will be an element with an event listener attached that is activated while inside a container that also has another event listener attached. We don't want both events being responded to, but want just one. Otherwise they can overlap each other and not work well. Provide an example of stopping event bubbling when clicking on a <button> contained within a <div> that both have click event listeners attached.
```
let btn = document.querySelector('button')
let divContainer = document.getElementById('div')

function stopButtonPropagation (e) {
    e.stopPropagation()
}

btn.addEventListener('click', stopButtonPropagation)
```
Not 100% sure about this one tbh.

### Dynamic page styling
Sometimes we will have elements on our pages that can be toggled for different effects, for example light/dark mode for websites. How can we toggle a class active on an element when it is clicked, ensuring that if the class is present it gets removed, and if its not, it gets added?
```
let toggleElement = document.getElementById('toggle-element')

function toggleStyle() {
    toggleElement.classList.toggle('active')
}

toggleElement.addEventListener('click', toggleStyle)
```

### Advanced event handling
Write JavaScript code to change the text content of a paragraph element to display the current time when a button is clicked. This can be applied to displaying any other item we want, in this example below we are showing time.
```
let paragraphElement = document.querySelector('p')
let xbtn = document.querySelector('button')

const currentTime = now.toLocaleTimeString

function displayTime(){
   paragraphElement.innerText = currentTime
}
xbtn.addEventListener('click', displayTime)
```
Also not sure about this one.

### Event listener removal
Nothing too complex here, just removing an event listener. The reason why you might need to remove an event is if you only want it to operate conditionally. You may have certain situations you want it and certain situations you dont. See the code below for an example:
```
document.getElementById('james-is-cool').removeEventListener('click', myFunction)
```

### Manipulate attributes and properties
Attributes are basically properties defined in the HTML and properties are basically attributes defined in JavaScript. So if you are working in JavaScript its called a property - the descriptor of the tag, and if you are working in HTML its called an attribute.
For example, if we wanted JavaScipt code to change the src attribute of an <img> element to a different destination, here is what the code might look like:
```
document.querySelector('img').setAatribute('src','new-image.png')
```

### Utilise dataset attributes
Sometimes HTML elements will hold data inside the tag, using data attributes. This is how to use data-* attributes within an HTML element to store extra information and how to access this information using JavaScript. See the code below:
```
let informationDiv = document.getElementById('info')
console.log(informationDiv.dataset.userId)

<div id = "info" data-user-id="12345" data-user-role="admin"></div>
```

## Set 4 - Object Oriented Programming
Write a JavaScript class named REctangle that has two properties, width and height, initialised through its constructior. Then, instantiate an object of Rectangle with a width of 5 and a height of 10.
```
class Rectangle {
    constructor (width, height){
        this.width = width
        this.height = height
    }
}

const rect_obj = new Rectangle(5,10)
console.log(rect_obj)
```

How do you create a constructor within a class named Circle that initialises a property radius and sets its value based on the argument passed when a new Circle instance is created?
```
class Circle {
    constructor(radius){
        this.radius = radius
    }
}

const new_circle_object = new Circle(4)
console.log(new_circle_object)
```

Explain how you would add a method named calculateArea to the rectangle class that calculates the area of the rectangle. How does this method get added to the prototype of the class, and how can all instances of Rectangle access it?

class Rectangle {
    constructor (width, height){
        this.width = width
        this.height = height
    }
    calculateArea(){
        let area = this.width*this.height
        return area
    }
}

const rect_obj = new Rectangle(5,10)
console.log(rect_obj.calculateArea())
```

In the context of a class method in JavaScript, what does the 'this' keyword refer to, and how would you use it inside a method named describe in a class Person to access the instance's properties named name and age?

class Person {
    constructor(name, age){
        this.name = name
        this.age = age
    }
   describe(){
    console.log('The name is ' + this.name + ' and the age is ' +this.age)
   }
}

const yash = new Person('Yash', 27)
yash.describe()

const second_person = new Person('Cherry', 24)
second_person.describe()
```

Create a class named Animal with a constructor that initialises a property species. Then, define a subclass named dog that inherits from Animal and adds an additional property name in its constructor. How do instances of Dog access methods defined on Animal's prototype?
```
class Animal {
    constructor(species) {
        this.species = species
    }
    describe (){
        console.log(this.species)
    }
}

class Breed extends Animal {
    constructor(species, breed){
        super(species)
        this.breed = breed
    }
}

const myAnimal = new Animal('dog')
console.log(myAnimal)

const myDog = new Breed ('dog','staffy')
console.log(myDog)
```