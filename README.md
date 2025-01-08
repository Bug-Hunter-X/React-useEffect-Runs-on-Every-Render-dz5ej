# React useEffect Runs on Every Render

This repository demonstrates a common issue with the React `useEffect` hook: unnecessary re-renders due to missing dependency arrays.

The `bug.js` file shows an example of `useEffect` running on every render. The `bugSolution.js` file shows how to fix this by correctly specifying the dependencies array.

## Bug

The `useEffect` hook in `bug.js` doesn't include a dependency array. This causes it to run after every render, potentially causing performance problems and unexpected behavior.

## Solution

The `bugSolution.js` file demonstrates the corrected implementation. By including `[count]` as a dependency array, `useEffect` only runs when the value of `count` changes.