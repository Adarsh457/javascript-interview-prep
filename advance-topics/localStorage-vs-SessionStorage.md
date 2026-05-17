# 22. localStorage vs sessionStorage in JavaScript

---

# What is localStorage?

## Answer

`localStorage` stores data permanently inside the browser.

Data remains even after:
- browser refresh
- browser close

---

# Example

```js
localStorage.setItem("name", "Adarsh");

console.log(localStorage.getItem("name"));
```

---

# Output

```js
Adarsh
```

---

# Removing Data

```js
localStorage.removeItem("name");
```

---

# Clearing All Data

```js
localStorage.clear();
```

---

# What is sessionStorage?

## Answer

`sessionStorage` stores data only for the current browser session.

Data is removed when:
```js
Browser Tab Closes
```

---

# Example

```js
sessionStorage.setItem("city", "Delhi");

console.log(sessionStorage.getItem("city"));
```

---

# Output

```js
Delhi
```

---

# Difference Between localStorage and sessionStorage

| localStorage | sessionStorage |
|---|---|
| Permanent storage | Temporary storage |
| Survives browser close | Removed after tab close |
| Storage limit ~5MB | Storage limit ~5MB |

---

# Common Methods

| Method | Description |
|---|---|
| `setItem()` | Store data |
| `getItem()` | Get data |
| `removeItem()` | Remove data |
| `clear()` | Remove all data |

---

# Important Interview Point

Both:
```js
localStorage
sessionStorage
```

store data as:
```js
Strings
```

---

# Storing Objects

## Example

```js
const user = {
  name: "Adarsh"
};

localStorage.setItem("user", JSON.stringify(user));

const data = JSON.parse(localStorage.getItem("user"));

console.log(data);
```

---

# Output

```js
{
  name: "Adarsh"
}
```