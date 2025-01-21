# Sveltekit Notes

## What is Sveltekit?
Sveltekit is another Javascript framework that can be used to quickly create dynamic and elegant websites.

## Routes
Routes folder that is the route based navigation system. The "home route" or "base level root route" is the +page.svelte that is then rendered inside the the +layout.svelte. This is similar to the way that Next.js works, where the page.js and layout.js are the higher level global files that are used repeatedly for different pages on the website, and get rendered within our app.html.

## Components
Svelte also has components the same as React or Next.js. Similar to react, it has a 'src' folder within the main folder, and within that src folder we have a 'components' folder. The components within here are similar to react, where the name of the component needs to have a capitalised first letter, however the file extension is .svelte.

### Exporting components
To pass a prop between components we need to use something called export. "Export let y;" is essentially receiving the prop from another file. And then to pass it, in the file that the prop exists, we must parse it into the invoked version of that file (similar to how we do in react).

### slot
The slot component is the thing that goes in the middle in between the header and footer. Item's are put into the page through the slot.

## Syntax differences
Of course there will be some syntax differences for frameworks like Svelte. These are in no particular order, but as they come up. And I will point it out if HTML or CSS is different, but also if JS is different from react JS.

### onClick
In react we use the onClick function that takes an arrow function as an argument, however the syntax here is different, see below for the syntax:
```
on:click = {goTop}
```
So the difference here is how the 'on click' element is written. 

### Mapping out items
We can map out items for example if we want pokemon cards to show up and we have heaps of them in an object, or say projects we have done, anything. The mapping function works the same way as we normally do in JavaScript, it just goes through each value in the array following the index. So the function also takes two arguments - the value and the index. We can map out using special syntax from Svelte as shown below:
```
{#each tabs as tab,index}

{/each}
```
In the example above - #each is the mapping function (both opening brace tag and closing brace tag), the array is tabs, each value in there is referred to as tab, and the index is the index. 

