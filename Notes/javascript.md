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

#### parseInt()
This one is pretty self explanatory, it allows you to take a string or array with numbers in a string data type and parse the integer out into a new array or string of data type numbers. The argument must be a numeric value inside of a string.

#### regex
Regex is a way of checking if a string or password or any regular expression contains certain characters. There are some very complicated rules for regex but you can implement this in your JS by going to chat gpt and asking it to provide some code as well as how to implement it.

### Array Methods
Arrays or lists are very important data structures and they hold a variety of different data, keeping in mind that each value has to be a valid data type. Just like the string, arrays also have a bunch of methods that can be used to manipulate data in them. The primary things we have to do with objects and arrays is follow the CRUD operations. CRUD stands for create, read, update and delete. 

This way any information stored in an array can be constantly updated in a database through user interactions. There is a certain order in which we can learn these operations.

#### Create
Creating arrays can be somewhat simple - it is only a matter of assigning empty square brackets to a variable. Quite often you will put it inside some sort of function that manipulates an existing array, so you want to write a function that takes an array as the argument. See the example below:
```
let example_array = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]
    
function arrayFilter (arr) {
    let new_array = []

    for (let i=0;arr.length;i++) {
        if (arr[i]%2!=0){
            console.log(example_array[i])
        }
    }
}
```
If we enter this in the console, it would return - 
As can be seen in the code above, we have put arr as the argument in the function that manipulates arrays - arr represents the array data type, so this sets the function to take any array as an argument in the future. 
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

Note, even if you console.log(simple_array), the console will still return a sorted one, despite only check being assigned to a sort operation. This is because the sort method actually gets applied to the simple_array itself, so once the code has been run the original array is now sorted (not just printed in a sorted order). It has actually been rearranged.

This is something to learn and get used to over time, but some methods will give you a new array that you can assign to another variable, while some will manipulates the original array *in place* and returns a reference to the same array. The intellisense can tell you which one a method does.

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

#### Delete
We may also need to delete values inside an array and there are a few ways to do that. The first way we will look at is splicing an array into two arrays that start/end next to the value we want to remove, and then joining them back together using the .concat method. See the code below:

```
let simple_array = [1,2,3,4,5]

let start_array = simple_array.slice(0,2)
let end_array = simple_array.slice(3)

let new_filtered_array = start_array.concat(end_array)
console.log(new_filtered_array)
```
This would return an updated array with the value at the 2nd index position (3) deleted from the array. The console would return - [ 1, 2, 4, 5 ]. 

However, we can make the function more flexible to remove a 3 wherever it shows up if we wanted to. The new code below shows a flexible way of programming this:
```
let simple_array = [1,2,3,4,5]

let index_of_three = simple_array.indexOf(3)
let start_array = simple_array.slice(0,index_of_three)
let end_array = simple_array.slice(index_of_three+1)

let new_filtered_array = start_array.concat(end_array)
console.log(new_filtered_array)
``` 
The console would return an array same as the one above - [ 1, 2, 4, 5 ]

If we rearranged the order of the values in the simple array to be as shown below, the new code will still work all the same. See below:
```
let simple_array = [1,4,3,2,5]

let index_of_three = simple_array.indexOf(3)
let start_array = simple_array.slice(0,index_of_three)
let end_array = simple_array.slice(index_of_three+1)

let new_filtered_array = start_array.concat(end_array)
console.log(new_filtered_array)
```
The console would return this - [1, 4, 2, 5].

### Dimensionality of arrays
#### Multidimensional arrays
So far we have learned about 1 dimensional arrays, however arrays can be multi-dimensional, we could even go to the 4th dimension with our arrays. Arrays can contain any valid data type, this means they can hold arrays within arrays, which could also be within another array. This is what it would look like:
```
let simple_array = [[[],[],[]], [[],[],[]], [[],[],[]],]
console.log(simple_array)
```
This would be printed in the console - [ [ [], [], [] ], [ [], [], [] ], [ [], [], [] ] ].

To call a value in this array you need to target the specific value within an array within another array etc. For example if we had an array within an array, we need to use two sets of [] to target a specific value. See the code below:

