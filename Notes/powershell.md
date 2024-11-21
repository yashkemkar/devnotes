# PowerShell Notes

Powershell is the language that runs your whole Windows system, it is the language that is currently in the terminal below that you enter commands into for the code to get executed. There are many things you can do and need to do using PowerShell.

## Check node.js version
To check your node.js version number go into your terminal and type in the following code
```
node -v
```
This should give you a standard version number for node.js.

## npm
npm is short for Node Packet Manager - this is typically for supplementary files that you add to your JavaScript code that are utilised within its execution. These files will have code and parameters set that are needed for your main script hence the term "packet". The node packet manager is a software that is utilised to incorporate these JSON files into your program.

## Check npm version
To check your npm version number go into your terminal and type in the following code
```
npm -v
```
This should give you a standard version number for npm.

Sometimes you may have a problem with an error showing up saying that "npm.ps1 cannot be loaded because running scripts is disabled on this system". If this happens, open Windows PowerShell as an administrator and enter in the following code:
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
This should allow npm to run now.

## Initialising a package file
If you want to add external packages then you need a package.JSON file - a JSON is a form thats pretty similar to an object. Now, in the terminal, we need to initialise the file using the code below:
```
node init -y
```
This is going to create the package.JSON file in the root directory of our project.

## Executing a JSON file within the console
Within this package file you can actually insert code within the "scripts" section of a JSON file to be executed, for example:
```
    "console": "node notes/chapter_7.js"
```
The console line is the only line I added to the original JSON, but if I then go to the terminal and type in 'npm run console' it will run the argument within the console - which is our chapter_7.js file. All the code within that file will get executed through the console.