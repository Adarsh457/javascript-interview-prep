# 14. Spread vs Rest Operator in JavaScript

---

# Spread Operator (`...`)

## Answer

The spread operator is used to expand elements of an array or object.

### Example with Array

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];

console.log(arr2);
```

### Output

```js
[1, 2, 3, 4]
```

---

### Example with Object

```js
const user = {
  name: "Adarsh"
};

const updatedUser = {
  ...user,
  age: 24
};

console.log(updatedUser);
```

### Output

```js
{
  name: "Adarsh",
  age: 24
}
```

---

# Rest Operator (`...`)

## Answer

The rest operator collects multiple values into a single array.

### Example

```js
function sum(...nums) {
  console.log(nums);
}

sum(1, 2, 3, 4);
```

### Output

```js
[1, 2, 3, 4]
```

---

# Rest Operator in Array Destructuring

### Example

```js
const nums = [1, 2, 3, 4];

const [a, ...rest] = nums;

console.log(a);
console.log(rest);
```

### Output

```js
1
[2, 3, 4]
```

---

# Difference Between Spread and Rest Operator

| Spread Operator | Rest Operator |
|---|---|
| Expands values | Collects values |
| Used in arrays/objects | Used in function parameters |
| Used while copying/merging | Used while grouping |

---

# Important Point

Both operators use:
```js
...
```

But their behavior depends on where they are used.