```
let simple_array = [[[3],[],[]], [[],[],[]], [[],[],[]],]
console.log(simple_array[0][0][0])
```
This would be printed in the console - 3

#### Loops in multidimensional arrays
We can run loops in multidimensional arrays, however our code will look a little different. What we can do is get our code to present the index locations of a value within our array as well as the value. See below for an example:
```
let simple_array = [[1, 2], [3, 4]]

for (let i = 0; i < simple_array.length; i++) {
    let subArray = simple_array[i]
    for (let j = 0; j < subArray.length; j++) {
        console.log(i, j,simple_array[i][j])
    }
}
```
This means that we are calling not only the value using simple_array[i][j] as discussed above, but we are also calling i and j themselves. This should give us the positions of each of these values as well as the values themselves. It would be printed in the console like this - 
0 0 1
0 1 2
1 0 3
1 1 4

The first column shows the position in the main array, and the second shows the position in the sub array, and the third is the actual value.

### Dictionaires/Objects

An object or a dictionary contains key value pairs and uses curly brackets for the argument. The word dictionary is actually quite an apt description because the way a dictionary works is that you look up a word and there is an attached meaning (or in this case a value) to it. Similarly a dictionary or object in programming contains a key (to describe the nature of the proceeding value) and a value (the actual value of that specific key type) attached to it.

#### Create
Creating an object/dictionary is not much different to creating anything else in JavaScript. I could create a dictionary about myself, or in otherwords a bio:

```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:`['gym', 'coding', 'reading']`
}
let name = bio['name']
console.log(name)
```
This would output 'yash' in the console. As you can see above, we need to access the key name as a string 'name'. However, we can make the code more dynamic by having another variable assigned to the key 'name', and then put the new variable as our argument. For example:

```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:`['gym', 'coding', 'reading']`
}
let name_key = 'name'
let name = bio[name_key]
console.log(name)
```

This would also output 'yash' into the console, however now it is more dynamic. 

#### Read
To search up if a key is within a bio we use a special syntax to see if the dictionary actually contains a key which follows the format 'key' in object_name within the console. The key must be in a string format because otherwise it would be treated as a variable. See the code below for an example:
```
console.log('age' in bio)
```
This would return 'true' in the console because age is present as a key in the bio. If the key wasn't there it would return 'false'.

We can also return a value within an object - all we would do is reference the index position of the value within the array and use the square bracket notation for referencing within arrays. If add this code after the main section above it would return the value we want:
```
console.log(bio.hobbies[2])
```
This would return 'reading' in the console. If the key-value pair wasnt an array, you wouldn't have any brackets, just bio.hobbies.

#### Update
Normally the const function wouldn't allow us to change a value assigned as constant, however with dictionaries, we can change values within the dictionary as long as we don't change the fact that it is a dictionary. But we can change the inside metadata. For example:

```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:`['gym', 'coding', 'reading']`
}

let name_key = 'name'
bio[name_key] = 'henry'
console.log(bio)
```
This would update the object and return the following in the console - { name: 'henry', age: 27, hobbies: "['gym', 'coding', 'reading']" }. If this key exists, it will update the key within the object, however if the key doesn't exist, it will create a new key and assign it that value. Either way, the object will be updated. See the code below:

```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading']
}

let name_key = 'name'
bio[name_key] = 'henry'

bio['number_of_friends'] = 0

console.log(bio)
```

This would return the following into the console:
  name: 'henry',
  age: 27,
  hobbies: ['gym', 'coding', 'reading'],
  number_of_friends: 0

We can make the code dynamic, but what if we knew what the key was and for certain it is in the bio. In this case we can use the dot operator to update elements in the bio quickly. See the code below:
```
bio.age = 28
console.log(bio)
```
If we run the console it will now print 28 instead of 27 (along with th rest of the original bio above). It would look like this - 
{
  name: 'henry',
  age: 28,
  hobbies: ['gym', 'coding', 'reading'],
  number_of_friends: 0
}
 This is a quick, shorthand way of manipulation the object when we know the key exists.

 #### Delete
 To remove a key value pair you just use the delete function and reference the key like we have done above - either the square brackets or the dot operator. See the code below:
 ```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading']
}

delete bio.age
console.log(bio)
```

