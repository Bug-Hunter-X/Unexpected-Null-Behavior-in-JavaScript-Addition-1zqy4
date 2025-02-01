# Unexpected Null Behavior in JavaScript Addition

This repository demonstrates a common JavaScript quirk related to loose comparison and how null values impact addition operations.  The `foo` function attempts to add two numbers, but returns `null` if either input is `null`. This behavior might be unexpected for developers accustomed to other languages.

## Bug Description
The `foo` function uses loose comparison (`===`) which accurately identifies null values.  However, returning null prevents the addition operation from being performed when one of the arguments is null. This leads to unexpected behavior if the intent was to simply ignore null values and perform the addition when possible. 

## Solution
The solution involves explicitly checking for null values and either handling them appropriately (e.g., assigning a default value of 0), or using stricter type checking mechanisms (e.g., TypeScript) to avoid these pitfalls. 