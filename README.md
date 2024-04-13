# Kotlin for algorithm interviews (In Progress - Join to Contribute)

## Content here

This repository contains the Kotlin 5-minute cheat sheet of APIs, which will be helpful during algorithm interviews. You can revise it right before the interview or during preparation.

Almost every company allows you to use Kotlin for their coding interviews, where you solve leetcode-like problems. However, the API you use in production code and the necessary API during an interview may differ. Do you remember how to check whether a char is a letter or a digit? These and other useful APIs are listed below.

## Contribution

The repository is open to contribution. To add the API, fork the repo and create a PR to the main branch. Please note the following:
- You are welcome to make a contribution
- We keep it simple and concise so that you can look over it in 5 minutes

## Cheatsheet

```Kotlin
// Char

// Code value - chat.toInt() returns the same, but it is deprecated
val code = char.code
// Digit value
val digit = char.digitToInt() // digitToIntOrNull() for nullable result

// Char type
val isDigit = char.isDigit()
val isLetter = char.isLetter()

// Letter case
val isUpperCase = char.isUpperCase()
val upperCase = char.uppercaseChar() // or uppercase() which returs String
val isLowerCase = char.isLowerCase()
val lowerCase = char.lowercaseChar() // or lowercase() which returns String
```

## Practice

Practice makes it perfect. You can solve the following Leetcode problems covering the cheat sheet APIs.

| Problem | Labels |
| --- | --- |
| TBD | TBD |
