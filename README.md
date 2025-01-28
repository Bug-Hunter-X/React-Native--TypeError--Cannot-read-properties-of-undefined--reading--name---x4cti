# React Native: TypeError: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common error in React Native applications: `TypeError: Cannot read properties of undefined (reading 'name')`. This error arises when you attempt to access a property of an object that is currently undefined or null.  This frequently happens when dealing with asynchronous operations like fetching data from an API.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version that effectively handles potential null or undefined values.

## Problem

The error stems from accessing `this.state.data.name` before the API call has finished and populated `this.state.data` with data.  Accessing a property of `null` or `undefined` causes the error.

## Solution

The solution involves adding checks to ensure `this.state.data` is not null or undefined before accessing its properties.  Optional chaining (`?.`) and the nullish coalescing operator (`??`) are effective ways to address this.

## How to run

1. Clone the repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app on an emulator or device.