The console would return the same object without the key age - { name: 'yash', hobbies: [ 'gym', 'coding', 'reading' ] }

#### Nested dictionaries
Dictionaries are similar to arrays, where we can have a dictionary within a dictionary. This is a more complicated data structure that contains a key known as friends that has another dictionary within it, which itself holds a key value pair. See the code below for an example:

 ```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}
console.log(bio)
```

The console would return - 
{
  name: 'yash',
  age: 27,
  hobbies: [ 'gym', 'coding', 'reading' ],
  friends: { juan: { description: 'good at maths' } }
}

If we wanted to access the description key value within the bio dictionary, we can do it in the same way we would access information in nested arrays - with subsequent [] operators. See the example below:
```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}

console.log(bio['friends']['juan']['description'])
```

This would return into the console - good at maths.

We can actually do exactly the same thing with the .operator also. For example, we can use the dot operator to change a value within nested dictionaries. If we use the same code as above, but change the bio line to . operators and change the value to 'bad at maths', it would look like this:
```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}

bio.friends.juan.description = 'bad at maths'
console.log(bio.friends.juan.description)
```
This would return 'bad at maths' into the console.

#### Loops within dictionaries
Now sometimes you may need to loop through keys within a dictionary to find something. However, loops require an indexing system, where arrays have a nice index system, you can't index the variables in a dictionary. So we have to approach it in a different way - we use a special method called Object.keys - that is going to return an array with all of the keys that are in the dictionary. **Note:** the O in Object.keys must be an uppercase O, it does not work with lowercase o. 

**Return keys**
See the example below:
```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}
const keys_in_object = Object.keys(bio)

console.log(keys_in_object)
```
This returns into the console - [ 'name', 'age', 'hobbies', 'friends' ].

**Return values**
We can do the same with values in the bio by substituting the .keys to .values. See the example below:
```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}
const values_in_object = Object.values(bio)

console.log(values_in_object)
```
If we run this through the console, we get - 
[
  'yash',
  27,
  [ 'gym', 'coding', 'reading' ],
  { juan: { description: 'good at maths' } }
]

**Return entries**
If we want to see both the key and the associated value, we can use a .entries function which will show us both. We can return entries in the console by substituting the .values to .entries. This will return an array of arrays with each key-value pair being inside an array of its own.. See the example below:
```
const bio = {
    name: 'yash',
    age: 27,
    hobbies:['gym', 'coding', 'reading'],
    friends: {
        'juan': {
            description: 'good at maths'
        }
    }
}
const entries_in_object = Object.entries(bio)

console.log(entries_in_object)
```

If we run this through the console we get - 
[
  [ 'name', 'yash' ],
  [ 'age', 27 ],
  [ 'hobbies', [ 'gym', 'coding', 'reading' ] ],
  [ 'friends', { juan: [Object] } ]
]

**Non-existent keys, values, entries**
If we try to look up a key, value or entry that doesn't exist, the console would just return undefined. To double check, we could use the 'key' in bio function to get a true/false telling us whether it exists or not.

## Scope, closures & modular code
### Global Scope vs. Local Scope
Any variable independently defined on a higher level is known to be part of the global scope, meaning that it can always be referred to at any point in the document as it is a defined variable. Whereas any variable defined within the scope of a smaller element, such as a for loop, cannot be referred to at any point in the body of code outside of the for loop.

Basically, if you define a variable outside of a function then it will have global scope, whereas if it is defined within a function by var, let or const, it will have local scope. It cannot be referred to outside of the function.

Something to be aware of is to not repeat variable names, even if local scope allows you to double up on variable names, it will just cause problems for your code.

### Closure
When we have a function inside a function as shown below:

```
function counter(){
    let count = 0

    return function() {
        count++
        console.log(count)
    }
}

let increment = counter()

increment()
increment()
```
The console will display this: 
1
2

Whats happening here is that we have a function starting with a count of 0. Inside that is what is known as an anonymous function (as it is not defined). At the end of the code we let increment invoke the counter function, whatever is left behind is effectively going to take the place off the counter function. This means that when you run increment() twice and invoke the counter function, it will remember the count outside of its local scope. A closure is formed when a function retains access to the variable count from outside its scope, even after the function has finished executing. This is known as data encapsulation.

