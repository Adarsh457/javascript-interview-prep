# 18. Prototypes in JavaScript

---

# What is a Prototype?

## Answer

A prototype is an object from which other objects inherit properties and methods.

In JavaScript, every object has a hidden property called:
```js
[[Prototype]]
```

which points to another object.

---

# Why are Prototypes Used?

## Answer

Prototypes are used for:
- inheritance
- sharing methods
- memory optimization

Instead of creating copies of methods for every object, JavaScript shares them using prototypes.

---

# Example

```js
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function () {
  console.log(`Hello ${this.name}`);
};

const user1 = new Person("Adarsh");

user1.greet();
```

---

# Output

```js
Hello Adarsh
```

---

# Step-by-Step Explanation

## Step 1

```js
function Person(name) {
  this.name = name;
}
```

A constructor function is created.

---

## Step 2

```js
Person.prototype.greet = function () {
  console.log(`Hello ${this.name}`);
};
```

A method named:
```js
greet()
```

is added to the prototype of `Person`.

All objects created using:
```js
new Person()
```

can access this method.

---

## Step 3

```js
const user1 = new Person("Adarsh");
```

A new object is created.

Internally:
```js
user1.__proto__ = Person.prototype
```

---

## Step 4

```js
user1.greet();
```

JavaScript first checks:
```js
user1 object
```

If method is not found, it checks:
```js
Person.prototype
```

There it finds:
```js
greet()
```

and executes it.

---

# Prototype Chain

## Answer

When JavaScript cannot find a property inside an object, it searches in its prototype.

This process continues until:
```js
null
```

This is called:
```js
Prototype Chain
```

---

# Example

```js
const arr = [1, 2, 3];

console.log(arr.length);
```

### Question

Where does:
```js
length
```

come from?

### Answer

From:
```js
Array.prototype
```

---

# `__proto__`

## Answer

`__proto__` points to the prototype object.

### Example

```js
const user = {
  name: "Adarsh"
};

console.log(user.__proto__);
```

---

# Important Point

Arrays, functions, and objects all use prototypes internally.

Example:
- `Array.prototype`
- `Object.prototype`
- `Function.prototype`

---

# Advantages of Prototypes

- Memory efficient
- Supports inheritance
- Method sharing
- Faster object creation

---

# Important Question

## Output

```js
function User(name) {
  this.name = name;
}

User.prototype.city = "Delhi";

const user1 = new User("Adarsh");

console.log(user1.city);
```

### Output

```js
Delhi
```

Because:
```js
city
```

is found inside:
```js
User.prototype
```