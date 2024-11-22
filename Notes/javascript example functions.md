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
Write a JavaScript class named Rectangle that has two properties, width and height, initialised through its constructior. Then, instantiate an object of Rectangle with a width of 5 and a height of 10.
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

## Set 5 - Asynchronous Programming
Create a function that uses the following asynchronous sleep call to print the message 'hellow world' after 2 seconds
```
const sleep = ms => new Promise(r => setTimeout(r, ms));

async function printHello () {
    await sleep(2000)
    console.log('hello world')
}

printHello()
```

Write an async function that attempts to fetch data from 'https://api.example.com/nonexistent', which will likely lead to a 404 error. Use try/catch to handle the error and log "Error fetching data" if the request fails.

async function fetchData() {
    try {
        const res = await fetch ('https://api.example.com/nonexistent')
        console.log ('successfully fetched')
    }
    catch (err) {
        console.log(err.message)
    }
}

fetchData()

3. Write an async function named fetchUserData that makes a GET request to 'https://the-one-api.dev/v2/book' using async/await. Lof the response to the console, handling any errors that might occur.
```
async function fetchUserData() {
    try {
        const res = await fetch ('https://the-one-api.dev/v2/book')
        const data = await res.json()
        console.log (data)
    }
    catch (err) {
        console.log(err.message)
    }
}

fetchUserData()
```
4. Demonstrate how to make a POST request to 'https:api.example.com/users' to create a new user with JSON data {name:"John", age:30} using async/await. Ensure you set the appropriate headers and catch any errors.
```
async function postUserData() {
    try {
        const options = {
            method: 'POST',
            headers: {
                'content-type':'application/json'
            },
            body: JSON.stringify({name: 'John', age: 30})
        }
        const res = await post ('https://api.example.com/users', options)
        const data = await res.json()
        console.log (data)
    }
    catch (err) {
        console.log(err.message)
    }
}

postUserData()
```

## Set 6 - Modern ES6+ JavaScript Syntax
1. How do you create a string that includes both static text and the value of the variable name, using template literals?
```
let name = 'gregothy'
let special_string = `hello my name is ${name}`

console.log(special_string)
```

2. Convert the following function into an arrow function syntax:
```
function add(a,b) {
    return a + b;
}
```
Here is the new code:
```
let add = (a, b) => { return a + b }
console.log(add(2,3))
```

3. Given an object person with properties name and age, use object destructuring to create two variables name and age, extracing the values from the object.
```
const person = {
    name: 'yash',
    age: 27
}

const {name, age} = person
console.log(name,age)
```

4. Given an array colours with the values ['red', 'green', 'blue'], use array destructuring to create three variables named first, second and third, assigning the first, second, and third elements of the array to them, respectively.
```
colour_array = ['red', 'green', 'blue']
let [first, second, third] = colour_array

console.log(first, second, third)
```

5. How do you create a new array combined that contains all the elements of array arr1 and arr2 using the spread operator?
```
arr1 = [1,2,3,4]
arr2 = [5,6,7,8]

let arr3=[...arr1,...arr2]
console.log(arr3)
```

6. How do you create a new object combinedObject that merges the properties of two objects obj1 and obj2, with properties from obj2 overwriting those in obj1 if they exist in both objects?
```
let obj1 = {name: 'henry', age: 14}
let obj2 = {name: 'gregothy', colour: 'blue}
let combined_obj = {
    ...obj1,
    ...obj2
}

console.log(combined_obj)
```

The second object is the one who's name remains, because the most recent value of the same key will remain.

7. How do you safely access the street property address inside an object user that may not exist, using optional chaining?
```
const user = {name:'yash'}
console.log(user?.address?.street)
```

8. Define a function greet(name, greeting = "hello") that takes a name and an optional greet. If the greeting is not provided it should default to "hello".
```
const greet = (name, greeting = 'Hello') => {
    console.log(`${greeting} ${name}`)
}
greet('yash', 'ni hao')
```

9. Explain the differnce between let and const keywrods, and give an example of when you would use each.
```
let chosen_number = 4
chosen_number = 83

const my_name ='yash'
```

10. Write a for...of loop that iterates over an array numbers and logs each number to the console. Below are two simple ways of doing it.
```
let new_array = [1,2,3,4]
new_array.forEach((current_value, current_index) => {
    console.log(current_value)
})

for (let current_value of new_array) {
    console.log(current_value)
}
```

11. Given an array of numbers, use the map method to create a new array with each number squared.
```
let new_array = [1,2,3,4]

let updated_array = new_array.map((current_value, current_index) => {
    return current_value*current_value
})

console.log(updated_array)
```

12. How would you use the ternary operator to assign "adult" to a variable ageStatus if age is 18 or over, and "minor" if under 18?

```
let age = 14
let ageStatus = age.valueOf()>18 ? 'Adult':'Minor'
console.log(ageStatus)
```

13. How do you use the logical AND operator to execute a function logMessage() only if the variable is LoggedIn is true?
```
const logMessage = () => {console.log('logged in')}

let isLoggedIn = true

isLoggedIn && logMessage()
```

