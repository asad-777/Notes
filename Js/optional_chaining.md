# Optional Chaining

Optional chaining allows safe access to deeply nested object properties without causing an error if a property doesn't exist.

## Syntax

```javascript
const user = {
  name: "Asad",
  address: {
    city: "Lahore",
  },
};

console.log(user.address?.city); // ✅ "Lahore"
console.log(user.address?.zip); // ✅ undefined (no error)
console.log(user.contact?.phone); // ✅ undefined (no error)
// without ?. → this would throw an error
```
