## ✅ JavaScript Modules & Exports — Summary

### 📦 What is a Module?

A **module** is any `.js` file that can export or import values (functions, variables, classes).

---

### 🧾 Types of Exports

#### 1. **Named Export**

Export multiple specific items by name.

```js
// math.js
export function add(a, b) {
  return a + b;
}
export const PI = 3.14;
```

```js
// app.js
import { add, PI } from "./math.js";
```

- Use `{}` in import.
- Can export many items.
- Must import with **same names**.

---

#### 2. **Default Export**

Export a **single main value** (function, object, class, etc.)

```js
// math.js
export default function add(a, b) {
  return a + b;
}
```

```js
// app.js
import add from "./math.js";
```

- No `{}` in import.
- Can name it anything while importing.
- Only one default export per file.

---

#### 3. **Exporting an Object**

Group multiple functions into an object and export as default.

```js
// utils.js
function greet(name) {
  return `Hello ${name}`;
}
function bye(name) {
  return `Bye ${name}`;
}

const utils = { greet, bye };
export default utils;
```

```js
// app.js
import tools from "./utils.js";
tools.greet("Asad");
```

---

### 🗃️ Exporting at End

You can also define everything first, then export:

```js
function a() {}
function b() {}

export { a, b }; // Named export
export default b; // Default export
```

---

### ⚠️ Rules

- **One `default export` only** per file.
- **Multiple `named exports`** allowed.
- Named and default can **exist together**.
