# React useEffect Hook Dependency Array Issue

This repository demonstrates a common error when using the `useEffect` hook in React: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior or stale closures.

## Bug
The `bug.js` file contains a component with a `useEffect` hook that attempts to log the current value of `count` after every render. However, it omits `count` from the dependency array, causing the effect to run only once and always use the initial value of `count` which leads to unexpected behavior.  The effect also runs again when the component unmounts but this is not what's expected from the component. 

## Solution
The `bugSolution.js` file demonstrates the correct way to use the `useEffect` hook.  By including `count` in the dependency array, the effect runs whenever the value of `count` changes, correctly logging the latest value.

## How to run
1. Clone the repo
2. Run `npm install`
3. Run `npm start`