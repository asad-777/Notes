# Nullish Coalescing Operator

## Purpose

Returns the right-hand side value only if the left-hand side is `null` or `undefined` (not 0, false, or "" like `||` does).

## Examples

```javascript
let name = null;
console.log(name ?? "Guest"); // 🔸 "Guest"

let age = 0;
console.log(age ?? 18); // 🔸 0 (because 0 is NOT null/undefined)

let username;
console.log(username ?? "Anonymous"); // 🔸 "Anonymous"
```

---

you can use multiple `??` operators in a single expression — JavaScript will check them from `left to right` until it finds the first value that is not null or undefined

## Example

```javascript
let a = null;
let b = undefined;
let c = "Hello";

let result = a ?? b ?? c ?? "Default";
console.log(result); // 🔸 "Hello"
```
