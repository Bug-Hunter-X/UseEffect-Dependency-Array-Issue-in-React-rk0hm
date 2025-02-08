# React useEffect Dependency Array Bug

This repository demonstrates a common bug related to the dependency array in React's `useEffect` hook.  The example shows how an incomplete dependency array leads to unexpected behavior and infinite loops.  The solution provides the correct way to manage dependencies for this effect.

## Bug

The original `MyComponent` demonstrates an incorrect usage of `useEffect`.  The `count` variable is not included in the dependency array, causing the effect to run after every render, even if the `count` variable hasn't changed. This leads to unintended re-renders and excessive console logging.

## Solution

The `bugSolution.js` file shows the corrected `useEffect` hook. By including `count` in the dependency array, the effect only runs when the `count` variable actually changes, leading to the desired behavior and preventing unnecessary re-renders.