# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook causing an infinite render loop.  The example shows a simple counter component where the `useEffect` hook is incorrectly used, leading to excessive re-renders and console spam.

## Bug Description

The `useEffect` hook in the `MyComponent` function runs after every render.  Because it doesn't have any dependencies, it triggers a re-render every time the component updates. This creates a cycle: the component renders, the effect runs, the component re-renders, and so on.

## Solution

The solution is to add a dependency array to the `useEffect` hook.  This ensures that the effect only runs when the specified dependencies change.

## How to reproduce

1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the infinite logging in your browser's console.

## How to fix

Review the solution file for the correct implementation using the dependency array to fix the infinite loop.