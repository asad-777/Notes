# Variables

There are three methods to declare variables in JavaScript

| Name  | Scope    | Reassign able | Hoisted   |
| ----- | -------- | ------------- | --------- |
| const | block    | no            | yes (tdz) |
| let   | block    | yes           | yes (tdz) |
| var   | function | yes           | yes       |

- Tdz = temporal dead zone hoisted, hoisted but can't be accessed before declaration

```javascript
const user = {
  name: "Asad",
  greet: function () {
    return "Hi " + this.name;
  },
  greetArrow: () => {
    return "Hi " + this.name;
  },
};

console.log(user.greet()); // ✅ Outputs: "Hi Asad"
console.log(user.greetArrow()); // ❌ Outputs: "Hi undefined"
```
