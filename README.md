# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React performance issue involving the `useEffect` hook. The provided `MyComponent` uses `useEffect` without specifying dependencies, leading to unnecessary re-renders and potential performance bottlenecks.

## Bug
The `useEffect` hook in `bug.js` runs after every render of the component because it lacks a dependency array. This causes the console log to appear repeatedly and impacts performance, especially with more complex components.

## Solution
The `bugSolution.js` demonstrates the correct usage of `useEffect`. By adding the `count` variable as a dependency, the effect now runs only when the `count` value changes.