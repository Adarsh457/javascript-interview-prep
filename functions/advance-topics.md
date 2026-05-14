# 07. Currying and Debounce in JavaScript

---

# Currying in JavaScript

---

## What is Currying?

### Answer

Currying is a technique where a function takes one argument at a time and returns another function.

### Example

```js
function add(a) {
  return function (b) {
    return a + b;
  };
}

console.log(add(2)(3));
```

---

## Arrow Function Version

### Example

```js
const multiply = (a) => (b) => a * b;

console.log(multiply(2)(4));
```

---

# Debouncing and Throttling in JavaScript

---

## What is Debouncing?

### Answer

Debouncing delays function execution until the user stops triggering the event.

### Example

```js
function debounce(func, delay) {
  let timer;

  return function () {
    clearTimeout(timer);

    timer = setTimeout(() => {
      func();
    }, delay);
  };
}
```

### Use Cases

- Search bars
- Input fields
- API calls

---

## What is Throttling?

### Answer

Throttling limits how often a function can execute.

### Example

```js
function throttle(func, delay) {
  let lastCall = 0;

  return function () {
    let now = new Date().getTime();

    if (now - lastCall < delay) return;

    lastCall = now;

    func();
  };
}
```

### Use Cases

- Scroll events
- Resize events
- Button clicks