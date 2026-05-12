# 02. Hoisting and Closure

---

## What is Hoisting?

## Ans

Hoisting is a mechanism in JavaScript where variable and function declarations are moved to the top of their scope during the memory creation phase.

### Ex:

```js
console.log(a);

var a = 10;

// Output: undefined
```

### Ex:

Internally, JavaScript treats it like this:

```js
var a;

console.log(a);

a = 10;
```

---

## What is Closure?

## Ans

A closure is created when an inner function remembers variables from its outer function even after the outer function has finished execution.

### Ex:

```js
function outer() {
  let count = 0;

  return function inner() {
    count++;

    console.log(count);
  };
}

const counter = outer();

counter(); // 1
counter(); // 2
```

---

### Use Cases of Closures

- Data Hiding
- Private Variables
- Memoization
- Callbacks

---

## What is Scope in JavaScript?

## Ans

Scope determines where variables can be accessed in the code.

### Types of Scope

- `Global Scope`
- `Function Scope`
- `Block Scope`
- `Lexical Scope`

---

## Global Scope

Variables declared outside functions can be accessed anywhere in the program.

### Ex:

```js
let name = "Adarsh";

function greet() {
  console.log(name);
}

greet();
```

---

## Function Scope

Variables declared inside a function can only be accessed inside that function.

### Ex:

```js
function test() {
  let age = 24;

  console.log(age); // 24
}

test();
```

---

## Block Scope

Variables declared using `let` and `const` inside `{}` can only be accessed within that block.

### Ex:

```js
{
  let city = "Delhi";

  console.log(city); // Delhi
}
```

---

## Lexical Scope

Lexical scope means inner functions can access variables from their parent functions.

### Ex:

```js
function outer() {
  let username = "Adarsh";

  function inner() {
    console.log(username);
  }

  inner();
}

outer();
```
