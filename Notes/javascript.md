# JavaScript Notes

## Introduction to JavaScript
JavaScript is a programming language that controls how users interact with a particular website. While HTML and CSS are responsible for the content and how its presented to the user, JavaScript controls the entire element of animations, interactions and just "movement" of the website.

It is a programming language that is **sequential**, as in it is executed from top to bottom and has many conditions and loops that must be followed with varying levels of importance. Check that your code follows a logical order and make sure each instruction is either on its own line or followed by a semicolon ;. This is different form HTML and CSS, where HTML and CSS are both "static", meaning that they are immediately executed and they do not change (yes CSS has some basic hover effects and what not, but its not a true animation like JS). JavaScript has its own separate syntax.

## How it works
Programming in general is essentially just a written out set of instructions that tell the computer/device interacting with the code what needs to happen. Basically like a recipe that puts multiple components together in a certain order to result in a delicious finished product.

As mentioned above JavaScript code must be executed using a runtime (like C++). The runtime interprets the code (set of instructions) and translates it into machine code (like how C++ compiles into an .exe file). The code is then executed on a machine (as per said instructions), either locally or on the cloud.

## Levels of programming
There are different levels at which programming languages operate. Low-level vs high-level is like machine vs human.

Low-level languages would be the languages that operate entirely within a machine environment, hence would be utilising machine code. These machines are structured and predictable so the instructions can be very simple, yet the syntax is complex as it does not really need to be read by a human, it just comes downs to zeroes and ones.

High-level languages would be the languages that are interacted with significantly by humans and allow for a variety of human interactions. There are a huge number of variables when it comes to human interaction and design so the instructions can be complex and specific, but the language is read by humans so it is easily understandable and close to english. We can get the general gist of it when we look at it.

## General notes

### How to write your JavaScript code well
Break down your code into its different functionalities, then invoke them in an order that makes sense, and when it is necessary. This will keep your code very clean and effective.

## Terminal/Console
The terminal or the console is where we go to run our javascript files. You can go into the terminal and type in as below:
```
node file_name.js
```

If the file is in a lower folder you must parse in the folder address where the file is located. For example:
```
node folder_name/file_name.js
```
Generally the terminal/console should print something. If the console doesn't return anything it means that there is nothing wrong with the code, but there is no command warranting the console to present a message.

### Executing
Remember to always save a modified file before executing the file program again, because the terminal will always just pull from a directory which has the most recently saved files. If you haven't saved it, the terminal will pull the same old version, not your edited one.

What we do in the code editor (with JavaScript) is utilise the console log with () inside which we put our function:

```
console.log()
```

Without a function, the terminal will print only an empty space. We need to try with our text string 'hello world' inside it. 

```
console.log('hello world')
```

And magically the console will print "hello world" in the next line. It will also print other things you put in there such as mathematical functions. for example if you put 4 + 4 inside the brackets, the console will return the value 8.

### Debugging
Faulty code will now be a lifelong problem for you as a software developer, its impossible to get it correct on the first try. However, when your program doesn't run correctly, you need to go through a debugging process to identify where the problem lies in your code.

We can use the console to debug our code - in fact it is the most useful way to debug JavaScript code.

## Fundamental JavaScript syntax

### Text
Words/phrases/sentences can be incorporated into JavaScript code by utilising either ' or " around either side of the text. The characters, words, or sentences going together are known as a string, ie a string of text. Any string of text can sit inside these apostrophe/speech marks and be recognised by JavaScript as a string.

"hello world"
'hello world'

However, if you are trying to print some text but nothing shows up (as discussed just above) it might mean that your string is correctly formatted but no instruction to print has been given. You need to introduce a print function.

If you need to use either the apostrophe or the quotation mark in your sentence, just use the other one to do the logic. Or alternatively, if you wan't to "escape" a variable, you just put a backslash before it. For example 'yash\'s house is cool' would print out Yash's house is cool.

### Variables
We can use something called variables. If we take something as simple as the string "I like apples". If we wanted to print this multiple times, rather than write it out every time, we could assign it to a variable. It could be text, numbers, colours, etc. See some examples below:
General format is var = value
```
sentence = "I like apples"

number_of_apples = 8
```
Variables help to make out code extra clean, and allow us to reuse them throughout our code with the exact same values without manually entering the value again.

However, you must remember that the first time you introduce a variable you must initialise it using proper syntax, and then after that you must use it as shown above (you cannot initialise twice). To initialise a variable we can use 'let', const', 'var'. We won't use 'var' so much, but 'const' and 'let' are more modern and will be the ones we use most.

