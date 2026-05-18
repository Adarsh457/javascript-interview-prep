# HashMap Problems in JavaScript

---

# Count Frequency of Elements

## Answer

Count occurrence of elements in an array.

---

## Explanation

We use an object:
```js
{}
```

as a:
```js
HashMap
```

Where:
- key → element
- value → frequency count

If element already exists:
- increase count by 1

---

## Brute Force Approach

```js
const fruits = [
  "apple",
  "banana",
  "apple",
  "orange"
];

for (let i = 0; i < fruits.length; i++) {

  let count = 0;

  for (let j = 0; j < fruits.length; j++) {

    if (fruits[i] === fruits[j]) {

      count++;
    }
  }

  console.log(fruits[i], count);
}
```

---

## Output

```js
apple 2
banana 1
apple 2
orange 1
```

---

## Optimized Approach

```js
const fruits = [
  "apple",
  "banana",
  "apple",
  "orange"
];

const freq = {};

for (let item of fruits) {

  freq[item] = (freq[item] || 0) + 1;
}

console.log(freq);
```

---

## Output

```js
{
  apple: 2,
  banana: 1,
  orange: 1
}
```

---

## Time Complexity

```js
O(n)
```

---

# Most Repeated Character

## Answer

Find most repeated character in a string.

---

## Explanation

We store frequency of every character inside:
```js
Object
```

Then compare frequency values and track:
- maximum count
- maximum occurring character

---

## Brute Force Approach

```js
const str = "javascript";

let maxChar = "";
let maxCount = 0;

for (let i = 0; i < str.length; i++) {

  let count = 0;

  for (let j = 0; j < str.length; j++) {

    if (str[i] === str[j]) {

      count++;
    }
  }

  if (count > maxCount) {

    maxCount = count;

    maxChar = str[i];
  }
}

console.log(maxChar);
```

---

## Output

```js
a
```

---

## Optimized Approach

```js
const str = "javascript";

const obj = {};

let maxChar = "";
let maxCount = 0;

for (let char of str) {

  obj[char] = (obj[char] || 0) + 1;

  if (obj[char] > maxCount) {

    maxCount = obj[char];

    maxChar = char;
  }
}

console.log(maxChar);
```

---

## Output

```js
a
```

---

## Time Complexity

```js
O(n)
```