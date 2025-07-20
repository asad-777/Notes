# Object Shorthand and computed properties

### 🔹 Object Shorthand

**Normally**, when creating an object:

```js
const name = "Asad";

const user = {
  name: name, // key and value both
};
```

But if the **key name is the same as the variable name**, you can write it in **shorthand**:

```js
const name = "Asad";

const user = {
  name, // same as name: name
};

console.log(user); // { name: 'Asad' }
```

✅ **Use Case:** Clean, shorter object code.

---

### 🔹 Computed Properties

You can use a **variable as a property name** in an object using `[]` brackets.

```js
const key = "age";
const value = 17;

const user = {
  name: "Asad",
  [key]: value, // becomes: age: 17
};

console.log(user); // { name: 'Asad', age: 17 }
```

⚠️ Without `[]`, it will literally be `"key"`:

```js
const user = {
  key: value, // this means: { key: 17 }, not { age: 17 }
};
```

✅ **Use Case:** Dynamic keys — when the key comes from user input, a loop, or a function.
