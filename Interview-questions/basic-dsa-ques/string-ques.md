# String Problems in JavaScript

---

# Reverse a String

## Answer

Reverse characters of a string.

---

## Explanation

We first convert string into:
```js
Array
```

using:
```js
split("")
```

Then:
- reverse the array
- join it back into string

---

## Brute Force Approach

```js
const str = "hello";

let reversed = "";

for (let i = str.length - 1; i >= 0; i--) {

  reversed += str[i];
}

console.log(reversed);
```

---

## Output

```js
olleh
```

---

## Optimized Approach

```js
const str = "hello";

const reversed =
  str.split("").reverse().join("");

console.log(reversed);
```

---

## Output

```js
olleh
```

---

## Time Complexity

```js
O(n)
```

---

# Palindrome Check

## Answer

Check whether string is palindrome or not.

---

## Explanation

A palindrome reads same:
- from left to right
- from right to left

Example:
```js
madam
racecar
```

---

## Brute Force Approach

```js
const str = "madam";

const reversed =
  str.split("").reverse().join("");

if (str === reversed) {

  console.log("Palindrome");

} else {

  console.log("Not Palindrome");
}
```

---

## Output

```js
Palindrome
```

---

## Optimized Approach

```js
function isPalindrome(str) {

  let start = 0;

  let end = str.length - 1;

  while (start < end) {

    if (str[start] !== str[end]) {

      return false;
    }

    start++;
    end--;
  }

  return true;
}

console.log(isPalindrome("madam"));
```

---

## Output

```js
true
```

---

## Time Complexity

```js
O(n)
```

---

# Count Characters

## Answer

Count total characters in string.

---

## Explanation

Strings have built-in:
```js
length
```

property which returns total number of characters.

---

## Example

```js
const str = "javascript";

console.log(str.length);
```

---

## Output

```js
10
```

---

## Time Complexity

```js
O(1)
```

---

# Find Duplicate Characters

## Answer

Find repeated characters from string.

---

## Explanation

We use an object:
```js
{}
```

to store frequency of every character.

If frequency becomes greater than:
```js
1
```

then character is duplicated.

---

## Brute Force Approach

```js
const str = "programming";

for (let i = 0; i < str.length; i++) {

  for (let j = i + 1; j < str.length; j++) {

    if (str[i] === str[j]) {

      console.log(str[i]);

      break;
    }
  }
}
```

---

## Output

```js
r
g
m
```

---

## Optimized Approach

```js
const str = "programming";

const obj = {};

for (let char of str) {

  obj[char] = (obj[char] || 0) + 1;
}

for (let key in obj) {

  if (obj[key] > 1) {

    console.log(key);
  }
}
```

---

## Output

```js
r
g
m
```

---

## Time Complexity

```js
O(n)
```

---

# Anagram Check

## Answer

Check whether two strings are anagrams or not.

---

## Explanation

Two strings are called:
```js
Anagrams
```

if both strings contain:
- same characters
- same frequency

Example:
```js
listen
silent
```

---

## Brute Force Approach

```js
const str1 = "listen";
const str2 = "silent";

const sorted1 =
  str1.split("").sort().join("");

const sorted2 =
  str2.split("").sort().join("");

console.log(sorted1 === sorted2);
```

---

## Output

```js
true
```

---

## Optimized Approach

```js
function isAnagram(str1, str2) {

  if (str1.length !== str2.length) {

    return false;
  }

  const obj = {};

  for (let char of str1) {

    obj[char] = (obj[char] || 0) + 1;
  }

  for (let char of str2) {

    if (!obj[char]) {

      return false;
    }

    obj[char]--;
  }

  return true;
}

console.log(
  isAnagram("listen", "silent")
);
```

---

## Output

```js
true
```

---

## Time Complexity

```js
O(n)
```