# 22. Event Loop in JavaScript

---

# What is the Event Loop?

## Answer

The Event Loop is a mechanism that allows JavaScript to handle asynchronous operations even though JavaScript is:
```js
Single Threaded
```

It continuously checks:
- Call Stack
- Callback Queue
- Microtask Queue

and manages code execution.

---

# Important Components

1. Call Stack
2. Web APIs
3. Callback Queue
4. Microtask Queue
5. Event Loop

---

# 1. Call Stack

## Answer

The Call Stack executes synchronous code line by line.

---

# 2. Web APIs

## Answer

Browser APIs that handle asynchronous tasks like:
- `setTimeout`
- `fetch`
- DOM events

---

# 3. Callback/Macrotask Queue

## Answer

Stores callback functions from:
```js
setTimeout()
setInterval()
DOM Events
```

---

# 4. Microtask Queue

## Answer

Stores:
- Promise callbacks
- async/await tasks

Microtask Queue gets higher priority than Callback Queue.

---

# Example

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

---

# Output

```js
Start
End
Promise
Timeout
```

---

# Step-by-Step Execution

## Step 1

```js
console.log("Start");
```

executes immediately.

Output:
```js
Start
```

---

## Step 2

```js
setTimeout()
```

goes to:
```js
Web APIs
```

---

## Step 3

```js
Promise.resolve()
```

callback goes to:
```js
Microtask Queue
```

---

## Step 4

```js
console.log("End");
```

executes immediately.

Output:
```js
End
```

---

# Current State

## Call Stack Empty

Now Event Loop checks queues.

---

# Step 5

Microtask Queue gets priority.

```js
console.log("Promise");
```

executes.

Output:
```js
Promise
```

---

# Step 6

Callback Queue executes.

```js
console.log("Timeout");
```

Output:
```js
Timeout
```

---

# Final Output

```js
Start
End
Promise
Timeout
```

---

# Important Point

Priority Order:
```js
Call Stack
↓
Microtask Queue
↓
Callback Queue
```

---

# Why Event Loop is Important?

## Answer

Event Loop helps JavaScript:
- handle async tasks
- perform non-blocking operations
- execute promises
- manage timers

---

# Real World Usage

Event Loop is used in:
- API calls
- Timers
- Async JavaScript
- React applications
- Node.js