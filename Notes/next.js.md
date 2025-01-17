# Next.JS Notes
## Introduction
Next.js is essentially the big brother to react - it incorporates react and offers more functionality. Next.js is excellent for applications that have multiple pages that need to be loaded, as it provides a sort of wrapped layout, that can be applied to every page.

## Initialising a Next.JS project
Enter the folder you want to create the project folder within through the terminal in VSCode. Run the command as below:
```
npx create-next-app@latest PROJECT_NAME
```

Then you will have a bunch of prompts come up to customise the project as you like.

This will create a folder with many different files in the project folder. 

## Reserved File Names
There are some file names within the next.js package that are known as 'reserved', which mean's there can only be one within any given folder. This means that there can only be one layout.js and page.js file in any given folder. The initialised project already comes with both of them in there. There are also some other reserved file names, that we will touch on later.

Layout.js essentially wraps the page.js and any subpages using the heirarchical approach where this main layout wraps page and any subsequent pages, unless there is a secondary layout which is specified within the subdirectory. This way we can put our Header and Footer within this function as well, and it will print thme out on every page without having to code it in every time.

## Routing
Next.js is brilliant for building multi page application, where a multi page application has a bunch of different pages. We can navigate to different pages that exist by typing them in after the url. For example:
localhost:3000/ - Home Page
localhost:3000/dashboard - Dashboard
localhost:3000/admin - Admin Page (if it exists)
localhost:3000/settings - Settings Page (if it exists)

If we tried to load dashboard, it would come up with a 404 error because it does not exist. We can create new routes in the app directory by just creating a new subdirectory with the name of the page. However, this alone won't work as we need the page.js file. So we create a new page.js file within this subdirectory /dashboard/ which doesn't violate our rule of only one page.js or layout.js file per subdirectory. 

The page.js file itself won't work, we need to program it like a react component. So we would use the following code:
```
export default function DashboardPage(){
    return(
        <div>Hello</div>
    )
}
```

Now when you navigate to the dashboard page on your browser, it will direct to the dashboard folder and look for the page.js file within there. The page will open on the browser reading "Hello".

## Components
Within Next.JS we use React components. So within the components folder, any files must be labeled in the standard convention of first letter of the name being capitalised. However, they can be given file extension of .js or .jsx. Doesn't matter which one you choose. NOTE: PRoject gave you problems for autoimporting correctly when you used .js ext, so just use .jsx.

## SSR vs. CSR
SSR components are the default setting. The way a SSR component works is that Next.js builds the server component on the server side and sends it to the browser to be rendered directly. There is no client side generation, the page is just done. It is very effecient and great for search engine optimisation, however the downside is that since it is complete prior to being rendered on the client's side, the client cant interact with it dynamically. There are no buttons, you can't change values, etc, because the page is finished.

If we want to have sections or bodies of code where we can have that level of interaction, we need to create client-side components. This is done simply by telling Next.js to 'use client' to render this component, within the component file. If we add that line to the top of the component, we will be able to use all of react's states and react hooks within our component. The components need to be CSR to use react hooks.

Most of the components we will normally create are SSR components, however some components like AuthContext.js will be CSR components. Note that client side components will not work for Search Engine Optimisation as a bot like Google will search through server side items - therefore it will not see those things. However, certain components such as those already sitting behind a wall of authentication, do not provide SEO value, so it's okay for them to be client side components.

## Application Wrapping
For certain functions like Authorisation, you will likely attribute children props to your AuthContext.jsx and then wrap the rest of the app (as children) with the AuthContext tag (like we do in React.js). However, unlike in React.js where you render the wrapper function in the index.html file, in Next.js you will wrap it in the layout.js file as the RootLayout function also wraps the whole application. See the example of the required code within the RootLayout function:
```
return (
        <html lang="en">
            <AuthProvider>
                <body className={'w-full max-w-[1000px] mx-auto text-sm sm:text-base min-h-screen flex flex-col text-slate-800 ' + opensans.className}>
                    {header}
                    {children}
                    {footer}
                </body>
            </AuthProvider>

        </html>
    )
```

## Importing Fonts & Icons
To import fonts and icons you need to create a new file in the app folder called 'head.js'
