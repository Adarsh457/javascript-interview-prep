# 10. Object Methods in JavaScript

---

## `Object.keys()`

### Answer

Returns all keys of an object as an array.

### Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

console.log(Object.keys(user));
```

### Output

```js
["name", "age"]
```

---

## `Object.values()`

### Answer

Returns all values of an object as an array.

### Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

console.log(Object.values(user));
```

### Output

```js
["Adarsh", 24]
```

---

## `Object.entries()`

### Answer

Returns key-value pairs as nested arrays.

### Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

console.log(Object.entries(user));
```

### Output

```js
[
  ["name", "Adarsh"],
  ["age", 24]
]
```

---

## `hasOwnProperty()`

### Answer

Checks whether the object contains a specific property.

### Example

```js
const user = {
  name: "Adarsh"
};

console.log(user.hasOwnProperty("name"));
console.log(user.hasOwnProperty("age"));
```

### Output

```js
true
false
```

---

## `Object.assign()`

### Answer

Copies properties from one or more objects into another object.

### Example

```js
const obj1 = {
  a: 1
};

const obj2 = {
  b: 2
};

const result = Object.assign({}, obj1, obj2);

console.log(result);
```

### Output

```js
{
  a: 1,
  b: 2
}
```

---

## `Object.freeze()`

### Answer

Prevents adding, deleting, or modifying object properties.

### Example

```js
const user = {
  name: "Adarsh"
};

Object.freeze(user);

user.name = "Rahul";

console.log(user);
```

### Output

```js
{
  name: "Adarsh"
}
```

---

## `Object.seal()`

### Answer

Allows modification of existing properties but prevents adding or deleting properties.

### Example

```js
const user = {
  name: "Adarsh"
};

Object.seal(user);

user.name = "Rahul";
user.age = 24;

console.log(user);
```

### Output

```js
{
  name: "Rahul"
}
```