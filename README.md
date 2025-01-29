# React useEffect Cleanup Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to clean up resources (like intervals or timeouts) in the return function. This can lead to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` uses `useEffect` to set up an interval that increments a counter every second. However, the `setInterval` function isn't cleared when the component unmounts causing the counter to continue incrementing even after the component is no longer rendered. 

## Solution
The solution involves using the return function from `useEffect` to clear the interval using `clearInterval` before the component is unmounted. 