### Modular code
We can reference all sorts of data between JavaScript files, for example functions. If we have a file with a function in it that we want to access and open a line of communication with, essentially we need to make that function modular and export the function or whatever data it is from one file so we can access it in another. For example, in we go back to the complete javascript course chapter_2.js and chapter_3.js - there was a function in chapter 2 known as the addStrings function. To access the function from chapter 2 in our chapter_3.js, we need to export the function.
```
function addStrings(string1 = 'default1', string2 = 'default2') {

let concatString = string1 + ' ' + string2
console.log(concatString)
 return concatString
}
let newString = addStrings('hello')
console.log('the new string is: ', newString)

module.exports = {
    addStrings,
    example_array
}
```
Now in the chapter 3 file if we start typing the function or array names, they show up on the intellisense. If we hit enter with the intellisense suggestion, it will automatically import addStrings as a constant into our chapter 3 file. See the code result below:
```
const { addStrings, example_array } = require("./chapter_2")
```
This line of code automatically appears at the top of our chapter_3.js file. This line of code above is known as destructuring syntax. However, it means that now addStrings and example_array is available in chapter_3.js now.

The benefit of this ability is that we can break down our JavaScript code into more bite-sized files that have more specific purposes. For example, you might have one file that is a data file, one that is a server file, or some other niche functionality. And each of these is just communicated with through the module.exports function.

### Error handling
#### Broken code
There may be times when your code does not work, it results in an error and can cause your code to break. In situations like this, where there may be something going wrong such as referencing something undefined or utilising it in a function. Broken code can cause the whole code to stop executing unless we use blocks to keep the rest of the code functioning even if one part is broken. For example, this is what broken code might look like:
```
const broken_object = {
    word:'nice'
}

function problematicCodeBlock() {
      const sub_object = broken_object.hello.world
    console.log(sub_object)
}

problematicCodeBlock()
console.log('code continued to execute')
```
With this current code, the console returns an error message and it has nothing after it. We can see there is a command to print 'code continued to execute' after the function, however the entire code just stopped and broke. To fix this, we must use a try-catch block.

#### Try-catch block
We can use something called the "try-catch" block. This is where we use a try method and then a catch method as shown below:
```
const broken_object = {
    word:'nice'
}

function problematicCodeBlock() {
    try {
        const sub_object = broken_object.hello.world
        console.log(sub_object)
    } catch(err){
        console.log(err)
    }
}
problematicCodeBlock()
console.log('code continued to execute')
```
The code above shows that there is an object with the key word with a value of 'nice'. However, we can put inside our function a try-catch block so that it doesnt just break the code. Within the try section we would put our function and within the catch section we need to put correct code, which is most often just console log the error message. Whatever we put inside the catch() brackets will be what the error is labeled, but it will always be an error. If we run that code above, the console will return:

**TypeError: Cannot read properties of undefined (reading 'world')**
    **at problematicCodeBlock**
    **(C:\Users\yashk\OneDrive\Documents\Github\the-complete-javascript-course\notes\chapter_3.js:96:48)**
    **at Object.**
    **(C:\Users\yashk\OneDrive\Documents\Github\the-complete-javascript-course\notes\chapter_3.js:103:1)**
    **at Module._compile (node:internal/modules/cjs/loader:1469:14)**
    **at Module._extensions..js (node:internal/modules/cjs/loader:1548:10)**
    **at Module.load (node:internal/modules/cjs/loader:1288:32)**
    **at Module._load (node:internal/modules/cjs/loader:1104:12)**
    **at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:174:12)**
    **at node:internal/main/run_main_module:28:49**
**code continued to execute**

As you can see above, it still prints "code continued to execute" at the end, indicating that the rest of the code was executed, despite the error.

Whenever you have some code that is temperamental at the best of times or you are fetching data from an external source and not sure about the validity of the date, or even if the response is going to be successfully met. If it is a risk point, a try-catch block can be a great contingency for your error handling.

