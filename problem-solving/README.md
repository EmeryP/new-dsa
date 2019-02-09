# Problem Solving

## Devising a Plan

### Understand The Problem
* Restate the problem in your own words
* What are the inputs to this problem?
  * Ask the important questions regarding the inputs. A function that adds two numbers might appear simple but it's important to think about the different types of numbers you might be adding, what size they'll be as JS has issues adding very large numbers, i.e. 1^300 zeros. Bottom line, dont make assumptions about the inputs or anything else.
* What are the outputs that should come from the solution to the problem?
* Can the outputs be determined directly from the inputs? Meaning do I immediately have enough information to solve this?
* How should I label the important pieces of data that are part of this problem?

### Explore Concrete Examples
* Write down a few simple examples of inputs and outputs then progress to more complex examples. 
* Explore examples with empty and invalid inputs.
* User stories, unit tests are good things that can guide you through the problem solving process.
### Break It Down
* Explicity write down the steps/algortihm you'll take to solve this problem in pseudocode or other format

### Solve/Simplify
* Identify the core difficutly in what you're trying to do
* Temporarily ignore that difficulty
* Write a simplified solution
* Then incorporate that difficulty back in

### Look Back And Refactor
* Refactoring questions
  * Can you check the result?
  * Can you derive the result differently?
  * Can you understand it at a glance?
  * Can you use the result or method for some other problem?
  * Can you improve the performance of your result?
  * Can you think of other ways to refactor?
  * How have other people solved this problem?


## Problem Solving Patterns

### Frequency Counter
* This pattern uses objects or sets to collect values/frequencies of values
* Operations to handle frequencies of values in arrays
  * Remove element from array
  * Store index of element in secondary array
  * Break down an array or string into an object and instead of using nested loops you can then use loops to simply compare the two objects
* Below is an example of using a frequency counter method to compare the values and frequency of values in arr1 to arr2. O(n) solution for time.

```
function compareArr(arr1, arr2) {
  if (arr1.length !== arr2.length) {
    return false;
  }
  let counter1 = {}
  let counter2 = {}
  for (let val of arr1) {
    counter1[val] = (counter1[val] || 0) + 1
  }
  for (let val of arr2) {
    counter2[val] = (counter2[val] || 0) + 1
  }
  console.log(counter1)
  console.log(counter2)
  for (let key in counter1) {
    if (!(key ** 2 in counter2)) {
      return false;
    }
    if (counter2[key ** 2] !== counter1[key]) {
      return false
    }
  }
  return true
}

compareArr([1,2,3,4], [16,4,9,1])
```
* Code to check if string is anagram using frequency counter method
```
function isAnagram(str1, str2) {

  // solve for base case (strings that are not the equivalent length)
  if (str1.length !== str2.length) {
    return false;
  }
  // define object used to map input strings
  let storageObj1 = {}
  let storageObj2 = {}

  //store values of str1 to storageObj1
  for (let val of str1) {
    storageObj1[val] = (storageObj1[val] || 0) + 1
  }
  //store values of str1 to storageObj1
  for (let val of str2) {
    storageObj2[val] = (storageObj2[val] || 0) + 1
  }
  //compare storageObj1 & storageObj2
  for (let key in storageObj1) {
    //does key's value exist in storageObj2
    if (!(key in storageObj2)) {
      return false;
    }
    //do keys in both objs have the same value/count
    if (!(storageObj1[key] === storageObj2[key])) {
      return false;
    }

  }
  // return true if all conditions pass
  return true;
}

isAnagram('carr', 'rcac')  //false scenario
isAnagram('carr', 'rca')  //false scenario
isAnagram('carr', 'rcat')  //false scenario
isAnagram('carr', 'rcar')  //true scenario
```
### Multiple Pointers
### Sliding Windows
### Divide and Conquer
### Dynamic Programming
### Greedy Algorithms
### Backtracking

