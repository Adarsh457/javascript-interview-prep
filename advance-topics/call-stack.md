# 15. Call Stack in JavaScript

---

# What is Call Stack?

## Answer

Call Stack is a mechanism used by JavaScript to keep track of function execution.

It follows:
```js
LIFO (Last In First Out)
```

The last function added to the stack is executed first.

---

# How Call Stack Works

- When a function is called, it is pushed into the call stack.
- When the function completes execution, it is removed from the stack.

---

# Example

```js
function one() {
  two();
}

function two() {
  three();
}

function three() {
  console.log("Hello");
}

one();
```

---

# Execution Flow

## Step 1

```js
Global Execution Context
```

gets pushed into the call stack.

---

## Step 2

```js
one()
```

gets pushed.

---

## Step 3

```js
two()
```

gets pushed.

---

## Step 4

```js
three()
```

gets pushed.

---

## Step 5

```js
console.log("Hello");
```

executes.

---

# Removing from Stack

Functions are removed in reverse order.

```js
three() → removed
two() → removed
one() → removed
```

---

# Output

```js
Hello
```

---

# Stack Overflow

## Answer

When too many functions are added to the call stack, it causes:
```js
Stack Overflow
```

---

# Example

```js
function test() {
  test();
}

test();
```

---

# Output

```js
Maximum call stack size exceeded
```

Because the function keeps calling itself infinitely.

---

# Important Interview Point

JavaScript has:
```js
Single Call Stack
```

That is why JavaScript is:
```js
Single Threaded
```

---

# Real World Usage

Call stack helps JavaScript:
- track function execution
- manage execution order
- handle nested function calls

---

# Relation with Execution Context

Every time a function is called: Function Execution Context is pushed into the call stack.

After execution: Execution Context is removed from the stack.