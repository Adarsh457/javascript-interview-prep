# Array Problems in JavaScript

---

# Reverse an Array

## Answer

Reverse the elements of an array.

---

## Explanation

We use:
```js
Two Pointer Approach
```

One pointer starts from:
- beginning of array

Another pointer starts from:
- end of array

Then we swap values until both pointers meet.

---

## Brute Force Approach

```js
const arr = [1, 2, 3, 4, 5];

const reversed = [];

for (let i = arr.length - 1; i >= 0; i--) {

  reversed.push(arr[i]);
}

console.log(reversed);
```

---

## Output

```js
[5, 4, 3, 2, 1]
```

---

## Optimized Approach

```js
const arr = [1, 2, 3, 4, 5];

let i = 0;
let j = arr.length - 1;

while (i < j) {

  let temp = arr[i];

  arr[i] = arr[j];
  arr[j] = temp;

  i++;
  j--;
}

console.log(arr);
```

---

## Output

```js
[5, 4, 3, 2, 1]
```

---

## Time Complexity

```js
O(n)
```

---

# Find Largest and Second Largest

## Answer

Find largest and second largest values in array.

---

## Explanation

We traverse the array once.

If current element becomes:
```js
largest
```

then previous largest becomes:
```js
secondLargest
```

---

## Brute Force Approach

```js
const arr = [1, 22, 3, 120, 121, 200];

arr.sort((a, b) => b - a);

console.log(arr[0]);

console.log(arr[1]);
```

---

## Output

```js
200
121
```

---

## Optimized Approach

```js
const arr = [1, 22, 3, 120, 121, 200];

let largest = -1;
let secondLargest = -1;

for (let num of arr) {

  if (num > largest) {

    secondLargest = largest;

    largest = num;
  }

  else if (
    num > secondLargest &&
    num < largest
  ) {

    secondLargest = num;
  }
}

console.log(largest);

console.log(secondLargest);
```

---

## Output

```js
200
121
```

---

## Time Complexity

```js
O(n)
```

---

# Remove Duplicates

## Answer

Remove duplicate elements from array.

---

## Explanation

Duplicate values appear multiple times.

We use:
```js
Set
```

because Set stores:
```js
Unique Values Only
```

---

## Brute Force Approach

```js
const arr = [1, 2, 2, 3, 4, 4];

const result = [];

for (let i = 0; i < arr.length; i++) {

  if (!result.includes(arr[i])) {

    result.push(arr[i]);
  }
}

console.log(result);
```

---

## Output

```js
[1, 2, 3, 4]
```

---

## Optimized Approach

```js
const arr = [1, 2, 2, 3, 4, 4];

const unique = [...new Set(arr)];

console.log(unique);
```

---

## Output

```js
[1, 2, 3, 4]
```

---

## Time Complexity

```js
O(n)
```

---

# Flatten an Array

## Answer

Convert nested array into single array.

---

## Explanation

Nested arrays contain arrays inside arrays.

We use:
```js
flat()
```

method to convert nested array into:
```js
Single Array
```

---

## Brute Force Approach

```js
const arr = [1, [2, [3, 4]], 5];

const result = [];

for (let item of arr) {

  if (Array.isArray(item)) {

    for (let inner of item.flat()) {

      result.push(inner);
    }

  } else {

    result.push(item);
  }
}

console.log(result);
```

---

## Output

```js
[1, 2, 3, 4, 5]
```

---

## Optimized Approach

```js
const arr = [1, [2, [3, 4]], 5];

console.log(arr.flat(2));
```

---

## Output

```js
[1, 2, 3, 4, 5]
```

---

## Time Complexity

```js
O(n)
```

---

# Find Missing Number

## Answer

Find missing number from array.

---

## Explanation

We calculate:
```js
Expected Sum
```

using formula:
```js
n * (n + 1) / 2
```

Then subtract:
```js
Actual Sum
```

from expected sum.

---

## Brute Force Approach

```js
const arr = [1, 2, 3, 5];

const total = 5;

for (let i = 1; i <= total; i++) {

  if (!arr.includes(i)) {

    console.log(i);
  }
}
```

---

## Output

```js
4
```

---

## Optimized Approach

```js
const arr = [1, 2, 3, 5];

const total = 5;

let expectedSum =
  (total * (total + 1)) / 2;

let actualSum = 0;

for (let num of arr) {

  actualSum += num;
}

console.log(expectedSum - actualSum);
```

---

## Output

```js
4
```

---

## Time Complexity

```js
O(n)
```