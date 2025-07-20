# Spread and Rest Operator

Both use the same syntax ..., but behave differently depending on context.

## Spread Operator

Used to expand arrays or objects into individual elements

- **Arrays**:

  ```javascript
  const nums = [1, 2, 3];
  const moreNums = [...nums, 4, 5];
  console.log(moreNums); // [1, 2, 3, 4, 5]
  ```

- **Objects**:
  ```javascript
  const user = { name: "Asad", age: 17 };
  const updatedUser = { ...user, age: 18 };
  console.log(updatedUser); // { name: 'Asad', age: 18 }
  ```

---

## Rest Operator

Used to gather multiple values into an array or object

Think of it as:
"Take the rest of the items and group them together"

- **In Function** - To Collect extra arguments

  ```javascript
  function logAll(first, second, ...others) {
    console.log(first); // First argument
    console.log(second); // Second argument
    console.log(others); // All remaining arguments as an array
  }

  logAll(1, 2, 3, 4, 5);
  // Output:
  // 1
  // 2
  // [3, 4, 5]
  ```

  - 📌 Use-case: Functions that accept unknown number of arguments.

- **In Arrays** - Destructing Remaining Items

  ```javascript
  const [first, ...rest] = [10, 20, 30, 40];

  console.log(first); // 10
  console.log(rest); // [20, 30, 40]
  ```

  - Use-case: You only need the first item, and then the rest as a new array.

- **In Objects** - Destructing Remaining Keys

  ```javascript
  const user = {
    name: "Asad",
    age: 17,
    country: "Pakistan",
  };

  const { name, ...otherInfo } = user;

  console.log(name); // "Asad"
  console.log(otherInfo); // { age: 17,  country: "Pakistan" }
  ```

  - Rest must be last: You can’t do **...x, y** — only **x, y, ...rest**.
  - You can only have one rest variable in the destructuring.
