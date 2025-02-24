# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code attempts to parse a user ID from a route parameter without verifying that it's a valid integer. This can lead to unexpected behavior or crashes if the ID is not a number.

## Bug

The `bug.js` file contains the buggy code.  It attempts to find a user based on an ID passed as a route parameter. However, it doesn't handle the case where the ID is not a number, causing a potential error.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes input validation to ensure the ID is a number before attempting to parse it.  If the ID is invalid, it returns a 400 Bad Request response.  It also handles the case where no user is found with the given ID, returning a 404 Not Found response.