# 20. Promises in JavaScript

---

# What is a Promise?

## Answer

A Promise is an object that represents the eventual completion or failure of an asynchronous operation.

Promises help handle:
- asynchronous code
- API calls
- timers
- database operations

---

# Promise States

A Promise has three states:

1. Pending
2. Fulfilled
3. Rejected

---

# 1. Pending

Initial state.

The operation is still running.

---

# 2. Fulfilled

Operation completed successfully.

---

# 3. Rejected

Operation failed.

---

# Creating a Promise

## Example

```js
const promise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Promise Resolved");
  } else {
    reject("Promise Rejected");
  }
});
```

---

# Consuming a Promise

## Using `.then()` and `.catch()`

```js
promise
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

# Output

```js
Promise Resolved
```

---

# Explanation

## `resolve()`

```js
resolve("Promise Resolved");
```

moves the promise to:
```js
fulfilled state
```

and executes:
```js
.then()
```

---

## `reject()`

```js
reject("Promise Rejected");
```

moves the promise to:
```js
rejected state
```

and executes:
```js
.catch()
```

---

# Example with `reject()`

```js
const promise = new Promise((resolve, reject) => {
  reject("Something Went Wrong");
});

promise
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log(error);
  });
```

---

# Output

```js
Something Went Wrong
```

---

# `.finally()`

## Answer

`.finally()` executes whether the promise is resolved or rejected.

---

# Example

```js
promise
  .finally(() => {
    console.log("Promise Completed");
  });
```

---

# Promise Chaining

## Example

```js
Promise.resolve(2)
  .then((data) => {
    return data * 2;
  })
  .then((data) => {
    console.log(data);
  });
```

---

# Output

```js
4
```

---

# Why Use Promises?

## Answer

Promises help:
- avoid callback hell
- write cleaner async code
- improve readability

---

# Important Point

Promises are `Asynchronous` and handled by `Microtask Queue` inside the `Event` Loop.

---

# Real World Usage

Promises are heavily used in:
- API calls
- Fetch requests
- Database operations
- Async JavaScript