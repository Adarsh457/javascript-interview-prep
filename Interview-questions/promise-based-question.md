# Promise Output Questions

---

# Question 1

```js
console.log("Start");

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

## Output

```js
Start
End
Promise
```

## Reason

Promise callbacks go to:
```js
Microtask Queue
```

---

# Question 2

```js
Promise.resolve(1)
  .then((data) => {
    return data + 1;
  })
  .then((data) => {
    console.log(data);
  });
```

## Output

```js
2
```

---

# Question 3

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

## Output

```js
Start
End
Promise
Timeout
```

## Reason

Promise callbacks go to:
```js
Microtask Queue
```

and:
```js
setTimeout
```

callbacks go to:
```js
Callback Queue
```

Microtask Queue gets higher priority.

---

# Question 4

```js
const promise = new Promise((resolve, reject) => {
  resolve("Success");

  reject("Failed");
});

promise.then((data) => {
  console.log(data);
});
```

## Output

```js
Success
```

## Reason

Once a promise is:
```js
Resolved
```

its state cannot change.

---

# Question 5

```js
Promise.reject("Error")
  .catch((err) => {
    console.log(err);

    return "Recovered";
  })
  .then((data) => {
    console.log(data);
  });
```

## Output

```js
Error
Recovered
```

## Reason

`.catch()` also returns a promise.

Returned value goes to next:
```js
.then()
```

---

# Question 6

```js
Promise.resolve()
  .then(() => {
    console.log(1);
  })
  .then(() => {
    console.log(2);
  });

console.log(3);
```

## Output

```js
3
1
2
```

## Reason

Synchronous code executes first.

Promise callbacks execute later from:
```js
Microtask Queue
```

---

# Question 7

```js
async function test() {
  return "Hello";
}

test().then((data) => {
  console.log(data);
});
```

## Output

```js
Hello
```

## Reason

Async functions always return:
```js
Promise
```

---

# Question 8

```js
async function test() {
  console.log("A");

  await Promise.resolve();

  console.log("B");
}

test();

console.log("C");
```

## Output

```js
A
C
B
```

## Reason

`await` pauses async function execution.

Remaining code executes after promise resolution.

---

# Question 9

```js
Promise.resolve(5)
  .then((num) => {
    return num * 2;
  })
  .then((num) => {
    return num + 1;
  })
  .then((num) => {
    console.log(num);
  });
```

## Output

```js
11
```

---

# Question 10

```js
Promise.resolve("First")
  .then((data) => {
    console.log(data);
  });

console.log("Second");
```

## Output

```js
Second
First
```

## Reason

Promise callbacks are asynchronous.

They execute after synchronous code finishes.