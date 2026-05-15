# `call()`, `apply()` and `bind()` in JavaScript

---

# What is `call()`?

## Answer

`call()` is used to invoke a function immediately by passing a custom `this` value.

Arguments are passed separately.

---

# Syntax

```js
functionName.call(thisValue, arg1, arg2);
```

---

# Example

```js
const user = {
  name: "Adarsh"
};

function greet(city) {
  console.log(this.name, city);
}

greet.call(user, "Delhi");
```

### Output

```js
Adarsh Delhi
```

---

# What is `apply()`?

## Answer

`apply()` works similar to `call()`.

Difference:
- arguments are passed inside an array.

---

# Syntax

```js
functionName.apply(thisValue, [args]);
```

---

# Example

```js
const user = {
  name: "Adarsh"
};

function greet(city, country) {
  console.log(this.name, city, country);
}

greet.apply(user, ["Delhi", "India"]);
```

### Output

```js
Adarsh Delhi India
```

---

# What is `bind()`?

## Answer

`bind()` returns a new function with a fixed `this` value.

It does NOT execute immediately.

---

# Syntax

```js
functionName.bind(thisValue);
```

---

# Example

```js
const user = {
  name: "Adarsh"
};

function greet(city) {
  console.log(this.name, city);
}

const newFunction = greet.bind(user);

newFunction("Delhi");
```

### Output

```js
Adarsh Delhi
```

---

# Difference Between `call()`, `apply()` and `bind()`

| Method | Arguments | Executes Immediately |
|---|---|---|
| `call()` | Separate arguments | Yes |
| `apply()` | Array of arguments | Yes |
| `bind()` | Separate arguments | No |

---

# Function Borrowing

## Answer

Function borrowing means borrowing a method from another object using:
```js
call()
apply()
bind()
```

---

# Example

```js
const user1 = {
  name: "Adarsh"
};

const user2 = {
  name: "Rahul"
};

function greet() {
  console.log(this.name);
}

greet.call(user1);
greet.call(user2);
```

### Output

```js
Adarsh
Rahul
```

---

# Important Interview Point

`bind()` is commonly used in:
- event handlers
- React class components
- callbacks

because it preserves the value of:
```js
this
```