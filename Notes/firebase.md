# Firebase
Firebase is a database storage platform that handles the entire backend of any front end software. So, we can use it to store profiles, authentications, data, inputs, etc. We need to link it to our React.JS application, or any other front end framework we use.

In react, context is another react hook. We normally use alot of props and send data through props, and have talked about state hierarchies. It's much easier to pass information from parent to child, and quite hard to pass information from child to parent or across componentry thats on the same level. In these scenarios, we often decide to use context. Context just gives context to our entire application - it's like a global state, it removes the need to pass the state between props. We instead create a top level overview, essentially a wrapper for our entire application. Create some stateful context in there, and then everything within that can be accessed without having to worry about passing it through props.

## Steps

1. Within the root directory of the application, we need to create a firebase.js file.

2. Within the src folder, we need to create a folder named 'context', and then within this, we need to create a jsx file  named 'AuthContext.jsx'.
