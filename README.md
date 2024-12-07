# React Component Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug Description

The `MyComponent` component uses `setInterval` to update the count every second. However, it fails to clear the interval when the component unmounts.  This means that the interval continues to run even after the component is no longer visible, leading to a memory leak.

## Bug Solution

The solution involves using the return value of `useEffect` to clear the interval before the component unmounts. This ensures that the interval is properly cleaned up, preventing memory leaks.