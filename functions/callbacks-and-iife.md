# 07. CallBakcs and IIFE in JavaScript

---


## 1. Anonymous Functions

### Answer

Anonymous functions are functions without a name.

### Example

```js
setTimeout(function () {
  console.log("Hello");
}, 1000);
```

---

## 2. Callback Functions

### Answer

A callback function is passed as an argument to another function.

### Example

```js
function greet(name, callback) {
  console.log(`Hello ${name}`);

  callback();
}

function sayBye() {
  console.log("Goodbye");
}

greet("Adarsh", sayBye);
```

## Why are Callbacks Used?

### Answer

Callbacks are mainly used for:
- Asynchronous operations
- Event handling
- Timers
- API calls

### Example

```js
setTimeout(function () {
  console.log("Executed after 2 seconds");
}, 2000);
```

---

## 3. Higher Order Functions

### Answer

A higher order function is a function that:
- accepts another function as an argument
- OR returns a function

### Example

```js
function greet(callback) {
  callback();
}

function sayHello() {
  console.log("Hello");
}

greet(sayHello);
```

---

## 4. What is an IIFE?

### Answer

IIFE stands for Immediately Invoked Function Expression.

It executes immediately after being created.

### Example

```js
(function () {
  console.log("IIFE Executed");
})();
```

## Why Use IIFE?

### Answer

IIFE is used to:
- Avoid global scope pollution
- Create private scope
- Execute code immediately

### Example

```js
(function () {
  let message = "Private Variable";

  console.log(message);
})();
```