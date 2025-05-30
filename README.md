# Kotlin for algorithm interviews

## Content here

This repository contains the Kotlin 5-minute cheat sheet of APIs, which will be helpful during algorithm interviews. You can revise it right before the interview or during preparation.

Almost every company allows you to use Kotlin for their coding interviews, where you solve leetcode-like problems. However, the API you use in production code and the necessary API during an interview may differ. Do you remember how to check whether a char is a letter or a digit? These and other useful APIs are listed below.

## Contribution

The repository is open to contribution. To add the API, fork the repo and create a PR to the main branch. Please note the following:
- You are welcome to make a contribution
- We keep it simple and concise so that you can look over it in 5 minutes

## Cheatsheet

### Char
```kotlin
// Code value - chat.toInt() returns the same, but it is deprecated
val code = char.code
// Digit value
val digit = char.digitToInt() // digitToIntOrNull() for nullable result

// Char type
val isDigit = char.isDigit()
val isLetter = char.isLetter()

// Letter case
val isUpperCase = char.isUpperCase() // isLowerCase()
val upperCase = char.uppercaseChar() // uppercase() which returns String
```

### String
```kotlin
val length = string.length // not size
val substring = string.substring(from, to) // [from, to) - from inclusive, to exclusive
val split: Array<String> = string.split(":", ",", "-")
val join = arrayOf("abc", "dfg", "123").joinToString(separator = ", ", prefix = "", postfix = "")
val replaced = "abc123abc".replace("ab", "qw") // -> "qwc123qwc"
```

### Indexing
```kotlin
val first = list.first() // works with List, Array, String
val last = list.last()

val lastIndex = list.lastIndex // works with List, Array, String

for (item in list) {} // works with List, Array, String
for ((index, item) in list.withIndex()) {}
for (index in 0 until list.size) {} // alternatives 0..list.lastIndex or list.indices
for (index in 5 downTo 0) {} // 5 4 3 2 1 0
for (index in list.indices.reversed()) {} // reversed indexing
```

### Array
```kotlin
val array = arrayOf(1, 2, 3)
val array = Array<Int>(3) { i -> i } // 1, 2, 3
val array: Array<Int?> = arrayOfNulls(3) // null null null
val list = array.toList()
val array = list.toTypedArray()
val intArray = IntArray(3) // 0 0 0 - primitive int array
```

### Map
```kotlin
val map = mutableMapOf<String, Int>()  // returns LinkedHashMap, maintains insertion order
val hashMap = HashMap<String, Int>() // returns HashMap, not maintains insertion order

val default = map.getOrDefault("key", 0)
```

### List
```kotlin
// Be careful when you need mutable and immutable lists
val list = listOf(1, 2, 3) // immutable
val mutableList = mutableListOf(1, 2, 3) // mutable

// Most operations similar for mutable and immutable,
// but one in-place and other returns new list.
// Operation names differ by d/ed ending.
val reversed = list.reversed()
mutableList.reverse() // in-place
```

### Sort
```kotlin
mutableList.sort() // min to max
mutableList.sortByDescending() // max to min
mutableList.sortBy { it * it } // min to max by expession
studens.sortWith(
  compareBy { it.grade }
  .thenByDesceding { it.name }
) // min to max with comparator
``` 

### Stack
```kotlin
// There are many alternatives like LinkedList,
// but ArrayList allows easy postprocessing with random access
val stack = mutableListOf<Int>()
stack.add(0)
val topPop = stack.removeLast() // removeLastOrNull() do not throws NoSuchElementException
val topElement = stack.last()
```

### Queue
```kotlin
val queue = LinkedList<Int>()
queue.offer(0) // adds to the tail
val next = queue.poll() // removes from the head and returns
val nextPeek = queue.peek() // only returns from the head
```

### Priority queue
```kotlin
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

