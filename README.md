# React Native AsyncStorage: Unexpected Behavior When Accessing Data Before Retrieval

This repository demonstrates a common error in React Native when using AsyncStorage: attempting to access stored data before it has been fully retrieved.  This often leads to unexpected crashes or undefined behavior.

## Problem

The asynchronous nature of `AsyncStorage.getItem` can mask the fact that the data isn't immediately available.  If you try to use the retrieved value before the `then` block has executed, you'll encounter errors.

## Solution

Always handle the case where the data might still be `null` or `undefined`.  Use conditional rendering or checks to prevent accessing properties of a potentially null value.

## How to reproduce the bug
1. Clone this repository
2. Run `npm install`
3. Run the app using your preferred React Native method
4. Observe the error in the console when the app tries to access data before it's loaded

## How to fix the bug
1. Examine the corrected code in `bugSolution.js`
2. Implement the appropriate checks and conditional rendering in your own code to handle null or undefined values.
