# Object Output Questions

---

# Question 1

```js
const obj = {
  name: "Adarsh"
};

console.log(obj.age);
```

## Output

```js
undefined
```

---

# Question 2

```js
const obj1 = {
  name: "Adarsh"
};

const obj2 = obj1;

obj2.name = "Rahul";

console.log(obj1.name);
```

## Output

```js
Rahul
```

## Reason

Objects are stored by:
```js
Reference
```

---

# Call By Value and Call by Reference Type Questions.

---

# Question 3

```js
let a = 10;

let b = a;

b = 20;

console.log(a);
console.log(b);
```

## Output

```js
10
20
```

## Reason

Primitive values are copied by:
```js
Value
```

Changing:
```js
b
```

does NOT affect:
```js
a
```

---

# Question 4

```js
const obj1 = {
  name: "Adarsh"
};

const obj2 = obj1;

obj2.name = "Rahul";

console.log(obj1.name);
```

## Output

```js
Rahul
```

## Reason

Objects are copied by:
```js
Reference
```

Both variables point to the same object in memory.

---

# Question 5

```js
function update(num) {
  num = 20;
}

let value = 10;

update(value);

console.log(value);
```

## Output

```js
10
```

## Reason

Primitive values are passed by:
```js
Value
```

Function receives a copy of:
```js
value
```

---

# Question 6

```js
function update(user) {
  user.name = "Rahul";
}

const person = {
  name: "Adarsh"
};

update(person);

console.log(person.name);
```

## Output

```js
Rahul
```

## Reason

Objects are passed by:
```js
Reference
```

Function modifies the original object.

---

# Important Interview Point

| Primitive Types | Objects |
|---|---|
| Passed by Value | Passed by Reference |
| Independent Copy | Shared Memory Reference |

---

# Primitive Types

```js
string
number
boolean
null
undefined
symbol
bigint
```

---

# Reference Types

```js
object
array
function
```