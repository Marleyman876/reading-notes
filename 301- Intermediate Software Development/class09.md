# Refactoring JavaScript

Refactoring code is making it more readable and in some cases shorter wihtout changing its functioanlity. For example a function can be refactored from: 

```
const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;
}

Refactored Code: 

const URLstore = new Map(); // Change this to a Map

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  // Place the short URL into the Map as the key with the long URL as the value
  URLstore.set(rndName, URL);
  return rndName;
}
```
the refactored code does the same functionality as the code above but it is less "wordy".

Reference:

[Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa).

[Refactoring JavaScript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readabili.