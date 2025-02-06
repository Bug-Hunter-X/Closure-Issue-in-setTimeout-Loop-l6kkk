# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common error in JavaScript involving closures and the `setTimeout` function within a loop. The issue arises because the loop variable 'i' is not captured correctly for each iteration of the loop, leading to unexpected behavior.

## Problem

The provided `myFunction` aims to log the numbers 0-9 to the console after a 1-second delay for each number. However, due to the closure issue, all timeouts will log the final value of 'i' (which is 10), instead of the expected values.

## Solution

The solution involves using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop.  This ensures that each timeout captures its own unique value of 'i'.