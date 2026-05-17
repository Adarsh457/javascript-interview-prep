# 23. Synchronous vs Asynchronous JavaScript

---

# Synchronous JavaScript

## Answer

In synchronous JavaScript:
- code executes line by line
- one task completes before the next task starts

JavaScript waits for each operation to finish.

---

# Example

```js
console.log("Start");

console.log("Middle");

console.log("End");
```

---

# Output

```js
Start
Middle
End
```

---

# Explanation

Each line executes one after another in sequence.

---

# Asynchronous JavaScript

## Answer

In asynchronous JavaScript:
- some tasks run in the background
- JavaScript does NOT wait for them to finish

This helps prevent blocking.

---

# Example

```js
console.log("Start");

setTimeout(() => {
  console.log("Async Task");
}, 2000);

console.log("End");
```

---

# Output

```js
Start
End
Async Task
```

(after 2 seconds)

---

# Explanation

```js
setTimeout()
```

runs asynchronously.

JavaScript continues executing the remaining code without waiting.

---

# Difference Between Synchronous and Asynchronous

| Synchronous | Asynchronous |
|---|---|
| Executes line by line | Executes tasks independently |
| Blocks execution | Non-blocking |
| Slower for heavy tasks | Better performance |

---

# Real World Examples

## Synchronous
- Mathematical calculations
- Simple loops

## Asynchronous
- API calls
- Timers
- Database operations
- File handling

---

# Important Interview Point

JavaScript is:
```js
Single Threaded
```

but handles asynchronous tasks using:
```js
Event Loop
```