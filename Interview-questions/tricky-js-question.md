# Tricky JavaScript Questions

---

# Question 1

```js
console.log([] + []);
```

## Output

```js
""
```

## Reason

Empty arrays convert to empty strings.

---

# Question 2

```js
console.log([] + {});
```

## Output

```js
[object Object]
```

---

# Question 3

```js
console.log({} + []);
```

## Output

```js
0
```

## Reason

JavaScript interprets:
```js
{}
```

as an empty block.

---

# Question 4

```js
console.log(typeof null);
```

## Output

```js
object
```

## Reason

This is a historical bug in JavaScript.

---

# Question 5

```js
console.log(NaN == NaN);
```

## Output

```js
false
```

## Reason

`NaN` is never equal to itself.

---

# Question 6

```js
console.log(typeof NaN);
```

## Output

```js
number
```

---

# Question 7

```js
console.log(0.1 + 0.2);
```

## Output

```js
0.30000000000000004
```

## Reason

Floating point precision issue.

---

# Question 8

```js
console.log([] == false);
```

## Output

```js
true
```

---

# Question 9

```js
console.log("5" - 2);
```

## Output

```js
3
```

## Reason

`-` triggers numeric conversion.

---

# Question 10

```js
console.log("5" + 2);
```

## Output

```js
52
```

## Reason

`+` triggers string concatenation.

---

# Question 11

```js
console.log([] === []);
```

## Output

```js
false
```

## Reason

Arrays are compared by reference.

---

# Question 12

```js
console.log({} === {});
```

## Output

```js
false
```

---

# Question 13

```js
let a = [1, 2];

let b = a;

b.push(3);

console.log(a);
```

## Output

```js
[1, 2, 3]
```

## Reason

Arrays are copied by reference.

---

# Question 14

```js
console.log(typeof undefined);
```

## Output

```js
undefined
```

---

# Question 15

```js
console.log(typeof function () {});
```

## Output

```js
function
```