"const" = constant, and this is used when the value of that item will not change again.

```
const sentence = "hi mum"
let number_of_apples = 3
number_of_apples = 8
console.log(sentence)
```
The console will always return the value "hi mum"". If you try to assign another value to a constant variable (such as "hi dad"), the console will give you a "TypeError: Assignment to constant variable."

"let" = assigned value, it is what it is for now, but it can be reassigned a different value later on. See the code below:

```
const sentence = "hi mum"
let number_of_apples = 3
number_of_apples = 8
console.log(number_of_apples)
```
The console will return the value 8.

"function" = enter function to return a value. Inside the brackets is an argument/s and then within the curly brackets is the actual function when we want to invoke it. A good function name describes the behaviour of the function.

```
function myFirstFunction() {
    // output the value of is_true
    insert function in here
}
```

**Important note** - while it is obviously possible to execute a function, loop, etc while being efficient and pulling exactly what you need from previous data. It is good practice to assign the calculation to a new variable and just call the variable rather than enter the calculation directly into a function.

#### Rules for Variables:
1. You cannot start your variable name with a number.
2. You cannot leave spaces in your variable name - use snakecase or camelcase. Snakecase is when you replace the spaces with underscores. Camelcase is when you make the first letter of the first word lowercase, and then the first letter of every subsequent word uppercase. Example
    snake_case --> number_of_apples = 8
    camelCase --> numberOfApples = 8
3. The first time you use a variable, you must initialise it with proper syntax, and thereafter reference it by itself.
4. At the top of your document you can initialise a variable without assigning a value to it ie, "let variable_name" and then assign a value later on in your code.
5. Multiple variables can be initialised with a comma separation.
6. You can assign a variable by reference to an existing variable.
7. Variables that reference other variables will only reference the most recent value when that variable is initialised. As mentioned above JavaScript is a sequential or top-down programming language - each line only has the lines before it to accurately follow instructions from.

### Comments
To make something a comment just use "//" at the start of that line of code. This way you can leave notes for yourself of what you learned, what you found useful, what you think you might want to use in a future project, etc. You can also use "//" after some code and everything after that will be a comment.

### Data types
- 1988789 - this is a number
- 'hello world' - this is a string of characters
- null - this is a special keyword that means the 'absence of a value'
- undefined - this represents the absence of a value, but not because it hasn't been assigned, but because we might intentionally want to set it to nothing.
- true - this represents as a 1 or yes or true. Booleans
- false - this represents as a 0 or no or false. Booleans
- () - this is the way to invoke or call a function which can manipulate data - it is essentially just something as a function of what is inside the bracket.
- {} - this is known as an object/dictionary - these are used to store complex data and multiple var/value pairs. These are known as key value pairs, and the dictionary can store many of them. The key value pairs must be separated by commas. See below
- [] - this is known as an array - it is essentially a list of values. Each value must be comma separated. The first entry is always indexed at 0. Index = n-1
- A function is a sub type of object that can be pre-programmed and then invoked/called in the future. Example: 'function add(x, y) {return x + y;}'

You can check data types by using the 'typeof' function in your console.log. It will pull the result into the console.

### Operators
#### Numerical operators
- '=' is an assignment operator
- '+', '-', '/', '*' all standards maths operators apply
- '%' is known as the modulus and that returns the remainder after dividing the first value by the second value.

#### Boolean operators
- '==' is a comparison operator (**soft** equality) to see if one value is more or less equal to another. It will only return true or false.
- '===' is a comparison operator (**hard** equality) to see if one value is exactly equal to another. It will only return true or false.
    Now there is a difference between the two that can be illustrated by the code below:
    ```
    function myFirstFunction (value, secondValue) {
        console.log(value==secondValue)
    }
    myFirstFunction('5',5)
    ``` 
    This would return a value of 'true'. However:

    ```
    function myFirstFunction (value, secondValue) {
        console.log(value===secondValue)
    }
    myFirstFunction('5',5)
    ``` 
    This would return a value of 'false', because the first '5' is a string and the second 5 is a numerical value. 
- '!=' is a comparison operator (**soft** inequality) - it checks to see if one value is not equal to another. It will only return true or false.
- '!==' is a comparison operator (**hard** inequality) - it checks to see if one value is strictly not equal to another. It will only return true or false.
    For these two the difference is exactly the same as the equality ones above, except the result would be reversed.

