# 🔹 What is a Promise?

A **Promise** is a special JavaScript object used to handle **asynchronous operations**. It represents a value that may be available **now**, **later**, or **never**.

---

### 🔹 Why Do We Need Promises?

JavaScript normally runs **line by line** (synchronously). But some operations, like fetching data from a server or reading a file, take time. Instead of **blocking** the whole code while waiting, JavaScript uses **Promises** to handle those operations in the background.

---

### 🔹 Basic Syntax of a Promise

```js
const myPromise = new Promise((resolve, reject) => {
  // Do something async
  if (success) {
    resolve(result); // means it worked
  } else {
    reject(error); // means it failed
  }
});
```

- `resolve()` is called if the operation was successful.
- `reject()` is called if there was an error or failure.

---

### 🔹 Example 1: Creating a Promise

```js
const promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("✅ Success!");
    // reject("❌ Failed!");
  }, 2000); // runs after 2 seconds
});

promise
  .then((result) => {
    console.log(result); // "✅ Success!"
  })
  .catch((error) => {
    console.log(error); // if rejected
  });
```

---

### 🔹 `.then()` and `.catch()`

- `.then()` runs when the promise is **resolved**.
- `.catch()` runs when the promise is **rejected**.

---

### 🔹 Example 2: Simulate Order Pizza

```js
function orderPizza() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const ready = true;
      if (ready) {
        resolve("🍕 Pizza delivered");
      } else {
        reject("🚫 Pizza shop closed");
      }
    }, 3000);
  });
}

orderPizza()
  .then((msg) => console.log(msg))
  .catch((err) => console.log(err));
```

> After 3 seconds, it prints `🍕 Pizza delivered` if `ready` is true.

---

### 🔹 Summary

| Part        | Meaning                    |
| ----------- | -------------------------- |
| `Promise`   | An object for future value |
| `resolve()` | Operation successful       |
| `reject()`  | Operation failed           |
| `.then()`   | Run if success (resolve)   |
| `.catch()`  | Run if failed (reject)     |

If you **don't know how much time** a task will take in JavaScript (like fetching data from a server, reading a file, or waiting for user input), you **don’t use `setTimeout`** — instead, you use a **`Promise`**.

---

### 🔹 What is a Promise?

A **`Promise`** is a way to **handle async operations**. It represents a **future value** — something that will be **available later**, either:

- ✅ fulfilled (success),
- ❌ rejected (error), or
- ⏳ still pending (in progress).

---

### 🔹 Basic Syntax of a Promise

```js
const myPromise = new Promise((resolve, reject) => {
  // Do something async, like fetching data
  if (/* success condition */) {
    resolve(result);  // Call this if successful
  } else {
    reject(error);    // Call this if failed
  }
});
```

---

### 🔹 Example: Simulate fetching data (time is unknown)

```js
const fetchData = new Promise((resolve, reject) => {
  let success = true;

  setTimeout(() => {
    if (success) {
      resolve("✅ Data received");
    } else {
      reject("❌ Failed to get data");
    }
  }, Math.random() * 3000); // Random delay between 0–3 seconds
});

fetchData
  .then((result) => console.log(result)) // Called if resolve() runs
  .catch((error) => console.log(error)); // Called if reject() runs
```

> ✅ `then()` handles success
> ❌ `catch()` handles error

---

### 🔹 Why Use a Promise?

Because you **don't know when**:

- A user will click something
- A server will respond
- A file will load

So you tell JavaScript:

> "Start this task. When it finishes, **then** do this."
