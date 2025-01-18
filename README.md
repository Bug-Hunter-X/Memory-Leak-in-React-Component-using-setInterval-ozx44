# React setInterval Memory Leak

This repository demonstrates a common React coding error involving the `setInterval` function within a `useEffect` hook without proper cleanup. This leads to a memory leak because the interval continues to run even after the component is unmounted.

## Problem

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function in the `useEffect` hook to stop the interval when the component is unmounted. This results in the interval continuing to run in the background, consuming resources and potentially leading to performance issues.

## Solution

The `bugSolution.js` file provides a corrected version of the component. It uses the return value of `useEffect` to implement a cleanup function that clears the interval when the component unmounts, preventing the memory leak.