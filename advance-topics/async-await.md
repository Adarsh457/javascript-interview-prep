# 21. Async Await in JavaScript

---

# What is `async` and `await`?

## Answer

`async` and `await` are used to handle asynchronous operations in a cleaner and more readable way.

They are built on top of:
```js
Promises
```

---

# `async` Function

## Answer

An `async` function always returns a promise.

---

# Example

```js
async function greet() {
  return "Hello";
}

greet().then((data) => {
  console.log(data);
});
```

---

# Output

```js
Hello
```

---

# Explanation

Even though:
```js
return "Hello"
```

looks like a normal value,

JavaScript internally converts it into:
```js
Promise.resolve("Hello")
```

---

# What is `await`?

## Answer

`await` pauses the execution of an async function until the promise is resolved.

---

# Example

```js
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data Fetched");
    }, 2000);
  });
}

async function getData() {
  const result = await fetchData();

  console.log(result);
}

getData();
```

---

# Output

```js
Data Fetched
```

(after 2 seconds)

---

# Explanation

## Step 1

```js
fetchData()
```

returns a promise.

---

## Step 2

```js
await fetchData()
```

waits until the promise resolves.

---

## Step 3

Resolved value gets stored inside:
```js
result
```

---

# Error Handling using `try...catch`

## Example

```js
function fetchData() {
  return new Promise((resolve, reject) => {
    reject("API Error");
  });
}

async function getData() {
  try {
    const result = await fetchData();

    console.log(result);
  } catch (error) {
    console.log(error);
  }
}

getData();
```

---

# Output

```js
API Error
```

---

# Why Use Async Await?

## Answer

Advantages:
- cleaner syntax
- easier to read
- avoids callback hell
- better error handling

---

# Important Point

`await` can only be used inside async functions

---

# Async Await vs Promise

| Promise | Async Await |
|---|---|
| Uses `.then()` | Uses `await` |
| More chaining | Cleaner syntax |
| Harder to read | Easier to read |

---

# Real World Usage

Async Await is heavily used in:
- API calls
- Fetch requests
- Database operations
- React applications