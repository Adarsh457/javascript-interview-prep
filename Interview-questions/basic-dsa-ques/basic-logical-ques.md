# Basic Logic Building Questions

---

# Swap Two Numbers

## Example

```js
let a = 10;
let b = 20;

[a, b] = [b, a];

console.log(a, b);
```

---

## Output

```js
20 10
```

---

# Even or Odd

## Example

```js
const num = 7;

if (num % 2 === 0) {

  console.log("Even");

} else {

  console.log("Odd");
}
```

---

## Output

```js
Odd
```

---

# FizzBuzz

## Example

```js
for (let i = 1; i <= 15; i++) {

  if (i % 3 === 0 && i % 5 === 0) {

    console.log("FizzBuzz");
  }

  else if (i % 3 === 0) {

    console.log("Fizz");
  }

  else if (i % 5 === 0) {

    console.log("Buzz");
  }

  else {

    console.log(i);
  }
}
```

---

# Sum of Array

## Example

```js
const arr = [1, 2, 3, 4];

let sum = 0;

for (let num of arr) {

  sum += num;
}

console.log(sum);
```

---

## Output

```js
10
```