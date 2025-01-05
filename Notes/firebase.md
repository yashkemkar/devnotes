# Firebase
Firebase is a database storage platform that handles the entire backend of any front end software. So, we can use it to store profiles, authentications, data, inputs, etc. We need to link it to our React.JS application, or any other front end framework we use.

## AuthContext.jsx
We need to create a folder within our src folder called "context", and within that a file called AuthContext.jsx.

In react, context is another react hook. We normally use alot of props and send data through props, and have talked about state hierarchies. It's much easier to pass information from parent to child, and quite hard to pass information from child to parent or across componentry thats on the same level. In these scenarios, we often decide to use context. Context just gives context to our entire application - it's like a global state, it removes the need to pass the state between props. We instead create a top level overview, essentially a wrapper for our entire application. Create some stateful context in there, and then everything within that can be accessed without having to worry about passing it through props.

## Steps

1. Within the root directory of the application, we need to create a firebase.js file.

2. Within the src folder, we need to create a folder named 'context', and then within this, we need to create a jsx file  named 'AuthContext.jsx'.

3. Create a new project in Firebase.

4. Install the firebase package using node.js

5. Create a .env file to store the secret keys.

6. Copy the SDK code from firebase and put it in your firebase.js file and copy over the information to your .env also (so the keys are there).

7. Change keys in your firebase.js folder to the capitalised version such as:
apiKey: import.meta.env.VITE_FIREBASE_APIKEY,

8. Import Authentication and Firestore (database) services into the firebase.js file.

9. Export a constant variable called auth and db to export your authentication service and database service.

10. Then you need to set the same services up in the firebase console online.

## Authentication
There are many different types of Authentication that are possible to use within your app. Spend some time looking over this - perhaps you can incorporate a facebook sign in, or a google sign in to get into your app. That would be a pretty cool feature to include.


## Database
The databse thats created is essentially a massive object - you have collections (key name) and documents (value) which are the values associated with them. You can have nested collections within documents, etc.

Within the database setup, you have to configure the rules for reading/writing data stored within the database. There is already some boiler plate code, but you need to add the following code in to make sure that the user can only read/write data that matches with their own user id. See the code below:
```
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
    	allow read, write: if false;
    }    
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
  	}
  }
}
```