#### Logical operators
- 'and' condition is a logical operator that states that **both** conditions inside must be simultaneously true. Even a single false result will return false.
Syntax: &&
- 'or' condition is a logical operator that states that **either** condition inside must be exclusively true.
Syntax: ||
- 'not' condition is a logical operator that states that **if not** this condition, then the opposite must be true. It returns the opposite value
Syntax: !
- Along with logical operators you can have mathematical functions to check for conditions, ie, >, <, =>, <=.

#### Falsy values
There are some values such as 0, or empty strings such as ' ' which tend to show up as false in JavaScript. so !0, would actually return true in the log. It's not too big of a deal, but just be mindful when programming that you don't unintentionally get the wrong value.

## Conditional Logic

### Conditional statements
We can also have functions or code that are executed based on certain conditions through the use of if and else statements, as well as and and or loops. It is very simple to use and works exactly as it would logically make sense in your head. The code might look something like this:
```
let condition1 = true
let condition2 = false

if (condition1) {
    console.log('hi mum')
}
```
The above would print out 'hi mum'. If it was condition2 inside the if statement, then condition 2 would be 'false' so it would not return anything.

You can introduce logical operators in conditional statements and loops if you want to check that multiple variables are either same, different, or whatever. And you can have if, elseif, and if statements work together to cover all possibilities. For example:
```
let condition1 = true
let condition2 = false

if (condition1 && condition2) {
    console.log('hi mum')
} else if (condition1 || condition2) {
    console.log('could be mum or could be dad')
} else {
    console.log('i guess its dad')
}
```
The code above would return 'could be mum or could be dad' because only one of the conditions are true. If condition 2 was true, then it would return 'hi mum', and if condition 1 were false, then it would return 'i guess its dad'.

### Loops
The purpose of a loop in JavaScript is to write a body of code once and execute it numerous times (could be thousands) until a particular condition is met. Often it goes through iterations until a particular number of iterations is reached a count. Typically counting variables are assigned as i, j or k. Lets go through each of the types of loops.

#### While Loops
While loops are pretty much what they sound like, the code inside keeps getting executed while a condition is met, typically as long as i is less than the length of the array lets say. Note that in a while loop there are only 2 arguments in there i >=< x. Anyways lets see some examples below.
```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]

let i = 0
let length = example_array.length
console.log(length)
while(i<length) {
    console.log('value was true', i)
}
```
This will run my computer into an infinite loop, because i is always 0, and it is always less than the array length (which is 11). We must format i to be a counting variable, it must increase with each iteration. The correct code would be:
```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]

let i = 0
let length = example_array.length
console.log(length)
while(i<length) {
    console.log('value was true', i)
    i = i + 1
}
```
This would cause i to increase with every iteration, eventually reachin 11 and meeting an end condition. 

There are a couple of shorthands for changing i:
- i = i + 1 can be represented as 'i++'
- i = i - 1 can be represented as 'i--'

We can also access the value at that index number within the array and print it in the console log. For example, see the code below:
```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]

let i = 0
let length = example_array.length
console.log(length)
while (i<length) {
    console.log('value was true', i, example_array[i])
    i = i + 1
}
```
This would print the index number as well as the corresponding value in that position for each entry.

#### For Loops
For loops are pretty much what they sound like, the code inside keeps getting executed while a condition is met, typically as long as i is within a particular range. Note that for loops are very similar to while loops, but have 3 arguments inside. the i sits within a range, and only for values within that range is the function executed.

```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]
let length = example_array.length

for (let j = 0; j < length; j = j+ 1) {
    console.log('value was true', example_array[j])
}
```

Something to note about for loops is that if you want to skip a particular value, for example if you wanted to skip every even number then you could put a function in like below and use the 'continue' command. Continue allows the function to continue onwards whil skipping the j values where that condition is met.

```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]
let length = example_array.length

for (let j = 0; j < length; j++) {
    if (j % 2 === 0) {
        continue
    }
    console.log('value was true', example_array[j])
}
```

Similarly, we can use the 'break' function to break a loop when a particular condition is met. Contrary to the continue function the break function causes the program to stop running once the j value is meets the condition - basically kill the loop early. See below:

```
let example_array = [1,5,7,8,3,4,5,6,4,2,1]
let length = example_array.length

for (let j = 0; j < length; j++) {
    if (j === 6) {
        break
    }
    console.log('value was true', example_array[j])
}
```

