# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and missing dependencies.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current count to the console after every render. However, the `count` variable is missing from the dependency array. This leads to an infinite render loop because the effect runs on every render, causing `count` to change, which then triggers another render, and so on.

## Bug Solution

To fix this bug, the `count` variable should be included in the dependency array of the `useEffect` hook. This ensures that the effect runs only when `count` changes.

## How to reproduce the bug

1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the infinite loop in the browser's console.

## How to fix the bug

1. Clone the repository
2. Open `bugSolution.js` to see the correct code implementation.