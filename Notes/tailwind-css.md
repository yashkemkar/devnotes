# TailwindCSS

TailwindCSS is essentially a CSS framework/library that enables the user to design beautiful websites with so many wonderful effects with speed, you no longer need to manually enter every single element of CSS by yourself. You will use TailwindCSS with almost every single website design you ever do.

## How to install
TailwindCSS first requires node.js to be installed so that you can use the npm function in Terminal to actually install TailwindCSS. So below is a step by step process of how to do it. I won't include exact links because they constantly get updated with new versions

1. Install Node.js from www.nodejs.org (install with chocolatey so node packages are easier to manage in the future).
2. Search up "vite install tailwindcss" on google.
3. Create a tailwindcss starter folder somewhere on your computer and open that in terminal.
4. Run the code they list in their instructions into your terminal (using something like npm create vite@my-project). Make sure not to include any of the react stuff after.
5. Select Vanilla as your framework option to start off (but there are other frameworks you can launch with such as svelte, react, etc).
6. Select Javascript as your variant.
7. Open the folder in Visual Studio Code.
8. You can delete the .js files and ignore the public item.
9. Clear the CSS file entirely and remove the script in the HTML doc that links to the main.js one.
10. Copy the install TailwindCSS command from the website and copy it directly into your VSC terminal.
11. Then copy the npm install commands followed by the npx command.
12. For the rest just follow their instructions.
13. Once its all done, in terminal type "npm run dev".

This should return you a local host link something like this:
http://localhost:5173/

Copy that link and pasted into a browser tab - that tab/window is an open live server essentially and any changes you make to your HTML will show up as content. You need to populate it first with some content to start designing.

You have successfully launched TailwindCSS. Enjoy using it.

## How it works
Standard CSS would require us to assign a class to an item in HTML and then target that class in CSS to stylise it. However, the way that TailwindCSS works is that once the package is all set up and installed, you can configure style elements in the config file. For example you can set screen sizes, text sizes, colours etc to values such as sm, md, lg, etc. These values set to specific sizes allows some coherency and "themeness" to be present in your design as you have font-family, sizing, gaps, colour pallete, etc already set. No need to manually do it every time - this will speed up your coding.

TailwindCSS has the same functions as CSS however by setting specifics, it allows you to stylise directly in the html by entering the style into the class atrribute in the element tag. For example, if we wanted to make the body position relative and make text small size:
```
<body class="relative text-sm">
```
This would achieve those particular styles from within the HTML. TailwindCSS has its own specific settings for various styles that we must learn. However, you can now see why there may be some styles that are too difficult for Tailwind CSS.

TailwindCSS will cover 99% of design elements/choices that you could make or use, however if there is something that may be too complex for TailwindCSS then you can simply use some basic CSS in your style sheet or even as inline style in your HTML sheet with the style tags. In fact you can still create styles for classes with traditional CSS within the style tags in the head and then pull that style through the standard class = approach. Just give your element a class name, and style that class in CSS.

Some typical examples of difficult things for TailwindCSS would be things like shadows - this can be programmed easily with CSS. Also, to assign custom values (not pre-defined by either TailwindCSS or you) you must use square brackets [ ].

### General notes

TailwindCSS works really well for Mobile first design as we can set styles for different (set)screen sizes within TailwindCSS directly inside the HTML document. This would remove the need for a media query.

TailwindCSS documentation has a whole bunch of resources to help you get a better understanding of customisability options. It also has colour shades, z-index default values, so many things. They are almost all abbreviated versions of CSS, so the document library will be your best friend when designing in TailwindCSS.

Note that when you are starting out it will be hard - the IntelliSense feature for Visual Studio Code is only applicable for standard CSS, so you will not be getting auto suggestions for what to fill in. You will have to learn and remember, with time you will know most of the functions and at that point programming will be much quicker this way.

### Theme/Presets

You can also configure your tailwind.config.js file within your project folder before you start to set up a type of "theme" for yourself. You can assign hex codes to the colours, assign font families, etc. This way you can set the whole project within these parameters rather than adjusting repeatedly (it will make your code much more concise with far fewer lines.)

For example in your config file you could go to the theme section and update any of these preset colours or screeen sizes for your theme - this is particularly helpful for specific responsive design. You can also create preset theme files and import them whenever you like - this is useful for utilising older colour palettes and themes in new projects. See the code below as an example for theme:
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    screens: {
      sm: '480px',
      md: '768px',
      lg: '976px',
      xl: '1440px',
    },
    colors: {
      'blue': '#1fb6ff',
      'purple': '#7e5bef',
      'pink': '#ff49db',
      'orange': '#ff7849',
      'green': '#13ce66',
      'yellow': '#ffc82c',
      'gray-dark': '#273444',
      'gray': '#8492a6',
      'gray-light': '#d3dce6',
    },
    fontFamily: {
      sans: ['Graphik', 'sans-serif'],
      serif: ['Merriweather', 'serif'],
    },
    extend: {
      spacing: {
        '128': '32rem',
        '144': '36rem',
      },
      borderRadius: {
        '4xl': '2rem',
      }
    }
  }
}
```

### Where you should go to learn
There is no point me typing up all these notes regarding specifics of TailwindCSS because that is only useful when information is fragmented. However, TailwindCSS have an extensive document library that highlights every single function, syntax, design principles, etc. If you need any help or want to learn more about something in TailwindCSS:

https://tailwindcss.com/

Just go there and search the document library. Thats all you need! Remember, it will take time to learn all the functions and have them memorised, however as you memorise more, you will speed up and eventually be able to build beautiful websites within hours.
