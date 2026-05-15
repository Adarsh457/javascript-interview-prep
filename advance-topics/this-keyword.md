# 16. `this` Keyword in JavaScript

---

# What is `this`?

## Answer

`this` refers to the object that is currently executing the function.

The value of `this` depends on:
- how the function is called
- where the function is called

---

# `this` in Global Scope

## Example

```js
console.log(this);
```

### Browser Output

```js
window
```

In browsers, global `this` refers to the `window` object.

---

# `this` Inside an Object Method

## Example

```js
const user = {
  name: "Adarsh",

  greet() {
    console.log(this.name);
  }
};

user.greet();
```

### Output

```js
Adarsh
```

### Reason

Here:
```js
this = user object
```

---

# `this` Inside a Regular Function

## Example

```js
function test() {
  console.log(this);
}

test();
```

### Browser Output

```js
window
```

In normal functions, `this` refers to the global object in non-strict mode.

---

# `this` Inside an Arrow Function

## Example

```js
const user = {
  name: "Adarsh",

  greet: () => {
    console.log(this.name);
  }
};

user.greet();
```

### Output

```js
undefined
```

---

# Reason

Arrow functions do NOT have their own `this`.

They inherit `this` from their surrounding lexical scope.

---

# Regular Function vs Arrow Function

| Regular Function | Arrow Function |
|---|---|
| Has its own `this` | Does not have its own `this` |
| Value depends on caller | Inherits from parent scope |

---

# `this` Inside Nested Function

## Example

```js
const user = {
  name: "Adarsh",

  greet() {
    function test() {
      console.log(this.name);
    }

    test();
  }
};

user.greet();
```

### Output

```js
undefined
```

Because regular function `test()` gets its own `this`.

---

# Fix Using Arrow Function

## Example

```js
const user = {
  name: "Adarsh",

  greet() {
    const test = () => {
      console.log(this.name);
    };

    test();
  }
};

user.greet();
```

### Output

```js
Adarsh
```

---

# Important Interview Point

The value of:
```js
this
```

is determined during:
```js
Function Invocation
```

NOT during function creation.

---

# Common Use Cases of `this`

- Object methods
- Classes
- Event handlers
- Constructors
- DOM manipulation