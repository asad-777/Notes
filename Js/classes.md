## ✅ **Classes & Prototypes in JavaScript**

### 📌 What Is a Class?

> A **class** is a blueprint for creating objects with the same structure and behavior.

JavaScript uses **prototypes** under the hood, and **`class`** is just a cleaner way to write it.

---

## 🧱 1. Creating a Class

```js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, I'm ${this.name} and I'm ${this.age} years old.`);
  }
}

const asad = new Person("Asad", 17);
asad.greet(); // Hi, I'm Asad and I'm 17 years old.
```

### 🔍 Breakdown:

- `class Person` defines a blueprint.
- `constructor()` is a function that runs when `new Person()` is called.
- `this.name` and `this.age` store values inside the object.
- `greet()` is a method that all `Person` objects will share (not copied).

---

## 🧬 2. What Are Prototypes?

> Every object in JavaScript has a **hidden `[[Prototype]]`**, which is another object it inherits from.

All methods (like `greet()`) are stored on the class's **prototype**, not inside each object — this saves memory.

---

### ✅ You can also create objects with functions (older style)

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.greet = function () {
  console.log(`Hi, I'm ${this.name}`);
};

const ali = new Person("Ali", 18);
ali.greet(); // Hi, I'm Ali
```

This is function-based prototype inheritance (before ES6).
The `class` keyword is just syntactic sugar for this.

---

## 🧠 3. Inheritance (Extend a Class)

```js
class Student extends Person {
  constructor(name, age, rollNo) {
    super(name, age); // call parent constructor
    this.rollNo = rollNo;
  }

  showRoll() {
    console.log(`${this.name}'s roll number is ${this.rollNo}`);
  }
}

const student1 = new Student("Asad", 17, "23A");
student1.greet(); // from Person
student1.showRoll(); // from Student
```

### 🔗 `extends` → Inherits from another class

### 🔗 `super()` → Calls the parent class’s constructor

---

## 🔄 4. Objects and `this`

Inside any method, `this` refers to the **current object**:

```js
const user = {
  name: "Asad",
  greet() {
    console.log(this.name); // refers to `user`
  },
};
```

Arrow functions **do not** have their own `this`, so avoid them for object methods when you need access to `this`.

---

## ✅ Summary

| Concept       | Purpose                       |
| ------------- | ----------------------------- |
| `class`       | Define object blueprints      |
| `constructor` | Set initial properties        |
| `this`        | Refers to the current object  |
| `prototype`   | Where shared methods live     |
| `extends`     | Inherit from another class    |
| `super()`     | Call parent class constructor |

---
