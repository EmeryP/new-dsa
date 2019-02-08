# Big O
## Overview
* Time complexity: Big O of time allows us to formally talk about how the runtime of an algorithm grows as the input grows
* Space complexity: Big O of space allows us to formally talk about how much more space we need to allocate to run the code in our algorithm

#### Big O's Value
* To determine the better of the various algorithms that could be used to solve any problem
* Better could be...
  * Faster (time)
  * Less memory intensive (space)

#### The problems with time	
  * Different machines will record different times
  * The same machine will record different times
  * For fast algorithms speed measurements might not be accurate enough

#### Examples of calculating time
* For calculating Big O of time you can count the operations of an algorithm, i.e. +,*,/,= etc.
* Simple for loops are generally going to be simplified down to O(n) although they have multiple operations.
* Nested for loops are generally going to be an O(n2) for the nesting reason.

#### Big O Time Shorthands
* Arithmetic operations are constant
* Variable assignment is constant
* Accessing elements in an array (by index) or an object (by key) is constant
* In a loop, the complexity is the length of the loop times the complexity of whatever happens inside the loop

#### Big O Space Shorthands
* Most primitives(booleans, numbers, underfined, null) are constant space
* Strings require O(n) space where the length of the string is n
* Reference types are generally O(n), where n is the length (for arrays) or the number of keys (for objects)


#### Arrays and Objects
* Objects
  * Insertion O(1)
  * Removal O(1)
  * Searching O(n)
  * Access O(1)
  * When you dont need ordering objects are a great choice!
* Arrays
  * Insertion (it depends...)
  * Removal (it depends...)
  * Searching O(n)
  * Access O(1)

#### Resources
* [Function performance tracker](https://rithmschool.github.io/function-timer-demo/)

