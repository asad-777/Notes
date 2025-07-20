# Logical Operators (`&&`, `||`, `!`)

These are used to combine or manipulate boolean values (true/false).

---

### ✅ 1. `&&` (AND)

Returns the second value **only if** the first is **truthy**. Otherwise, returns the first.

```js
true && "Hello"; // → "Hello"
false && "Hello"; // → false
0 && 100; // → 0
```

---

### ✅ 2. `||` (OR)

Returns the first **truthy** value it finds, or the last one if none are truthy.

```js
false || "Hi"; // → "Hi"
0 || null || 5; // → 5
"Hello" || "World"; // → "Hello"
```

---

### ✅ 3. `!` (NOT)

Negates a value — turns **truthy to false**, and **falsy to true**.

```js
!true; // → false
!0; // → true
!undefined; // → true
```

### `&&` in `if`

```js
let user = { name: "Asad" };

if (user && user.name) {
  console.log("User has a name");
}
```

- `user && user.name` returns `"Asad"` (a truthy **string**, not `true`).
- `if ("Asad")` is still considered **true**, so it runs the block.

---

### 🔍 Example 2 – `||` in `if`

```js
let a = 0;
let b = "fallback";

if (a || b) {
  console.log("One is truthy");
}
```

- `a || b` returns `"fallback"` (truthy), even though `a` is `0` (falsy).
- `if ("fallback")` → **truthy**, so it runs.

---

### ✅ Key Concept

- JavaScript **doesn't require** `true` or `false` in `if (...)`.
- It accepts any **truthy or falsy value**.
- That’s why `&&` and `||` returning values is more **flexible and powerful**.

Let me know if you want truthy/falsy explained or move to next topic.
