# React useEffect Hook causing unnecessary re-renders

This example demonstrates a common mistake when using the `useEffect` hook in React.  The effect is placed without a dependency array, causing it to run after every render. This leads to inefficient re-renders and may clog up the console with unnecessary log messages.

The `bug.js` file shows the erroneous code. The `bugSolution.js` file provides a corrected version, where the dependency array is properly used to only run the effect when the relevant value (in this case, `count`) changes.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory containing the `bug.js` and `bugSolution.js` files.
3. Run the `bug.js` code in a React development environment.
4. Observe the excessive logging in the console.
5. Compare with the corrected `bugSolution.js` code to understand the solution.

## Solution

The key is to specify the dependency array in the `useEffect` hook.  In this case, only when `count` changes should the effect trigger. This is a crucial aspect of performance optimization in React.