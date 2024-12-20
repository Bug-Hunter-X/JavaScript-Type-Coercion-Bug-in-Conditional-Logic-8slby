# JavaScript Type Coercion Bug
This repository demonstrates a subtle bug in JavaScript code that arises from loose comparison and type coercion. The code appears to correctly handle null and negative numbers, but it fails when dealing with negative numbers represented as strings.

## Description
The `foo` function aims to classify numbers as 0, -1, or 1 based on their value. However, due to JavaScript's loose comparison (`==`), the condition `x < 0` implicitly coerces the input `x` to a number if it's a string, resulting in unexpected behavior when the input is a string representation of a negative number.

## How to Reproduce
1. Clone this repository.
2. Run `bug.js` using a JavaScript runtime (like Node.js).
3. Observe the incorrect output for string input of '-1'.

## Solution
The solution employs strict equality (`===`) to prevent type coercion and ensure accurate comparisons. This guarantees the correct classification of numbers regardless of their type.