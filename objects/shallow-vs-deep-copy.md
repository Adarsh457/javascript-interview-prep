# 13. Shallow Copy vs Deep Copy in JavaScript

---

# Shallow Copy

## Answer

A shallow copy copies only the first level of an object.

Nested objects are copied by reference.

---

## Example

```js
const user = {
  name: "Adarsh",

  address: {
    city: "Delhi"
  }
};

const copiedUser = { ...user };

copiedUser.address.city = "Mumbai";

console.log(user.address.city);
```

### Output

```js
Mumbai
```

Both objects share the same nested object reference.

---

# Deep Copy

## Answer

A deep copy creates completely independent copies of all nested objects.

Changes in copied object do NOT affect the original object.

---

## Example

```js
const user = {
  name: "Adarsh",

  address: {
    city: "Delhi"
  }
};

const copiedUser = structuredClone(user);

copiedUser.address.city = "Mumbai";

console.log(user.address.city);
```

### Output

```js
Delhi
```

Original object remains unchanged.

---

# Another Deep Copy Method

### Example

```js
const user = {
  name: "Adarsh",
  age: 24
};

const copiedUser = JSON.parse(JSON.stringify(user));

console.log(copiedUser);
```

### Output

```js
{
  name: "Adarsh",
  age: 24
}
```

---

# Difference Between Shallow Copy and Deep Copy

| Shallow Copy | Deep Copy |
|---|---|
| Copies first level only | Copies complete object |
| Nested objects share reference | Nested objects are independent |
| Faster | Slightly slower |
| Uses spread operator | Uses `structuredClone()` |

---

# Important Point

Spread operator (`...`) and:
```js
Object.assign()
```

create shallow copies only.