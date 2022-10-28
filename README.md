# Upskilling readme (core-code)

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
