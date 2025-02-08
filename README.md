# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and its dependency array. The `useEffect` hook with an empty dependency array runs after every render, leading to an infinite loop if the effect modifies state or causes re-renders.

## Bug Description

The `bug.js` file contains a component that uses the `useEffect` hook with an empty dependency array.  This causes the `console.log` statement to execute on every render, leading to a potentially infinite loop, particularly if the effect interacts with state or causes re-renders.

## Solution

The `bugSolution.js` file provides the corrected component. The `count` variable is added to the dependency array of `useEffect`.  This ensures the effect only runs when the `count` value changes, preventing the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server. 
4. Observe the console for an indication of continuous logging in `bug.js`, whereas `bugSolution.js` demonstrates the corrected behavior.