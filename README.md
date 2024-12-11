# React useEffect Runs on Every Render
This repository demonstrates a common mistake in using the `useEffect` hook in React where the effect runs on every render, even when an empty dependency array is provided.  This can lead to performance issues and unexpected behavior.

The `bug.js` file contains the erroneous code, while `bugSolution.js` demonstrates the correct implementation.

## Problem
The `useEffect` hook with an empty dependency array is intended to run only once after the initial render. However, the example in `bug.js` incorrectly shows that this doesn't always occur.  This often happens if a value within the component that is referenced in a callback function gets changed on every render.