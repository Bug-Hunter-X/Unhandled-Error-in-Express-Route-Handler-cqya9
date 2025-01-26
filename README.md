# Unhandled Error in Express Route Handler

This repository demonstrates a common error in Express.js applications: failing to handle potential errors in route handlers.  Specifically, the example shows a route that fetches user data based on an ID but doesn't gracefully handle cases where the ID is invalid or the user doesn't exist.

## Bug

The `bug.js` file contains the flawed code. The route handler `/users/:id` attempts to access user data using `req.params.id`, but it does not handle the scenario where `req.params.id` might be invalid or missing, leading to potential errors and unexpected behavior.

## Solution

The `bugSolution.js` file provides a corrected version.  It includes error handling to check if the `userId` is valid before attempting to fetch user data.  If the ID is invalid, it sends an appropriate error response to the client.