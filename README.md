# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook:  forgetting to include dependencies in the dependency array, leading to an infinite render loop.

The `bug.js` file shows the incorrect implementation. The `bugSolution.js` file provides the correct implementation.

## Bug Description
The `useEffect` hook is designed to perform side effects.  If you forget to list the variables it depends on in the second argument (dependency array), React will run this effect on every render.  If the effect itself changes a state variable that triggers re-rendering, you get an infinite loop. 

## Solution
Ensure you include all state variables or other values the effect depends on in the dependency array.