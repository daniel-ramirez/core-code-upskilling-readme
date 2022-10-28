# Upskilling readme (core-code)

# Index
1. [Week 1](#week-1)
    - [Ensure Question](#ensure-question)
    - [Reversed Words](#reversed-words)
    - [Smallest Integer In Array](#smallest-integer-in-array)
    - [Odd or Even?](#odd-or-even)

## Week 1
### Ensure Question
Given a string, write a function that returns the string with a question mark ("?") appends to the end, unless the original string ends with a question mark, in which case, returns the original string.

For example (Input --> Output)

> "Yes" --> "Yes?"
> 
> "No?" --> "No?"


#### Solution
```js
function ensureQuestion(s) {
  if (!s.endsWith("?")) {
    s += "?";
  }
  return s;
}
```


### Reversed Words
Complete the solution so that it reverses all of the words within the string passed in.

Example (Input --> Output):

> "The greatest victory is that which requires no battle" --> "battle no requires which that is victory greatest The"


#### Solution
```js
function reverseWords(str){
  str = str.split(" ").reverse().join(" ");
  return str; // reverse those words
}
```


### Smallest Integer In Array
Given an array of integers your solution should find the smallest integer.

For example:

- Given `[34, 15, 88, 2]` your solution will return `2`
- Given `[34, -345, -1, 100]` your solution will return `-345`

You can assume, for the purpose of this kata, that the supplied array will not be empty.


#### Solution
```js
class SmallestIntegerFinder {
  findSmallestInt(args) {
    args.sort((a, b) => (a - b));
    return args.shift();
  }
}
```


### Odd or Even?
Given a list of integers, determine whether the sum of its elements is odd or even.

Give your answer as a string matching "odd" or "even".

If the input array is empty consider it as: [0] (array with a zero).
Examples:

> Input: [0] => Output: "even" 
>
> Input: [0, 1, 4] => Output: "odd" 
>
> Input: [0, -1, -5] => Output: "even" 

Have fun!


#### Solution
```js
function oddOrEven(array) {
  if (array.length === 0) {
    return "even";
  }
  
  const sum = array.reduce((a, b) => a + b, 0);
  const result = sum % 2;
  
  return result === 0 ? "even" : "odd";
}
```
