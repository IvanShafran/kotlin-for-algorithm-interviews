# Kotlin for algorithm interviews (In Progress - Join to Contribute)

## Content here

This repository contains the Kotlin 5-minute cheat sheet of APIs, which will be helpful during algorithm interviews. You can revise it right before the interview or during preparation.

Almost every company allows you to use Kotlin for their coding interviews, where you solve leetcode-like problems. However, the API you use in production code and the necessary API during an interview may differ. Do you remember how to check whether a char is a letter or a digit? These and other useful APIs are listed below.

## Contribution

The repository is open to contribution. To add the API, fork the repo and create a PR to the main branch. Please note the following:
- You are welcome to make a contribution
- We keep it simple and concise so that you can look over it in 5 minutes

## Cheatsheet

### Char
```Kotlin
// Code value - chat.toInt() returns the same, but it is deprecated
val code = char.code
// Digit value
val digit = char.digitToInt() // digitToIntOrNull() for nullable result

// Char type
val isDigit = char.isDigit()
val isLetter = char.isLetter()

// Letter case
val isUpperCase = char.isUpperCase() // isLowerCase()
val upperCase = char.uppercaseChar() // lowercaseChar() or uppercase() / lowercase() which returns String
```

### String
```Kotlin
val length = string.length // not size
val substring = string.substring(from, to) // [from, to) - from inclusive, to exclusive
val split: Array<String> = string.split(":", ",", "-")
val join = arrayOf("abc", "dfg", "123").joinToString(separator = ", ", prefix = "", postfix = "")
```

### Indexing
```Kotlin
val first = list.first() // works with List, Array, String
val last = list.last()

val lastIndex = list.lastIndex // works with List, Array, String

for (item in list) {} // works with List, Array, String
for ((index, item) in list.withIndex()) {}
for (index in 0 until list.size) {} // alternatives 0..list.lastIndex or list.indices

```

```Kotlin
// Array


```

```Kotlin
// Map

getOrDefault()
```

### List
```Kotlin
// Be careful when you need mutable and immutable lists
val list = listOf(1, 2, 3) // immutable
val mutableList = mutableListOf(1, 2, 3) // mutable

// Most operations similar for mutable and immutable, but one in-place and other returns new list.
// Operation names differ by d/ed
val sortedList = list.sorted() // sorts from min to max
mutableList.sort() // in-place sort

sortBy

sortWith (comparator and thenBy)

find / filter / map / reverse ?
``` 

### Stack
```Kotlin
// There are many alternatives like LinkedList, but ArrayList allows easy postprocessing with random access
val stack = mutableListOf<Int>()
stack.add(0)
val topPop = stack.removeLast() // removeLastOrNull() do not throws NoSuchElementException
val topElement = stack.last()
```

### Queue
```Kotlin
val queue = LinkedList<Int>()
queue.offer(0) // adds to the tail
val next = queue.poll() // removes from the head and returns
val nextPeek = queue.peek() // only returns from the head
```

### Priority queue
```Kotlin
val priorityQueue = PriorityQueue<Int>() // head is the least element
priorityQueue.offer(0) // adds to the tail
val next = priorityQueue.poll() // removes from the head and returns
val nextPeek = priorityQueue.peek() // only returns from the head
```

### Bit manipulation - different from Java

Simple operators - `and`, `or`, `xor`

Not - `value.inv()`

Shifts - `shl` (signed shift left), `shr`, `ushr` (unsigned shift right)

## Practice

Practice makes it perfect. You can solve the following Leetcode problems covering the cheat sheet APIs.

https://www.techinterviewhandbook.org/grind75

