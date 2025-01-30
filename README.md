# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common React coding error: omitting the cleanup function in the `useEffect` hook.  This can lead to memory leaks and unexpected behavior when a component unmounts.  The example shows a simple counter component and illustrates how to properly add a cleanup function to avoid these issues.

## Bug Description

The `useEffect` hook, without a cleanup function, keeps running even after the component is unmounted. This is typically not the desired behavior. In the example, the `console.log` statement would execute repeatedly, or even cause errors if it interacts with now-unmounted components. 

## Solution

The solution involves adding a return statement to the `useEffect` which is the cleanup function, which will be executed before the component is unmounted. 