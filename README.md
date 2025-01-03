# React Native Unhandled Promise Rejection

This example demonstrates a common error in React Native applications involving unhandled promise rejections within asynchronous functions. The issue arises when errors occurring during a network request (or other asynchronous operations) are not properly caught and handled, leading to crashes or unexpected behavior.

## Problem

The provided `bug.js` file contains a component that fetches data from an API.  If the API request fails (e.g., due to a network error or a non-2xx status code), the `catch` block isn't comprehensive enough, potentially leading to an unhandled promise rejection.

## Solution

The `bugSolution.js` file presents a corrected version with improved error handling.  Key changes:

- More robust error handling in the `catch` block.
- Clearer error messages to aid in debugging.
- Consider using a logging library for better error tracking in production environments.

## How to reproduce the bug

1. Run `bug.js`.
2. Simulate a network error (e.g., disconnect your internet). Observe the console for the unhandled rejection error.

## How to implement the solution

Replace the contents of `bug.js` with the contents of `bugSolution.js`. Rerun your application.  The application should now handle network errors gracefully.