# Express.js Unhandled Error During JSON Body Parsing

This repository demonstrates a common error in Express.js applications: unhandled errors during JSON body parsing and accessing properties of undefined objects.

## Bug
The `bug.js` file contains an Express.js application that creates a new user.  It fails to handle potential errors during JSON body parsing and accessing properties of undefined objects. If the request body doesn't contain a `name` property or if there is any issue parsing the JSON, the application will crash. 

## Solution
The `bugSolution.js` file provides a corrected version. It includes comprehensive error handling to gracefully manage situations where the request body is malformed or missing required properties.

## How to reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the required dependencies.
4. Run `node bug.js`. 
5. Send a POST request to `http://localhost:3000/users` with a JSON body that doesn't include the name property, or send a malformed JSON payload. Observe the error.
6. Run `node bugSolution.js`. 
7. Send the same POST request. Observe the improved error handling.
