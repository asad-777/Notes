# Methods to loop through an array

There are three methods to loop through an array, but each serves a different purpose:

| Method  | Purpose                           | Returns   |
| ------- | --------------------------------- | --------- |
| forEach | Do something for each item        | undefined |
| map     | Transform each item               | new array |
| filter  | Keep items that match a condition | new array |

---

**forEach **- Just loop (no return)

```javascript
const users = ["Asad", "Ali", "Umar"];

users.forEach((name) => {
  console.log("User:", name);
});

```

- Doesn't returns anything

- Use when you want to just loop through, not change any data
  
  ---
  
  **map** - Transform data (used in jsx)
  
  ```javascript
  const users = ["Asad", "Ali", "Umar"];
  
  const greetings = users.map((name) => "Hello " + name);
  console.log(greetings); // ✅ ["Hello Asad", "Hello Ali", "Hello Umar"]
  
  ```

- Returns a new array

- Most used in React for rendering lists
  
  ---
  
  **filter** - Keep inly what matches

```javascript
const numbers = [1, 2, 3, 4, 5];

const even = numbers.filter((n) => n % 2 === 0);
console.log(even); // ✅ [2, 4]

```

- returns a new array

- Use to remove unwanted items before rendering

- only accepts data that return **true** on condition and rejects the data that returns **false**


