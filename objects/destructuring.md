# 12. Object Destructuring in JavaScript

---

## What is Object Destructuring?

### Answer

Object destructuring allows extracting object properties into variables.

It makes code cleaner and shorter.

---

# Basic Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

const { name, age } = user;

console.log(name);
console.log(age);
```

### Output

```js
Adarsh
24
```

---

# Renaming Variables

### Example

```js
const user = {
  name: "Adarsh"
};

const { name: username } = user;

console.log(username);
```

### Output

```js
Adarsh
```

---

# Default Values

### Example

```js
const user = {
  name: "Adarsh"
};

const { age = 25 } = user;

console.log(age);
```

### Output

```js
25
```

---

# Nested Object Destructuring

### Example

```js
const user = {
  name: "Adarsh",

  address: {
    city: "Delhi"
  }
};

const {
  address: { city }
} = user;

console.log(city);
```

### Output

```js
Delhi
```

---

# Destructuring in Function Parameters

### Example

```js
function greet({ name, age }) {
  console.log(name, age);
}

const user = {
  name: "Adarsh",
  age: 24
};

greet(user);
```

### Output

```js
Adarsh 24
```

---

# Array Destructuring

### Example

```js
const colors = ["Red", "Blue", "Green"];

const [first, second] = colors;

console.log(first);
console.log(second);
```

### Output

```js
Red
Blue
```

---

# Skipping Values in Array Destructuring

### Example

```js
const nums = [1, 2, 3];

const [a, , c] = nums;

console.log(a);
console.log(c);
```

### Output

```js
1
3
```

---

# Advantages of Destructuring

- Cleaner syntax
- Less repetitive code
- Easy extraction of values
- Commonly used in React

---

# Important Point

Destructuring is heavily used in:
- React props
- API responses
- State management
- Function parameters