#### Planning out your conditional flow
It is very important to plan out your conditional flow properly, otherwise your formulas/code may not work or make sense, simply because you have a misunderstanding of the direction i is supposed to go in, or something similar. Really take the time to write down on a piece of paper how its supposed to flow, and then reverse engineer the code required to make that work.

It might be worth doing a condition flow chart or something like that, which visualises what needs to happen for the next code to be executed. Once you have done that and the path makes sense, you can assign arrays or other data (on a piece of paper) to these steps in the flow chart. After all this, it should be easy to actually write out the code with the proper knowledge of what is going to occur next.

## Basic Functions

There are a few things you can do with different basic functions that result in essentially the same value. 

- Printing two separate strings together:
```
function addStrings(string1, string2) {
    console.log(string1, string2)
}
addStrings('hello', 'mum')
```

If you run this in the terminal it will return "hello mum", despite us entering two different strings in there. This is just printing out two separate strings, they are still individual.

- Joining strings together (string concatenation):
```
function addStrings(string1, string2) {
    console.log(string1 + string2)
}
addStrings('hello', 'mum')
```

Running this in the terminal prints "hellomum". See how this joined both of the words together, but because there is no space anywhere in the function, there is no space here. The simple fix to this would be to concatenate a space also in the same function ie (string1 + ' ' + string2).

- Cancelling code if conditions aren't met (similar to break) is doable through the use of the return function. If the condition isn't met, then return stops the function from continuing.

```
function addStrings(string1, string2) {
    if(!string1 || !string2) {
        return
    }

    let concatString = string1 + ' ' + string2
    console.log(concatString)
}

addStrings('hello', 'mum')
```

This code above will return hello mum because there are both arguments (string 1 and string 2) present in the addStrings function so the logic continues through. However, if we failed to input one of the arguments, such as 'mum', then the function would completely fail. In fact we could even program some type of error message to show up if an input was missed as shown below:

```
function addStrings(string1, string2) {
    if(!string1 || !string2) {
        console.log('you are missing an input')
        return
    }

    let concatString = string1 + ' ' + string2
    console.log(concatString)
}

addStrings('hello')
```
- Return a value to a new variable - you can also just return a value and assign it to a new variable by putting the original variable name in front of return and then assigning the function itself to a new variable. For example:
```
function addStrings(string1, string2) {

    let concatString = string1 + ' ' + string2
    return concatString
}
let newString = addStrings('hello', 'mum')
console.log('the new string is: ', newString)
```

This would return "the new string is hello mum" in the console.

- Presenting default values if one of the arguments is not present. Similar to the return (empty) function, we can actually set default values to the arguments in our function. So when the function is called at any other time and an argument is missing from the code, then the function will revert back to the original value for the missing one. This can stop code from breaking, and be useful in calculations where a data point might be missing, but the default could be say the average value (so it would be a good representation). Here is an example of the code:

```
function addStrings(string1 = 'dafault1', string2 = 'default2') {
    let concatString = string1 + ' ' + string2
    return concatString
}
let newString = addStrings('hello')
console.log('the new string is: ', newString)
```

The code above would return the value of 'hello default2' in the terminal because the argument for string2 was missing in the original addStrings function so JavaScript uses the default value to keep the code from breaking.

## Data Manipulation
### String Manipulation
#### String Concatenation
We can access values in a string, for example we can pull a particular value at a particular index in the sentence 'this is a string'. See the code below:

```
let example_sentence = 'this is a string'
let string_length = example_sentence.length

console.log('Value at the end of the string = ', example_sentence[2])
```

Now if we want to add two strings together, we would enter code as shown below:
```
let combined_string = 'hello world' + ' ' + 'my name is yash'

console.log(combined_string)
```
This would print out "hello world my name is yash" in the console.

We can also pull something from another string and join it to ours using the same as above, however instead of a second string you just add an array[i].

#### Addition
We can also do something called coersion whereby if we add a number and a string of a number, it will put them both together into a new string. For example:
```
let combined_string = '3' + 5
let new_var = combined_string + 6
console.log(new_var)
```
The combined string variable would become '35' due to coersion. And finally the console would display new var being '356' as a string, so the value is not 8 or 14 but '356'. So if you tried to run a typeof function it would result in a string.

#### Subtraction
If you do subtraction from a string, it will return the string back to a number and give a result of a number. For example:
```
let combined_string = '3' + 5
let new_var = combined_string - 6
console.log(new_var)
```
The console would return the value 29 as a number!
It is important to be aware of how JavaScript handles these sorts of things in relation to strings, addition/subtraction is different.