#### Debugging
Debugging is a critical skill for a programmer, however debugging starts when you write the code. You should write the code with provisions in place to make it easier for debugging in the future. One such thing that can help is to add a console.log phrase in at the start of your try block so that you know where the code failed.
```
const broken_object = {
    word:'nice'
}

function problematicCodeBlock() {
    try {
        console.log('Attempted the try block')
        const sub_object = broken_object.hello.world
        console.log(sub_object)
    } catch(err){
        console.log(err)
    }
}

problematicCodeBlock()

console.log('code continued to execute')
```
If we entered that it would return the same error message as in the try-catch block, however with the string 'Attempted the try block' at the very start of that message. This is an indicator that the console log was executed, and then somewhere in the two lines below it the code failed, taking us to the console log error message.

Now since we did not console.log sub object, we can deduce that the error must have been in the line above with the const sub_object. This in combination with the error message should be enough information to debug.

One more thing to note is that instead of the standard console.log(err) which gives us the error message as well as the stack trace (everything below the error) as shown in the try-catch block section above. The stack trace can be a bit complex, however it can guide you as to where the problem is as it does highlight line numbers sometimes.

If we wanted we can also modify the try-catch block to get only the literal error message, without the stack trace, as shown below:
```
catch(err){
        console.log(err.message)
    }
```
The above code is just a small snippet from the larger code, but it shows the console.log(err) changed to console.log(err.message). Running the console would return:
**Attempted the try block**
**Cannot read properties of undefined (reading 'world')**
**code continued to execute**

#### Throw error
We can also generate a custom error message how we want using the throw error function. Error() is a class in JavaScript and needs to be invoked with a capital E. The code below shows an example of setting up your own error message:
```
function throwError() {
    throw new Error('custom error message')
}

throwError()
```
Running this in the console would return the entire error message with the stack trace, however the error message would be our custom one.
**Error: custom error message**
    **remaining stack trace...*

We don't throw errors that much, but try-catch is really good.

#### Guard clause
A guard clause is something used in functions to execute different logic for elements within an array or list of items. For example if integer is even continue, if integer is odd push from array, then back to even continue, etc. It runs through the whole for loop with different instructions for different integers. It is a way to filter out an array.

## Domain Object Model (DOM) and its Manipulation
The document object model is the JavaScript interactive version of an HTML document. Basically we take our HTML document and model it as an object, so that we can interact with it in JavaScript. This is no different to interacting with objects in JavaScript, except that we will be modifying in an HTML document instead and it will look different on our webpage.

### JavaScript in HTML, User events and Dynamic DOM update
Firstly the console in your browser is your best friend to see what is happening on the webpage when you assign bits of code. 

The way to edit your HTML doc is to insert JavaScript within your HTML doc's body section just before the body closing tag; you can type in regular JavaScript syntax here.

#### Targeting an element
To reference an HTML element in your script, you can use many different methods to manipulate those elements, however a very common one is .getElementById() where you can parse in the element name. This will allow you to have control over the animation/interaction with this HTML element.
```
console.log(document.getElementById('close-modal-btn'))
```
But an even better way to do this would be to assign that code to a variable as we would in classic JS:
```
let modalBtn = document.getElementById('close-modal-btn)
```
Now we can manipulate this variable through Javascript by referencing it as we normally would. To interact with any element we need to target it in our JS.

#### addEventListener
It isnt enough to just target an element, we need the action or response to occur when a particular event happens or when there is interaction with the element on the webpage. What we would use here is a method called "addEventListener", which tells the HTML element to listen for a particular event. See the example below:
```
let modalBtn = document.getElementById('open-modal-btn')
        
    function handleOpenModal() {
       console.log('button is working') 
       }

    modalBtn.addEventListener('click', handleOpenModal)
```
Now if we go to our browser console and press the 'Open Modal' button, we can see in the console that the console is printing 'button is working'. This means the event is being registered, in fact it even has a counter for the number of times an event happened.

