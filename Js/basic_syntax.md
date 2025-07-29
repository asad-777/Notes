## ✅ **JavaScript Syntax & Operators**

(Straightforward, no fluff — just what’s needed for logic in React or general JS)

---

### 🧱 1. **Basic Syntax Rules**

| Concept          | Example                         |
| ---------------- | ------------------------------- |
| End statements   | Use `;` (optional but cleaner)  |
| Block of code    | Use `{ }`                       |
| Comment (single) | `// this is a comment`          |
| Comment (multi)  | `/* this is a block comment */` |
| Case-sensitive   | `name` ≠ `Name`                 |

---

### 🔣 2. **Arithmetic Operators**

Used for calculations.

| Operator | Meaning     | Example  | Result |
| -------- | ----------- | -------- | ------ |
| `+`      | Add         | `2 + 3`  | `5`    |
| `-`      | Subtract    | `5 - 2`  | `3`    |
| `*`      | Multiply    | `3 * 4`  | `12`   |
| `/`      | Divide      | `10 / 2` | `5`    |
| `%`      | Remainder   | `10 % 3` | `1`    |
| `**`     | Power (ES6) | `2 ** 3` | `8`    |

---

### 🧮 3. **Assignment Operators**

| Operator | Meaning           | Example  | Same As     |
| -------- | ----------------- | -------- | ----------- |
| `=`      | Assign            | `x = 5`  | —           |
| `+=`     | Add & assign      | `x += 3` | `x = x + 3` |
| `-=`     | Subtract & assign | `x -= 2` | `x = x - 2` |
| `*=`     | Multiply & assign | `x *= 4` | `x = x * 4` |
| `/=`     | Divide & assign   | `x /= 2` | `x = x / 2` |

---

### 🔄 4. **Comparison Operators**

Used in `if`, `while`, `? :`, etc.

| Operator | Meaning            | Example     | Result  |
| -------- | ------------------ | ----------- | ------- |
| `==`     | Equal (loose)      | `5 == "5"`  | `true`  |
| `===`    | Equal (strict)     | `5 === "5"` | `false` |
| `!=`     | Not equal (loose)  | `5 != "5"`  | `false` |
| `!==`    | Not equal (strict) | `5 !== "5"` | `true`  |
| `>`      | Greater than       | `7 > 3`     | `true`  |
| `<`      | Less than          | `2 < 4`     | `true`  |
| `>=`     | Greater or equal   | `5 >= 5`    | `true`  |
| `<=`     | Less or equal      | `3 <= 2`    | `false` |

---

### ⚙️ 5. **Logical Operators**

Used to combine conditions.

| Operator | Meaning | Example         | Result  |        |     |         |        |
| -------- | ------- | --------------- | ------- | ------ | --- | ------- | ------ |
| `&&`     | AND     | `true && false` | `false` |        |     |         |        |
| \`       |         | \`              | OR      | \`true |     | false\` | `true` |
| `!`      | NOT     | `!true`         | `false` |        |     |         |        |

---

### 🧠 6. **Typeof Operator**

To check the type of a value.

```js
typeof 123; // "number"
typeof "hello"; // "string"
typeof true; // "boolean"
typeof {}; // "object"
typeof []; // "object"
typeof undefined; // "undefined"
```

---

### 📌 7. **Ternary Operator** (Already Covered)

```js
let result = age >= 18 ? "Adult" : "Minor";
```

---

### 💡 8. **Optional Chaining & Nullish Coalescing** (Already Covered, quick review)

| Syntax              | Meaning                                      |
| ------------------- | -------------------------------------------- |
| `obj?.prop`         | Safe access — returns `undefined` if missing |
| `value ?? fallback` | Return fallback **only if null/undefined**   |

---

### ✅ Summary: Use in Conditions

```js
let x = 10;

if (x > 5 && x < 20) {
  console.log("x is between 5 and 20");
}

let result = x > 15 ? "Big" : "Small";
```

---
