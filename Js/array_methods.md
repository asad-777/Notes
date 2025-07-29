# find, some, every, includes, reduce

---

## 🔍 `find()`

### ➤ **What it does**:

Returns the **first element** in the array that satisfies a condition. If none match, returns `undefined`.

### ➤ **Syntax**:

```js
array.find(callback);
```

- `callback`: a function that returns `true` for the item you’re looking for.
- Stops after **first match**.

### ➤ **Example**:

```js
const users = [{ id: 1 }, { id: 2 }, { id: 3 }];
const user = users.find((u) => u.id === 2);
console.log(user); // {id: 2}
```

---

## ✅ `some()`

### ➤ **What it does**:

Returns `true` **if at least one** element passes the condition. Otherwise, `false`.

### ➤ **Syntax**:

```js
array.some(callback);
```

- Runs the `callback` on each item.
- Returns **true immediately** when any item passes.

### ➤ **Example**:

```js
const numbers = [1, 3, 5, 7];
const hasEven = numbers.some((n) => n % 2 === 0);
console.log(hasEven); // false
```

---

## ✅ `every()`

### ➤ **What it does**:

Returns `true` **only if all** items pass the condition.

### ➤ **Syntax**:

```js
array.every(callback);
```

- Returns **false immediately** if any item fails.

### ➤ **Example**:

```js
const scores = [80, 90, 85];
const allPassed = scores.every((score) => score >= 50);
console.log(allPassed); // true
```

---

## 🔎 `includes()`

### ➤ **What it does**:

Checks whether an array **contains a specific value**.

### ➤ **Syntax**:

```js
array.includes(value);
```

- Checks by value (not by condition or object property).
- Uses `===` internally.

### ➤ **Example**:

```js
const items = ["apple", "banana"];
console.log(items.includes("banana")); // true
console.log(items.includes("grape")); // false
```

---

## 🧠 `reduce()`

### ➤ **What it does**:

Processes all elements and **reduces the array to a single value** (sum, object, etc.)

### ➤ **Syntax**:

```js
array.reduce((accumulator, current, index, array) => {
  return newAccumulatorValue;
}, initialValue);
```

- `accumulator`: the result so far.
- `current`: current item.
- `initialValue`: starting value for `accumulator`.

### ➤ **Example 1: Sum of numbers**:

```js
const nums = [1, 2, 3];
const total = nums.reduce((acc, curr) => acc + curr, 0);
console.log(total); // 6
```

### ➤ **Example 2: Grouping by property**:

```js
const users = [{ role: "admin" }, { role: "user" }, { role: "admin" }];

const grouped = users.reduce((acc, curr) => {
  acc[curr.role] = (acc[curr.role] || 0) + 1;
  return acc;
}, {});

console.log(grouped); // { admin: 2, user: 1 }
```

Let’s break down `reduce()` **step by step**, in a detailed and beginner-friendly way — **without any React references**.

---

## 🧠 What is `reduce()`?

The `reduce()` method **reduces** an array to a **single value** — like a number, string, object, etc.

It processes each element **one by one**, keeping track of a **running result** (called the _accumulator_).

---

## 🔧 Syntax

```js
array.reduce((accumulator, currentValue, index, array) => {
  // logic
  return updatedAccumulator;
}, initialValue);
```

### 🔹 Parameters:

- `accumulator`: The running result, updated after every iteration.
- `currentValue`: The current element in the array.
- `initialValue`: The value to start the accumulator with. It’s **required** for reliable behavior.

---

## ✅ Example 1: Sum of numbers

```js
const numbers = [10, 20, 30];

const total = numbers.reduce((acc, curr) => {
  return acc + curr;
}, 0);

console.log(total); // 60
```

### 💡 Breakdown:

| Iteration | acc | curr | return (new acc) |
| --------- | --- | ---- | ---------------- |
| 1         | 0   | 10   | 10               |
| 2         | 10  | 20   | 30               |
| 3         | 30  | 30   | 60               |

---

## ✅ Example 2: Find the longest word

```js
const words = ["apple", "banana", "kiwi", "watermelon"];

const longest = words.reduce((acc, curr) => {
  return curr.length > acc.length ? curr : acc;
}, "");

console.log(longest); // "watermelon"
```

### 💡 Logic:

- `acc` starts as an empty string `""`
- Each time, it compares the current word’s length with the accumulator’s length.
- The longer one becomes the new `acc`.

---

## ✅ Example 3: Group by object property

```js
const people = [
  { name: "Ali", age: 18 },
  { name: "Sara", age: 20 },
  { name: "Bilal", age: 18 },
];

const groupedByAge = people.reduce((acc, person) => {
  const key = person.age;
  if (!acc[key]) {
    acc[key] = [];
  }
  acc[key].push(person);
  return acc;
}, {});

console.log(groupedByAge);
```

### 🔎 Output:

```js
{
  18: [{ name: "Ali", age: 18 }, { name: "Bilal", age: 18 }],
  20: [{ name: "Sara", age: 20 }]
}
```

---

## ⚠️ Common Mistakes

- Forgetting to return the `accumulator`.
- Not passing an `initialValue` (can cause bugs if array is empty).
- Confusing `reduce()` with `map()` (map returns an array, reduce returns a value).
