# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file contains code that attempts to find a user by ID but doesn't handle cases where the ID is not a number or the user is not found.  The `bugSolution.js` file provides a corrected version with proper error handling.

## Bug

The original code lacks error handling for scenarios where `req.params.id` is not a valid integer or if no user with the provided ID exists. This could lead to unexpected behavior or application crashes.

## Solution

The solution includes comprehensive error handling to address invalid input and missing users gracefully.  It checks for the existence of the user and uses appropriate HTTP status codes (400 for bad request and 404 for not found).