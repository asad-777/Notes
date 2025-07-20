# Function Declaration

There are three methods to declare a function in js.

### Method 1

```javascript
function name(parameter) {
  return `hi` + parameter;
}
```

### Method 2

```javascript
const name = (parameter) => {
  return `hi` + parameter;
};
```

### Method 3

```javascript
const name = (parameter) => `hi` + parameter;
```

---

**<u>this</u>**: refers to the object itself, this can only be used in method one, method 2 and 3 don't accept this by default

### Example Usage

```javascript
const obj = {
  name: "Asad",
  regular() {
    console.log(this.name); // ✅ 'Asad'
  },
  arrow: () => {
    console.log(this.name); // ❌ 'undefined'
  },
};

obj.regular(); // 'Asad'
obj.arrow(); // undefined (arrow function has no own `this`)
```

Arrow Function Templates

```javascript
const func = () => value;
const func = (arg) => value;
const func = (arg1, arg2) => {
  /* multiple lines */ return value;
};
const func = () => ({ key: "value" }); // return object
```
