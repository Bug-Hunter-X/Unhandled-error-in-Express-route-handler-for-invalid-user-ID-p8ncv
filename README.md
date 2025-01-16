# Express.js Unhandled Error: Invalid User ID

This repository demonstrates a common error in Express.js route handlers: failure to handle invalid input, specifically non-numeric user IDs. The `bug.js` file contains the erroneous code, which crashes when provided with a non-numeric ID.  `bugSolution.js` provides a corrected version with robust error handling.

## Bug Description
The original code attempts to parse the user ID as an integer using `parseInt()`, but doesn't check if the parsing was successful. If the ID is not an integer, `parseInt()` returns `NaN`, leading to a crash. 

## Solution
The solution involves adding error handling to check if `parseInt(userId)` results in `NaN`.  If it does, an appropriate error response is sent, preventing the application from crashing.