#### getElementById
We can also actually get the button to open, or change how it displays, basically some type of animation or interaction that alters the look of it when an event occurs. If we look at the html element prior to event, we can see that it is set to display:none:
```
    <div id="modal" class="modal" style="display: none;">
        <div class="modal-content">
            <span class="close">&times;</span>
            <p>Some text in the Modal..</p>
            <button id="close-modal-btn">Close Modal</button>
        </div>
    </div>
```
We can actually target the modal specifically by using the getElementById function again:
```
 <script>
        let modalBtn = document.getElementById('open-modal-btn')
        let modal = document.getElementById ('modal')
        function handleOpenModal() {
           console.log('button is working') 
           modal.style.display = 'flex'
        }
        modalBtn.addEventListener('click', handleOpenModal)
    </script>
```
The code above now causes the button to open up an extra display below it with some text when it is clicked, making the website dynamic and interactive, and not a static page.

#### querySelector (target class or tag)
We can also target a class by using something called querySelector. For example, in this example above we modified the open modal button, yet the close modal button does not do anything yet. So we can target that using the following code:
```
    <script>
        let modalBtn = document.getElementById('open-modal-btn')
        let closeModalBtn = document.getElementById('close-modal-btn')
        let modal = document.getElementById ('modal')
        let xBtn = document.querySelector('.close')
        function handleOpenModal() {
           console.log('button is working') 
           modal.style.display = 'flex'
        }
        modalBtn.addEventListener('click', handleOpenModal)
      
        function handleCloseModal() {
            modal.style.display = 'none'    
        }
        closeModalBtn.addEventListener('click', handleCloseModal)
        xBtn.addEventListener('click', handleCloseModal)
    </script>
```
This is how we can make things functional using JavaScript. 

To target a class within a tag you need . in front of the class name to access it.

To target the tag itself, you don't need a . in front

#### createElement
We can use creatElement as a method in JavaScript to literally create a new element in the HTML file. When using the create Element you must put the html tag for the element inside the brackets, and then you can edit the variable to which it is assigned in JS afterwards. See the code below:
```
let listContainer = document.getElementById('list-container')
let newItem=document.createElement ('li')
newItem.innerText = 'New Item'
listContainer.appendChild(newItem)
```
.appendChild is the method you can use to add the new element you just created to an existing element. It will pin it to the end of the existing element.


#### Access value of text and modify in JS
If we want to be able to target text area, in this case it is an id, so we simply use getElementById:
```
let textArea = document.getElementById (text-area)
```
If we insert that text area targeting code into the button code above:
```
<script>
        let modalBtn = document.getElementById('open-modal-btn')
        let closeModalBtn = document.getElementById('close-modal-btn')
        let modal = document.getElementById ('modal')
        let xBtn = document.querySelector('.close')
        let textArea = document.getElementById ('text-area')

        function handleOpenModal() {
           console.log(textArea.value) 
           modal.style.display = 'flex'
        }
        modalBtn.addEventListener('click', handleOpenModal)
      
        function handleCloseModal() {
            modal.style.display = 'none'    
        }
        closeModalBtn.addEventListener('click', handleCloseModal)
        xBtn.addEventListener('click', handleCloseModal)
    </script>
```

### Event delegation and bubbling 
#### How to make a submit form button work without refreshing the whole page
Not sure why it was decided that way, however the default action for submitting a form is to refresh the whole page. However, this can be disruptive and can end up making the user's experience of the website quite slow, so we can submit button in a different way and cancel the default behaviour. We can still make it work on an event, ie with a click, but the way we do it is to assign an onsubmit attribute in the form open tag and set it equal to return handleSubmitForm(event) with the same event parsed into the handleSubmitForm function below in our JavaScript code. See the code below for an example:
```
    <form id="form-example" onsubmit="return handleSubmitForm(event)">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name"><br><br>
        <label for="age">Age:</label>
        <input type="number" id="age" name="age"><br><br>
        <input type="submit" value="Submit">
    </form>
    ...
    <script>
        let modalBtn = document.getElementById('open-modal-btn')
        let closeModalBtn = document.getElementById('close-modal-btn')
        let modal = document.getElementById ('modal')
        let xBtn = document.querySelector('.close')
        let textArea = document.getElementById ('text-area')
        function handleOpenModal() {
            console.log(textArea.value) 
            modal.style.display = 'flex'
            textArea.value = 'hi mum'
        }
        modalBtn.addEventListener('click', handleOpenModal)
  
        function handleCloseModal() {
            modal.style.display = 'none'    
        }
        closeModalBtn.addEventListener('click', handleCloseModal)
        xBtn.addEventListener('click', handleCloseModal)

        function handleSubmitForm (event){
            event.preventDefault()    
        }
    </script>
```
As you can see above, the form opening tag needs to have the onsubmit attribute added there with the event parsed into the function being invoked. And the same event needs to be parsed into the code for the actual function below.
 
