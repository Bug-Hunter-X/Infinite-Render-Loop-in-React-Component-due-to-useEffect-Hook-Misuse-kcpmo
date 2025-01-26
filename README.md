# React Infinite Render Loop Bug

This repository demonstrates a common bug in React applications: an infinite render loop caused by improper use of the `useEffect` hook.  The `MyComponent` attempts to increment the count state within the `useEffect`'s dependency array, leading to continuous re-renders.

## Bug Description

The bug lies in the `useEffect` hook.  The `setCount` function is called inside the effect, causing an infinite loop as the state changes, triggering the effect to run again, and so on.

## Solution

The solution avoids the infinite loop by removing `count` from the dependency array or by using a conditional update to prevent infinite loops.