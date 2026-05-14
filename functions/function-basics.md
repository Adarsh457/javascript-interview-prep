# 06. Functions in JavaScript

---

## 1. What is a Function?

### Answer

A function is a reusable block of code used to perform a specific task.

### Example

```js
function greet() {
  console.log("Hello JavaScript");
}

greet();
```

---

## 2. Function Declaration

### Answer

A function declaration defines a named function using the `function` keyword.

### Example

```js
function add(a, b) {
  return a + b;
}

console.log(add(2, 3));
```

---

## 3. Function Expression

### Answer

A function expression stores a function inside a variable.

### Example

```js
const greet = function () {
  console.log("Hello");
};

greet();
```

---

## 4. Parameters vs Arguments

### Answer

- Parameters → Variables defined in function definition
- Arguments → Values passed during function call

### Example

```js
function multiply(a, b) {
  return a * b;
}

multiply(2, 3);
```

Here:
- `a` and `b` are parameters
- `2` and `3` are arguments

---

## 5. Return Keyword

### Answer

The `return` keyword sends a value back from a function.

### Example

```js
function square(num) {
  return num * num;
}

console.log(square(4));
```

---

## 6. Arrow Functions

### Answer

Arrow functions provide a shorter syntax for writing functions.

### Example

```js
const add = (a, b) => {
  return a + b;
};

console.log(add(2, 3));
```

---