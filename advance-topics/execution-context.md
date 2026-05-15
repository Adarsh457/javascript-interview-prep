# 14. Execution Context in JavaScript

---

# What is Execution Context?

## Answer

Execution Context is the environment in which JavaScript code is executed.

It contains:
- variables
- functions
- scope
- value of `this`

JavaScript creates an execution context whenever code runs.

---

# Types of Execution Context

1. Global Execution Context
2. Function Execution Context

---

# Global Execution Context

## Answer

The Global Execution Context is created when the JavaScript program starts execution.

There is only one global execution context.

---

# Function Execution Context

## Answer

Whenever a function is invoked, JavaScript creates a new function execution context.

---

# Phases of Execution Context

JavaScript executes code in two phases:

1. Memory Creation Phase
2. Execution Phase

---

# 1. Memory Creation Phase

## Answer

In this phase:
- memory is allocated to variables and functions
- variables are initialized with `undefined`
- function declarations are stored completely in memory

---

# Example

```js
console.log(a);

var a = 10;
```

---

# Memory Creation Phase

```js
a = undefined
```

---

# Execution Phase

```js
console.log(a); // undefined

a = 10
```

---

# 2. Execution Phase

## Answer

In this phase:
- code executes line by line
- actual values are assigned
- functions are invoked

---

# Function Execution Context Example

```js
function greet() {
  let name = "Adarsh";

  console.log(name);
}

greet();
```

---

# What Happens Internally?

1. Global Execution Context gets created.
2. `greet()` function stored in memory.
3. `greet()` invoked.
4. New Function Execution Context created.
5. `name` variable allocated memory.
6. Function executes.
7. Function Execution Context removed from Call Stack.

---

# Important Interview Point

JavaScript is:
```js
Single Threaded Synchronous
```

Meaning:
- executes one line at a time
- executes in order

---

# Relation with Hoisting

Hoisting happens because of the:
```js
Memory Creation Phase
```

Variables and functions are stored before execution starts.

---

# Interview Question

## Output

```js
console.log(a);

var a = 5;
```

### Output

```js
undefined
```

### Reason

During memory creation:
```js
a = undefined
```

Later in execution phase:
```js
a = 5
```