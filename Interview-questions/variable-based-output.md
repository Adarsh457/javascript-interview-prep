# Variable Output Questions

---

# Question 1

```js
console.log(a);

var a = 10;
```

## Output

```js
undefined
```

## Reason

`var` is hoisted and initialized with:
```js
undefined
```

during memory creation phase.

---

# Question 2

```js
console.log(a);

let a = 10;
```

## Output

```js
ReferenceError
```

## Reason

`let` stays inside:
```js
Temporal Dead Zone (TDZ)
```

until initialization.

---

# Question 3

```js
const user = {
  name: "Adarsh"
};

user.name = "Rahul";

console.log(user.name);
```

## Output

```js
Rahul
```

## Reason

`const` prevents reassignment,
but object properties can still be modified.

# Question 4

```js
console.log(0 == false);
```

## Output

```js
true
```

## Reason

Using:
```js
==
```

JavaScript performs:
```js
Type Coercion
```

Internally:

```js
0 == 0
```

So output becomes:
```js
true
```

---

# Question 5

```js
console.log(1 == true);
```

## Output

```js
true
```

## Reason

JavaScript converts:
```js
true → 1
```

So internally:

```js
1 == 1
```

---

# Question 6

```js
console.log("" == false);
```

## Output

```js
true
```

## Reason

JavaScript converts:

```js
"" → 0
false → 0
```

So comparison becomes:

```js
0 == 0
```

---

# Question 7

```js
console.log(null == undefined);
```

## Output

```js
true
```

## Reason

In loose equality:
```js
==
```

JavaScript treats:
```js
null and undefined
```

as equal.

---

# Question 8

```js
console.log(null === undefined);
```

## Output

```js
false
```

## Reason

Strict equality:
```js
===
```

checks both:
- value
- datatype

Their datatypes are different.

---

# Question 9

```js
console.log([] == false);
```

## Output

```js
true
```

## Reason

JavaScript converts:
```js
[] → ""
"" → 0
false → 0
```

So internally:

```js
0 == 0
```

---

# Question 10

```js
console.log([] == ![]);
```

## Output

```js
true
```

## Reason

Step 1:
```js
![] = false
```

because arrays are truthy.

Step 2:

```js
[] == false
```

Step 3:

JavaScript converts both to:
```js
0
```

So output becomes:
```js
true
```