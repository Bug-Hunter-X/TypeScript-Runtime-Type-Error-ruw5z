# TypeScript Runtime Type Error

This example demonstrates a scenario where TypeScript's type system fails to catch a runtime type error, leading to unexpected behavior.

The `add` function is defined to accept two numbers, but it's called with a number and a string. While this is a type mismatch, TypeScript doesn't throw a compile-time error.  Instead, the runtime performs type coercion, resulting in NaN (Not a Number). This unexpected result can be hard to debug.

## Problem

The core issue is that TypeScript's type checking is primarily focused on compile-time safety. While it effectively detects many type errors, it doesn't guarantee the complete absence of runtime type errors, particularly when type coercion is involved.

## Solution

To prevent this issue, add explicit runtime checks to validate the input types before proceeding.  This adds redundancy but enhances robustness.

This issue highlights the importance of combining static typing with runtime checks for comprehensive error handling, especially when dealing with potentially untrusted input data.