14. How can you use the logical OR operator to assign a default value of "guest" to a variable username if the current user.name is defined or null?
```
let user = {
    name: 'banana muffin'
}

let username = user.name || 'guest'

console.log(username)
```

## Set 8 - Algorithmic Programming Questions
1. Unique Characters in a String
Question: Write a function to determine if a string has all unique characters. Return true if all characters are unique, and false otherwis. Assume the string only contains lowercase letters.

```
let string_1 = 'helloworldmynameisyashandilikeicecream' // should have repetitions
let string_2 = 'thequickbrownfoxjumpsoverthelazydog' //definitely has repetitions
let string_3 = 'abcdefghijk' //cannot have repitition

// Need to create a function that checks if the character in the string is unique
function isUnique(str) {
    // Create an empty dictionary that will record when a character shows up uniquely.
    let count_dict = {} 
    // Now loop through the string to assess each character individually. 
    for (let i = 0; i < str.length; i++) {
        let current_char = str[i]
        // Conditional heck if the current character is present in the dictionary - if it is present, its not unique - return false and the code stops there (this is the break that we were talking about for efficiency - no need to execute the code further).
        if (current_char in count_dict) {
            return false
        }
        // If it is unique, add the current character to count_dict.
        count_dict[current_char] = 1
    }
    // The return true line is outside of the loop because you don't need it to return true for every instance that is unique - you just need to check all and give a true response once.
    return true
}

console.log(isUnique(string_2))
```

2. Merge Sorted Arrays
Question: Given two sorted arrays nums1 and nums2, write a function to merge them into a single, sorted array.

```
let string_arr_1 = ['a', 'b', 'c', 'd', 'e', 'f']
let string_arr_2 = ['a', 'b', 'c', 'd', 'e', 'f']

let arr_1 = [2,4,6]
let arr_2 = [1,3,5]

// Standard spread operator function and put back together + sort at the end.
let merge_sort_function = (first_array, second_array) => {
    let merged_array = [...first_array, ...second_array].sort()
    // Putting return inside the function is more efficient - don't need to console.log it unless we specifically want to at some point. And if we do want to we can just console log the whole function.
    return merged_array
}
console.log(merge_sort_function(string_arr_1, string_arr_2))
```

3. Find All Duplicates in an Array
Question: Given an array of integers where 1 <= a[i] <= n (n = size of the array), some elements appear twice and others appear once. Write a function that returns an array of all the elements that appear twice in a given array. You must achieve this with O(n) time complexity and O(1) extra space complexity.

```
//Since we are only allowed O(n) time complexity we are only allowed a single loop.
let dummy_arr = [1, 4, 1, 2, 3, 4, 6, 5]

let findAllDuplicates = (nums) => {
    let duplicates = []
    let count_dict= {}
    // Use a count dictionary with this simple for loop to check if that value is in the count dictionary, if it is, then push it to the duplicates array. If not, then create a key-value pair in the count_dict where the key is the number and the value is 1. This way it shows up only once in the dictionary, and additional repetitions get pushed to a new array called duplicates.
    for (let current_value of nums){
        if (current_value in count_dict) {
            duplicates.push(current_value)
        } else {
            count_dict[current_value] = 1
        }
    }
    return duplicates
}
console.log(findAllDuplicates(dummy_arr))
```

4. Rotate Array
Question: Rotate an array to the right by k steps, where k is non-negative. Modify the input array in-place with O(1) extra space.

```
let start_array = [1, 2, 3, 4, 5, 6]

rotate_array = (nums, k) => {
    let end_values = nums.slice(k)
    let start_values = nums.slice(0,k)
    
    let new_array=[...end_values,...start_values]
    return new_array
}

console.log(rotate_array(start_array, 3))
```

5. Valid Parentheses
Question: Given a string s containing just the characters '(',')','{','}','[' and']', determine if the input string is valid. An input string is valid if:
    - Open brackets must be closed by the same type of brackets.
    - Open brackets must be closed in the correct order.

```
let s = '()[]{}'
let s_2 = '())[{]{)}'

function validParentheses(str) {
    const combos = {
        '{': '}',
        '[': ']',
        '(': ')',
    }

    let stack = []

    for (let current_bracket of str) {
        if (stack.length === 0) { //if theres nothing there in stack then push one
            stack.push(current_bracket)
        } else if (current_bracket in combos) { //opening bracket check
            stack.push(current_bracket)
        } else { //if we reach this stage it has to be a closing bracket
            let last_value_on_stack = stack[stack.length - 1]
            if (!(last_value_on_stack in combos)) { //this checks if last value on the stack is NOT an opening bracket (but not yet if its the correct one)
                stack.push(current_bracket)
            } else {
                if (combos[last_value_on_stack] === current_bracket) { //this checks if the last value is the same as what is currently there (essentially a repeat) then it pops it from the stack.
                    stack.pop()
                }
            }
        }
    }

    return stack.length === 0
}

console.log(validParentheses(s_2))
```
