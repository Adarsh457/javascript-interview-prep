# 09. Objects in JavaScript

---

## What is an Object?

### Answer

An object is a collection of key-value pairs used to store related data.

### Example

```js
const user = { // Object Definiton.
  name: "Adarsh",
  age: 24,
  city: "Delhi"
};

console.log(user);
```

---

## Accessing Object Properties

### Two ways to access properties of object.

### 01. Dot Notation

```js
const user = {
  name: "Adarsh"
};

console.log(user.name);
```

---

### 02. Bracket Notation

```js
const user = {
  name: "Adarsh"
};

console.log(user["name"]);
```

---

## Adding Properties

### Example

```js
const user = {
  name: "Adarsh"
};

user.age = 24; // Add prop to existing obj.

console.log(user);
```

---

## Updating Properties

### Example

```js
const user = {
  name: "Adarsh"
};

user.name = "Rahul";

console.log(user);
```

---

## Deleting Properties

### Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

delete user.age;

console.log(user);
```

---

## Object Inside Object(Nested Object)

### Example

```js
const user = {
  name: "Adarsh",

  address: {
    city: "Delhi",
    pincode: 110001
  }
};

console.log(user.address.city);
```

---

## Looping Through Objects

### `for...in`

```js
const user = {
  name: "Adarsh",
  age: 24
};

for (let key in user) {
  console.log(key, user[key]);
}
```