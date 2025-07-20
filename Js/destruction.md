# Destruction

Destructuring is a clean way to unpack values from arrays or objects into individual variables.

### Example:

```javascript
const fruits = ["apple", "banana", "cherry"];
const [first, second] = fruits;

console.log(first); // "apple"
console.log(second); // "banana"
```

### Breakdown:

- **first** gets **apple**
- **second** gets **banana**
- You can skip values too:
  ```javascript
  const [, , third] = fruits;
  console.log(third); // "cherry"
  ```

### Object Destruction

```javascript
const user = { name: "Asad", age: 17 };
const { name, age } = user;

console.log(name); // "Asad"
console.log(age); // 17
```

### Breakdown

- Variables name must match the key
- You can rename while destruction :
  ```javascript
  const { name: userName } = user;
  console.log(userName); // "Asad"
  ```
