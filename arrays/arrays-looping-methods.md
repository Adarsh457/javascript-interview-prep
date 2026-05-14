# 05. Looping Concepts in JavaScript

---

## 1. `for` Loop

### Ans

The `for` loop is used when the number of iterations is known.

### Syntax

```js
for(initialization; condition; increment/decrement) {
   // code
}
```

### Ex :

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### Output

```js
0
1
2
3
4
```

---

## 2. `while` Loop

### Ans

The `while` loop runs as long as the condition is true.

### Ex :

```js
let i = 0;

while (i < 5) {
  console.log(i);

  i++;
}
```

---

## 3. `do...while` Loop

### Ans

The `do...while` loop executes the code at least once.

### Ex :

```js
let i = 0;

do {
  console.log(i);

  i++;
} while (i < 5);
```

---

## 4. `for...of` Loop

### Ans

The `for...of` loop is used to iterate over iterable objects like arrays and strings.

### Ex :

```js
let fruits = ["Apple", "Banana", "Mango"];

for (let fruit of fruits) {
  console.log(fruit);
}
```

---

## 5. `for...in` Loop

### Ans

The `for...in` loop is used to iterate over object keys.

### Ex :

```js
let user = {
  name: "Adarsh",
  age: 24
};

for (let key in user) {
  console.log(key, user[key]);
}
```

---

## 6. `forEach()` Method

### Ans

The `forEach()` method executes a function for each array element.

### Ex :

```js
let nums = [1, 2, 3];

nums.forEach((num) => {
  console.log(num);
});
```

---

## 7. `map()` Method

### Ans

The `map()` method creates a new array by transforming each element.

### Ex :

```js
let nums = [1, 2, 3];

let doubled = nums.map((num) => num * 2);

console.log(doubled);
```

---

# Difference Between `forEach()` and `map()`

| `forEach()` | `map()` |
|---|---|
| Does not return a new array | Returns a new array |
| Used for iteration | Used for transformation |
| Cannot chain methods | Can chain methods |

### Ex :

```js
let nums = [1, 2, 3];

nums.forEach((num) => console.log(num));

let result = nums.map((num) => num * 2);

console.log(result);
```