### Dynamic page styling

#### Creating HTML directly through JavaScript
There will be times where we need to create HTML through JavaScript, for example something gets filled in one one page, and displayed as the filled in information on the next page. See the code below for how to do it:
```
let contentArea = document.getElementById('content-area')
contentArea.innerHTML = '<h1>Hi Mum </h1>'
``` 
This gets added to the top of the script section. Now when we go to the console on the browser we can see that we have actually modified the div tag and actually added in an h1 tag in the content area div. Beyond this, we can add:
```
  let newHTML = document.querySelector('#content-area h1')
    newHTML.style.background = 'yellow'
    newHTML.style.color = 'pink'
    newHTML.style.padding = '3rem'
```
This allows us to target the content area heading with a variable, and now we can repeatedly edit the variable as we want.

#### Updating a JS file to affect HTML
We can create a script tag and give it a source linked to a JavaScript file. However, the one chritical thing you need to do is to "defer" it - which means to add it last in the course of action. Here's an example of what it would look like:
```
<script src = "chapter_2.js" defer></script>
```
#### Accessing information submitted through the website
To be able to capture information from forms, we need to assign variables to the fields in the form - this can be with the rest of the 'let' variables at the top of the script section. For example:
```
let nameInput = document.getElementById('name')
let ageInput = document.getElementById('age')
```
This would allow those fields to be variables that we can control in JS. In addition to these, in the handleSubmitForm function we could put in the following:
```
console.log('name: ', nameInput.value)
console.log('age: ', ageInput.value)
```
This puts the information into an object for both name and age. Now we can do whatever we want with our form.

### JavaScript Methods
#### .innerText
This method allows you to change the text string inside a variable once you have already targeted that element in the HTML and assigned it to a variable using 'getElementByID'. For example:
```
let maintitle = document.getElementById('main-title')
maintitle.innerText = "Welcome to the DOM World"
```
This would change the text inside main-title to "Welcome to the DOM World"

## Modern OOP with classes, constructors and inheritance
This is a system that is built around classes and objects. In JavaScript a class is a template for creating an object. Some of the objects might have a key-value pair like a name and an age. Now if we want to create a skeleton or a template for creating that person in the future, we can use classes.
### Defining and instantiating classes
Lets say that we started off with an object with a key-value pair in it relating to a person such as below:
```
const person = {
    name: 'Yash',
    age: 27
}
```
Now, if we want to define this template for our person, so that we can make more people, we would use the class declaration. Note - the best practice for initialising classes is to name them with an uppercase first letter. See the example below for a class declaration:
```
class Person {
    //class body
}
const you = new Person()
```
This calls it as a method and we make a new version before we start editing it. Now this is a very simple way to call a class. 

### initialising properties with constructors
What happens if we actually wanted it to have some properties and default information? For that we can use what is known as a constructor. When we are constructing our template we might have some default values. See the example below (using the code above as well) for calling a class with default values:
```
class Person {
    //class body
    constructor (name,age){
        this.name=name; //name is a property of the class
        this.age=age; //age is a property of the class
    }
}

const cherry = new Person('Cherry', 24)
const pa = new Person('Pa, 52)
const ma = new Person('Ma', 51)

console.log(cherry)
console.log(pa)
console.log(ma)
```
The above code would return: 
Person { name: 'Cherry', age: 24 }
Person { name: 'Pa', age: 52 }
Person { name: 'Ma', age: 51 }

this.name is equal to the namethat gets parsed in as the constructor. What we have done here is that name is now a property of the class, and its the same for age. Now if we put new values into the class Person, we get a new object representing the new person by simply calling the class like a function.

