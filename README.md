# JavaScript Floating-Point Comparison Bug

This repository demonstrates a common yet subtle bug in JavaScript related to comparing floating-point numbers using the strict equality operator (`===`).

## The Bug

The provided `foo` function aims to check if two numbers are equal. However, due to the limitations of floating-point representation, the strict equality (`===`) operator may not always produce the expected results when comparing floating-point numbers. This is because floating-point numbers are stored as approximations, and slight precision errors can occur during calculations.

For example, the expression `0.1 + 0.2 === 0.3` evaluates to `false` in JavaScript because the sum of `0.1` and `0.2` is not exactly represented as `0.3` due to floating-point precision.

## The Solution

To mitigate this issue, it's generally recommended to avoid using strict equality (`===`) for direct comparison of floating-point numbers.  Instead, use a tolerance-based comparison. The solution file provides an example of how to compare floating-point numbers within a certain tolerance.