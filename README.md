# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` is intended to log a message to the console each time the component renders. However, because the `count` variable is not included in the dependency array, the effect runs on every render, causing `setCount` to be called continuously, leading to an infinite re-render loop.

## Solution

The `bugSolution.js` file corrects this by adding `count` to the dependency array. This ensures the effect only runs when the `count` variable changes.