### Assigning methods particular to a class
We can also define a method within the class similar to a function without having to instantiate it with the function tag. Instead we have now given every person access to this method that is instantiated within the class. See an example below:
```
class Person {
    //class body
    constructor (name,age){
        this.name=name;
        this.age=age;
    }

    greet() {
        console.log('Hello my name is ', this.name)
    }
}

const cherry = new Person('Cherry', 24)
const pa = new Person('Pa', 52)
const ma = new Person('Ma', 51)
const yash = new Person('Yash', 27)

console.log(cherry.age)
yash.greet()
```

We can call the age, and we can greet the person. The above code would print this:
24
Hello my name is  Yash.

Basically we have instantiated that using this person class will give access to the greet() method for those constants, and those constants only. This allows us to use specific functions in specific scenarios.

### Understand the prototype chain and how objects inherit properties and methods
We can also create new classes that inherit properties of prior classes. This is useful when you already have information like a person's details, and you want to assign something else to them as a key value pair. For example, if we wanted to assign a favourite videogame we can create another class that extends the person class. See the example below (continued on from above code relating tot he Person class):
```
class Person {
    constructor (name, age){
        this.name = name
        this.age = age
    }
}
class Gamer extends Person {
    constructor(name, age, videogame){
        super(name, age)
        this.videogame = videogame
    }
}

const nerdyGuy = new Gamer('Ash', 10, 'Pokemon')
console.log(nerdyGuy)
```
The console prints - Gamer { name: 'Ash', age: 10, videogame: 'Pokemon' }.
This way we can define all of these templates that are dependent on all of these other templates. It means that as we instantiate new versions of the object, it can be so much easier to just define a new Gamer off the Person class, rather than writing out a whole new object with all the key value pairs.

This process above is called Inheritance. When a new class inherits the template of a parent class, and when we define a new version that is called instantiation.

### Getters and setters
It's pretty self-explanatory, but a getter is to get the information and setter is to set the information, and they are methods that we define within a class. A common practice is for the entity within the class to have an underscore in front of the name and then we assign the name. We can then define the get name method (keyword get in front of it). See the example below:
```
class MyClass {
    constructor(name) {
        this._name = name
    }

    get name(){
        return this._name
    }

    set name(value){
        this._name = value
    }
}

const obj = new MyClass('Moksh')
console.log(obj)
```
This would return: {_name: 'Moksh'}

These methods as shown above are specifically for retrieving and updating new properties with the instantiated class. As shown above we can instantiate a new version of MyClass as shown above. The console.log above returns the class itself as an object, we can also return just the name within the object as we normally would:
```
console.log(obj.name)
```
The above would return 'Moksh'.

To update the value of name, we could just assign a new value to obj.name if we parse in a value as the set name function takes an input as a value and will change the name to the new value. See an example shown below:
```
obj.name = 'Pranav'
console.log(obj.name)
```
This would then update the name and return - Pranav.


### The 'this' keyword
Now, getters and setters look like functions, but are technically not necessary:
```
nerdyGuy.videogame = 'League of Legends'
console.log(nerdyGuy)
```
This would also return an updated value for the game:
Gamer { name: 'Ash', age: 10, videogame: 'League of Legends' }

However, the benefit of using getters and setters is that we can intercept the update with logic in the middle. For example when a new value gets updated we can add in logic of console.log('Fetched new name') in between, where we would not be able to do that by directly accessing the value in an object as shown with the nerdyGuy code above. All we can do with the above syntax is change the value we cannot console.log the new value. However in the case, as shown below, we can console.log the new value within the same code:
```
class MyClass {
    constructor(name) {
        this._name = name
    }

    get name(){
        console.log('Fetched current name')
        return this._name
    }

    set name(value){
        this._name = value
    }
}

const obj = new MyClass('Moksh')
console.log(obj.name)

obj.name = 'Pranav'
console.log(obj.name)
```
This would return:
Fetched current name
Moksh
Fetched current name
Pranav

### Order of operations
With a function we can define a function further down the document and access it near the top, however with a class you can only instantiate the class after the class has already been defined above.