### String Methods
There are inherently built in functions such as length, indexOf, split that we can use in JavaScript. The way they are used is you must have the variable and then put .[insert method] in front of it (there are no square brackets, thats just a place holder). For example for length of a string the code would look like this:
```
let example_sentence = 'this is a string'
let string_length = example_sentence.length
```

In visual studio code the intellisense is very helpful with this. If you have a variable that you put a period in front of, it will provide a whole list of autofill options for methods that you can manipulate the variable with. If it recognises the data is a string, it will show all the methods for strings, and respectively the same for other types of data. It would be impossible for us to cover or remember all, so just pay attention to your intellisense - you can do a lot of things with methods. Let's cover a few of the important/frequent ones.

In case you are interested, here is a whole documented list of methods available:
https://www.tutorialspoint.com/javascript/javascript_builtin_functions.htm

#### .indexOf ()
The first method thats pretty simple to use is indexOf which returns the index where the argument is present within the variable being checked. For example:

```
let example_sentence = 'this is a string'
let string_length = example_sentence.length

const contains_the_letter_a = example_sentence.indexOf('a')
console.log('sentence contains the letter a?', contains_the_letter_a)
```
This returns a value of 8 in the console because the letter a is in the 8th position in the string. If we were to switch the argument in the indexOf function to something that isn't present in the variable, for example 'z', then it would return a value of -1 meaning that its not present.

#### .split ()
We can use split to return the values of the string split up into individual components, and the components can be characters, words, sentences, depending on how you formulate the function. For example if we wanted to get back all the letters in a string the fuction would look like below:
```
let example_sentence = 'this is a string'
const split_sentence = example_sentence.split('')
console.log(split_sentence)
```
This would return an array in the console with values: 
[
  't', 'h', 'i', 's',
  ' ', 'i', 's', ' ',
  'a', ' ', 's', 't',
  'r', 'i', 'n', 'g'
]

This is because the argument inside of the split function is '' two speech marks with no space in between - so the function is instructed to split up every character. If we wanted to split up the words, we would put a space inside the speech marks as shown below:
```
let example_sentence = 'this is a string'
const split_sentence = example_sentence.split(' ')
console.log(split_sentence)
```
This would return an array in the console with values: 
[ 'this', 'is', 'a', 'string' ]

Now, if we wanted to do sentences, we would enter a period '.' inside the function as an argument. Pro tip: enter a space in front of the period so that the values you receive (which will be smaller strings) don't have a space at the start. See the code below:
```
let example_sentence = 'this is a string. this is also a string'
const split_sentence = example_sentence.split('. ')
console.log(split_sentence)
```
This would return an array in the console with values: 
[ 'this is a string', 'this is also a string' ] - this is with a space after the period.
[ 'this is a string', ' this is also a string' ] - this is without a space after the period.

Essentially a split function filters out whatever the argument is that you put inside it.

#### .includes ()
Includes is a cool function that will return a true or false if the argument is present in the variable or string that is being checked. For example:
```
let example_sentence = 'this is a string'
const value_exists = example_sentence.includes('a')
console.log(value_exists)
```
The console will show true because 'a' is present, if instead we searched for 'z', it would show up false.

#### .replace() and .replaceAll()
This is very self-explanatory, however there are two arguments that go inside the function, first is what you want to remove, and second is what you want to replace it with - replace.(a, b). There are two versions - replace will replace only the first encounter of the value matching the argument inside, whereas replace all will...you guessed it...replace all encounters of the argument inside. Once it has done its function it will return the edited string into the console. If you enter a value that isn't in the string, it will just return the original string. See below for .replace and .replaceAll:
```
let example_sentence = 'this is a string'
const replace_letter = example_sentence.replace('i, I')
console.log(replace_letter)
```
This would return 'thIs is a string'

```
let example_sentence = 'this is a string'
const replace_letter = example_sentence.replaceAll('i, I')
console.log(replace_letter)
```
This would return 'thIs Is a strIng'.

A very useful example of this is if you wan't to display some text or a file name that has been saved with - or _ in the string. We can use replace all to remove them and replace with spaces so that it looks clean.

