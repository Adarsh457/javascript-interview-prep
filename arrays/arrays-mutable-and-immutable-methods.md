# 04. Arrays Methods in JavaScript

---
## Mutable vs Immutable Methods

### Mutable Methods

Mutable methods modify the original array.

### Common Mutable Methods

- `push()`
- `pop()`
- `shift()`
- `unshift()`
- `splice()`
- `sort()`
- `reverse()`

### Ex :

```js
let nums = [1, 2, 3];

nums.push(4);

console.log(nums); // [1, 2, 3, 4]
```

## `push()`

### Ans

Adds elements at the end of an array.

### Ex :

```js
let fruits = ["Apple", "Banana"];

fruits.push("Mango");

console.log(fruits);
```

### Output

```js
["Apple", "Banana", "Mango"]
```

---

## `pop()`

### Ans

Removes the last element from an array.

### Ex :

```js
let fruits = ["Apple", "Banana", "Mango"];

fruits.pop();

console.log(fruits);
```

### Output

```js
["Apple", "Banana"]
```

---

## `shift()`

### Ans

Removes the first element from an array.

### Ex :

```js
let nums = [1, 2, 3];

nums.shift();

console.log(nums);
```

### Output

```js
[2, 3]
```

---

## `unshift()`

### Ans

Adds elements at the beginning of an array.

### Ex :

```js
let nums = [2, 3];

nums.unshift(1);

console.log(nums);
```

### Output

```js
[1, 2, 3]
```

---



## `slice()`

### Ans

Returns a portion of an array without modifying the original array.

### Ex :

```js
let nums = [1, 2, 3, 4, 5];

let result = nums.slice(1, 4);

console.log(result);
```

### Output

```js
[2, 3, 4]
```

---

## `splice()`

### Ans

Adds or removes elements from an array by modifying the original array.

### Ex :

```js
let nums = [1, 2, 3, 4];

nums.splice(1, 2);

console.log(nums);
```

### Output

```js
[1, 4]
```

---

## `concat()`

### Ans

Merges arrays and returns a new array.

### Ex :

```js
let arr1 = [1, 2];
let arr2 = [3, 4];

let result = arr1.concat(arr2);

console.log(result);
```

### Output

```js
[1, 2, 3, 4]
```

---

## `sort()`

### Ans

Sorts array elements.

### Ex :

```js
let nums = [4, 2, 1, 3];

nums.sort();

console.log(nums);
```

### Output

```js
[1, 2, 3, 4]
```

---

## `reverse()`

### Ans

Reverses the array.

### Ex :

```js
let nums = [1, 2, 3];

nums.reverse();

console.log(nums);
```

### Output

```js
[3, 2, 1]
```




Here, the original array is modified.

---

### Immutable Methods

Immutable methods do NOT modify the original array.

They return a new array.

### Common Immutable Methods

- `map()`
- `filter()`
- `slice()`
- `concat()`

### Ex :

```js
let nums = [1, 2, 3];

let doubled = nums.map((num) => num * 2);

console.log(nums);     // [1, 2, 3]
console.log(doubled);  // [2, 4, 6]
```

The original array remains unchanged.

---

# Common Array Methods

---

## `map()`

### Ans

Creates a new array by transforming each element.

### Ex :

```js
let nums = [1, 2, 3];

let doubled = nums.map((num) => num * 2);

console.log(doubled);
```

### Output

```js
[2, 4, 6]
```

---

## `filter()`

### Ans

Returns a new array containing elements that satisfy a condition.

### Ex :

```js
let nums = [1, 2, 3, 4];

let evenNumbers = nums.filter((num) => num % 2 === 0);

console.log(evenNumbers);
```

### Output

```js
[2, 4]
```

---

## `reduce()`

### Ans

Reduces an array into a single value.

### Ex :

```js
let nums = [1, 2, 3, 4];

let sum = nums.reduce((acc, curr) => acc + curr, 0);

console.log(sum);
```

### Output

```js
10
```

---

## `find()`

### Ans

Returns the first element that satisfies a condition.

### Ex :

```js
let nums = [10, 20, 30, 40];

let result = nums.find((num) => num > 20);

console.log(result);
```

### Output

```js
30
```

---

## `findIndex()`

### Ans

Returns the index of the first matching element.

### Ex :

```js
let nums = [10, 20, 30, 40];

let index = nums.findIndex((num) => num > 20);

console.log(index);
```

### Output

```js
2
```

---

## `includes()`

### Ans

Checks whether an element exists in the array.

### Ex :

```js
let fruits = ["Apple", "Banana", "Mango"];

console.log(fruits.includes("Mango"));
```

### Output

```js
true
```

---