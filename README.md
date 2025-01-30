# Express.js Route Handler Bug: Missing Error Handling for Invalid User IDs

This repository demonstrates a common bug in Express.js route handlers: the lack of proper error handling when dealing with user inputs.

## Bug Description

The provided code snippet defines a route that retrieves user data based on their ID.  However, it fails to handle cases where the provided `userId` is not a valid number.  This can result in errors or unexpected application behavior. 

## Solution

The solution includes comprehensive error handling to gracefully handle invalid `userId` values.  This involves checking if the parsed `userId` is a valid number and returning appropriate HTTP error responses for different error scenarios.

## How to Reproduce the Bug

1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `node bug.js`.
4. Send a GET request to `/users/abc` (or any non-numeric ID).  The application will likely crash or return an unexpected response.

## How to Run the Solution

1. Run `node bugSolution.js`.
2. Send a GET request to `/users/abc`. The application now returns a proper 400 error response.