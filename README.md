# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by an infinite loop resulting from a missing dependency in the `useEffect` call.

## Bug Description

The `MyComponent` component uses `useEffect` to update the `count` state. However, because `count` is not included as a dependency, the effect runs continuously, causing an infinite loop and potentially crashing the application.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the continuously increasing `count` value in the browser console and the browser's performance degradation.

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` call, ensuring the effect only runs when these dependencies change. 