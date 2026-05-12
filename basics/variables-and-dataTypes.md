# 01. JavaScript Variables and Data Types.

---

## 1. What is JavaScript?

**Ans:**  
JavaScript is a single-threaded scripting language used to create dynamic and interactive web pages.

### Ex : 

```js
console.log("Hello JavaScript");
```

---

## 2. Difference Between `var`, `let`, and `const`

`var` :
- can be redeclared and reassign
- Function Scoped.
- Supports Hoisting.

### Ex:   
    var a = 10;
    var a = 20;

    console.log(a); // 20

`Let` :
- Cannot be redeclared in the same scope
- Can be reassigned
- Block Scoped
- Hoisted but stored inside Temporal Dead Zone (TDZ)

### Ex:
        let age = 24;
        age = 25;

        console.log(age); // 25

`Const` :
- Cannot be redeclared and reassign.
- Blocked Scoped.
- Temporal Dead Zone.

## Ex:
        const PI = 3.14;

        // PI = 4; ❌ Error

---

## 3. Data Types in JavaScript

**Ans:**  

Js has two categories. 

`Primitive Data Types` : (`string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`).
```js
Ex :
let str = "JavaScript";
let num = 10;
let big = 891283991n;
let bool = true;
let sym = Symbol("id");
let und;
let n = null;
```

`Non - Primitive Data Types` :

`Object` : Objects store data in the form of key-value pairs.

### Ex

```js
let user = {
  name: "Adarsh",
  age: 24
};

console.log(user.name); // Adarsh
```

`Array` : Arrays are used to store multiple values in a single variable.

### Ex

```js
let numbers = [1, 2, 3, 4];

console.log(numbers[0]); // 1
```

`Function` : Functions are reusable blocks of code used to perform specific tasks.

### Ex

```js
function greet() {
  console.log("Hello JavaScript");
}

greet();
```

---

## 4. Difference Between `==` and `===` ?

**Ans:**  

`Loosely Equal(==)` -> Compares the values on both the side.

### Ex: 

```js
console.log(5 == "5"); // true
```

`Strictly Equal(===)` -> Compares both the Values and Data Types on both the side.

### Ex:

```js
console.log(5 === "5"); // false
```

---

## 5. What is Type Coercion?

Type coercion is JavaScript's automatic conversion of one data type into another during operations.

### Ex: 

```js
console.log("5" + 2); // "52"
```

---

## 6. Difference Between null and undefined ?

**Ans:**  

`undefined` -> means a variable has been declared but no value has been assigned.

### Ex: 

```js
let name;
console.log(name); // undefined
```

`null` -> represents an intentional empty value.

### Ex: 

```js
let user = null;
console.log(user); // null
```

---

## 7. What is NaN ?

**Ans:**  

`NaN` stands for "Not a Number".

It occurs when a mathematical operation fails to produce a valid number.

### Ex:

```js
console.log("hello" / 2); // NaN
```
