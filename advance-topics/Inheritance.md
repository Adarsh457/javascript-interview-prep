# 19. Inheritance in JavaScript

---

# What is Inheritance?

## Answer

Inheritance allows one object or class to acquire properties and methods from another object or class.

It helps in:
- code reusability
- cleaner code
- method sharing

---

# Prototype Inheritance

## Example

```js
const user = {
  greet() {
    console.log("Hello");
  }
};

const student = Object.create(user);

student.name = "Adarsh";

student.greet();
```

---

# Output

```js
Hello
```

---

# Explanation

```js
Object.create(user)
```

creates a new object whose prototype points to:
```js
user
```

So:
```js
student
```

inherits methods from:
```js
user
```

---

# Class Inheritance

## Example

```js
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello ${this.name}`);
  }
}

class Student extends Person {
  constructor(name, course) {
    super(name);

    this.course = course;
  }
}

const student1 = new Student("Adarsh", "MCA");

student1.greet();
```

---

# Output

```js
Hello Adarsh
```

---

# Explanation

## `extends`

```js
class Student extends Person
```

means:
```js
Student
```

inherits from:
```js
Person
```

---

# `super()`

## Answer

`super()` calls the constructor of the parent class.

---

# Example

```js
super(name);
```

passes:
```js
name
```

to:
```js
Person constructor
```

---

# Method Inheritance

## Example

```js
class Animal {
  sound() {
    console.log("Animal Sound");
  }
}

class Dog extends Animal {}

const dog1 = new Dog();

dog1.sound();
```

### Output

```js
Animal Sound
```

Because:
```js
Dog
```

inherits methods from:
```js
Animal
```

---

# Method Overriding

## Example

```js
class Animal {
  sound() {
    console.log("Animal Sound");
  }
}

class Dog extends Animal {
  sound() {
    console.log("Dog Barks");
  }
}

const dog1 = new Dog();

dog1.sound();
```

### Output

```js
Dog Barks
```

---

# Important Point

JavaScript supports:
```js
Prototype Based Inheritance
```

Classes internally use prototypes.

---

# Advantages of Inheritance

- Code reusability
- Cleaner code
- Easier maintenance
- Better structure

---

# Real World Usage

Inheritance is heavily used in:
- React class components
- OOP concepts
- Backend frameworks
- UI component systems