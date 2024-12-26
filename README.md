# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, this example shows a route that fetches a user by ID.  The code fails to handle the case where the user ID is not a valid integer, potentially leading to unexpected behavior or crashes.

## Bug

The `bug.js` file contains the buggy code.  The route handler attempts to parse the `userId` parameter as an integer without error handling. If the parameter is not a valid integer, `parseInt(userId)` will return `NaN`, causing the `users.find` method to fail silently or throw an error depending on the data structure of `users`.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes explicit error handling to check if the `userId` is a valid integer and handles the case where the user is not found.