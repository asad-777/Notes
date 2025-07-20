# Method Channing

Method chaining is when you call multiple methods on the same data, one after another, in a single statement.

You can do this when each method returns a value (usually the modified object or array) that the next method can act on.

### Example with **.map** and **.filter**:

```javascript
const result = [1, 2, 3, 4, 5]
  .map((num) => num * 2) // [2, 4, 6, 8, 10]
  .filter((num) => num > 5); // [6, 8, 10]

console.log(result);
```

#### How it works:

- **.map** returns a new array --> [2,4,6,8,10]

- **.filter** is then called on this new array --> [6,8,10]

---

#### General Syntax:

```javascript
someArray.method1().method2().method3();
```
