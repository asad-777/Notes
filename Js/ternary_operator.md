# Ternary Operator (? :)

The ternary operator is a short way to write an if...else statement.
It’s used for simple conditional expressions.

## Syntax

```javascript
condition ? value_if_true : value_if_false;
```

## Example

```js
let score = 85;
let grade = score >= 90 ? "A" : score >= 80 ? "B" : score >= 70 ? "C" : "F";

console.log(grade); // 🔸 "B"
```