#### .slice()
Slice is very common as a function, it typically takes two arguments, a starting index and ending index. It will then return just that portion of the string. For example:
```
let example_sentence = 'this is a string'
const slice_word = example_sentence.slice(2,8)
console.log(slice_word)
```
The code above would return a portion of the string 'is is' as that is everything included from "i" which is index = 2, and up to "s" which is index = 8.

If you only enter 1 argument, then it will still work, but it will take everything after the argument inputted. For example:
```
let example_sentence = 'this is a string'
const slice_word = example_sentence.slice(5)
console.log(slice_word)
```
This would return 'is a string' as that is whats left after index = 5.

#### regex
Regex is a way of checking if a string or password or any regular expression contains certain characters. There are some very complicated rules for regex but you can implement this in your JS by going to chat gpt and asking it to provide some code as well as how to implement it.

### Array Methods
Arrays or lists are very important data structures and they hold a variety of different data, keeping in mind that each value has to be a valid data type. Just like the string, arrays also have a bunch of methods that can be used to manipulate data in them. The primary things we have to do with objects and arrays is follow the CRUD operations. CRUD stands for create, read, update and delete. 

This way any information stored in an array can be constantly updated in a database through user interactions. There is a certain order in which we can learn these operations.
#### Dimensionality of arrays

#### Read
This is probably the most simple. Similar to how we used the array function above, we can input any index value in the argument to read the corresponding word in that position within the array. See the function below for an example:
```
let simple_array = ['yash','is','cool']
console.log (simple_array[0])
```
The console will return 'yash' as that is the value in the 0th position in the array.

Most of the read methods are similar to string such as .includes, .ofType, .indexOf, .slice, etc. These will work just the same as they did with the string.

**Join**
An interesting one that is different from strings is .join. For strings we have split as a string is one value together. Whereas in an array we have multiple values that can be joined together. We can use .join to join elements inside an array together with a value that we parse into the argument. For example:
```
let simple_array = ['yash','is','cool']
let check = simple_array.join('-')
console.log(check)
```
The console would return the string 'yash-is-cool'.

**Reverse**
We can also reverse the order of the values in the array using the reverse function. It takes no arguments. For example:

```
let simple_array = ['yash','is','cool']
let check = simple_array.reverse()
console.log(check)
```
Entering this into the console returns the array [ 'cool', 'is', 'yash' ].

**Sort**
We can also sort the order of the values in the array into an alphabetical order using the sort function. It takes no arguments. For example:

```
let simple_array = ['yash','is','cool']
let check = simple_array.sort()
console.log(check)
```
Entering this into the console returns the array [ 'cool', 'is', 'yash' ]. It just so happens to be the same as the reverse one for these particular strings, but it has sorted it alphabetically.

#### Update
With our initial understanding of JavaScript we can update the information within an array just by assigning a new value to said position for example: 
```
simple_array[1] = 'hello'
console.log (simple_array)
```
If we follow up the read code with this code just above, the console will now return [ 'yash', 'hello', 'cool' ] as simple_array has now been updated with a new value in index position 1.

 However, this provides very limited functionality since we would have to know the index position of a particular value to replace it, and we could be working in an evergrowing data structure of thousands of values for a single variable out of thousands. This is not practical so we use different methods to update.

There are 4 methods of updating data in an array - pop, push, shift and unshift (shift and unshift are much less common than pop and push). Pop/push either clip off or add values to the **end of an array**, whereas shift/unshift do the same but to the **start of an array**.

**Push** will add a value at the end of an array. The push function takes one argument as shown in the example below:
```
let simple_array = ['yash','is','cool']
simple_array.push('new word')
console.log(simple_array)
```
This would return an updated array into the console - [ 'yash', 'is', 'cool', 'new word' ].

**Pop** will simply delete the value at the end of an array entirely, and does not take any arguments. See the example below:
```
let simple_array = ['yash','is','cool']
simple_array.pop()
console.log(simple_array)
```
This would return an updated array into the console - [ 'yash', 'is' ]. The last value can be kicked without knowing what the length of this array is.

**Shift** will simply delete the value at the start of an array. The shift function does not take any arguments - it isimilar to pop. See the example below:
```
let simple_array = ['yash','is','cool']
simple_array.shift()
console.log(simple_array)
```
This would return an updated array into the console - [ 'is', 'cool' ].

**Unshift** will add a value at the start of an array. The unshift function takes one argument as shown in the example below:
```
let simple_array = ['yash','is','cool']
simple_array.unshift('new word')
console.log(simple_array)
```
This would return an updated array into the console - [ 'new word', 'yash', 'is', 'cool' ].















