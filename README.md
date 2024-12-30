# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrectly configured dependency array, leading to an infinite render loop. 

## Bug Description
The `useEffect` hook is used to perform side effects after every render. However, if the dependency array is missing or incorrectly specified, it can cause the effect to run repeatedly, creating an infinite loop.  This example shows an infinite loop caused by omitting `count` from the dependency array.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the continuous logging in your browser's console and the rapidly incrementing counter, indicating an infinite loop.

## Solution
The solution involves correctly specifying the dependency array to include all variables used within the `useEffect` callback that change between renders.