# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications where an infinite loop occurs within the `useEffect` hook. The bug arises from incorrectly updating state within the dependency array, leading to continuous re-renders and an infinite loop.

## Bug Description
The `useEffect` hook is used to perform side effects after rendering. However, when the state update within the `useEffect` causes the component to re-render, triggering the `useEffect` again, it leads to an infinite loop. 

## Solution
The solution involves ensuring that the state update does not trigger a re-render within the `useEffect` hook itself. This can be achieved by using a functional update or by ensuring the dependency array correctly manages the updates.