# Async Flow Exercises

## Overview
This repository contains laboratory exercises focused on the JavaScript Event Loop. The goal is to demonstrate how JavaScript handles asynchronous execution using the Call Stack, Microtask Queue, and Macrotask Queue.

## Learning Objectives
* Understand **Synchronous vs Asynchronous** behavior.
* Identify **Microtasks** (Promises) and **Macrotasks** (setTimeout).
* Predict and explain the execution order of complex async flows.

---

## Technical Analysis: The Event Loop
One of the key challenges in this lab was predicting the output of the following code:

```javascript
console.log("A");
setTimeout(() => {
  console.log("B");
}, 0);
Promise.resolve().then(() => {
  console.log("C");
});
console.log("D");
