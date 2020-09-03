# Class 01 Readings (Sept. 3rd)

## Promise

- The Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value.
- A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

- A promise is in one of these states:
  1. pending: initial state - A pending promise can either be fulfilled with a value, or rejected with a reason (error).
  1. fulfilled: operation success
  1. rejected: operation failed

---

<img src="images/promises.png">

---

## Static Methods

1. Promise.all(iterable)
1. Promise.allSettled(iterable)
1. Promise.any(iterable)
1. Promise.race(iterable)
1. Promise.reject(reason)
1. Promise.resolve(value)

### Instance Methods

1. Promise.prototype.catch()
1. Promise.prototype.then()
1. Promise.prototype.finally()

---

## Destructuring

- The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.
- The destructuring assignment uses similar syntax, but on the left-hand side of the assignment to define what values to unpack from the sourced variable.

---

## Spread

- Spread syntax (...) allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

### Spread in function calls

- Replace apply()
- It is common to use Function.prototype.apply() in cases where you want to use the elements of an array as arguments to a function.

- With spread syntax the above can be written as:

```javascript
function myFunction(x, y, z) {}
const args = [0, 1, 2];
myFunction(...args);
```

---

### Rest

- The rest parameter syntax allows us to represent an indefinite number of arguments as an array.
- A function's last parameter can be prefixed with ... which will cause all remaining (user supplied) arguments to be placed within a "standard" JavaScript array.

  - Only the last parameter can be a "rest parameter".

---

## There are three main differences between rest parameters and the arguments object:

1. rest parameters are only the ones that haven't been given a separate name (i.e. formally defined in function expression), while the arguments object contains all arguments passed to the function;
1. the arguments object is not a real array, while rest parameters are Array instances, meaning methods like sort, map, forEach or pop can be applied on it directly;
1. the arguments object has additional functionality specific to itself (like the callee property).

---

## Videos

### TDD, Where did it all go wrong

- Key misunderstandings around what do I test, what is a unit test, and what is the 'public interface' have led to test suites that are brittle, hard to read, and do not support easy refactoring. In this talk, we re-discover Kent's original proposition, discover where key misunderstandings occurred and look at a better approach to TDD that supports software development instead of impeding it. Be prepared from some sacred cows to be slaughtered and fewer but better tests to be written.

---

### What the heck is the event loop anyway

- &yet employee talking about how event loops work in JavaScript.
- the call stack
  - one thread == one call stack == one thing at a time
- setTimeout is a minimun time to execution.

- callbacks an asynchronous callback
  - forEach takes a function but doesn't run it asynchronously

- JavaScript programmers like to use words like, “event-loop”, “non-blocking”, “callback”, “asynchronous”, “single-threaded” and “concurrency”.

- We say things like “don’t block the event loop”, “make sure your code runs at 60 frames-per-second”, “well of course, it won’t work, that function is an asynchronous callback!”
