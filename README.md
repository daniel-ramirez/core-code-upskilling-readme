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
