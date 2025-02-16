# React useEffect setInterval Memory Leak
This repository demonstrates a common error in React components: a memory leak caused by the improper use of `setInterval` within the `useEffect` hook.

The `bug.js` file showcases the problematic code.  The `setInterval` function is used to update a counter every second. However, it lacks a cleanup function to clear the interval when the component unmounts. This results in the interval continuing to run indefinitely, even after the component is no longer needed, leading to a memory leak.

The `bugSolution.js` file provides the corrected version with the necessary cleanup function using `clearInterval` within the return statement of the `useEffect` hook. This ensures the interval is properly cleared when the component is unmounted, preventing memory leaks and improving the application's performance and stability.