# Objects in JavaScript

> 📚 Chapter 1 of Objects

---

## 📖 Imagine This...

Suppose you want to store details about a student.

Without objects:

```javascript
let name = "Chinmay";
let age = 20;
let branch = "CSE";
```

These variables are related, but they're scattered.

Instead, we can group them together.

That's exactly what an **object** does.

---

# 🤔 What is an Object?

An object is a collection of **key-value pairs**.

Think of it like a student's ID card.

```text
Student
│
├── Name   → Chinmay
├── Age    → 20
└── Branch → CSE
```

Here,

- `name`, `age`, and `branch` are **keys**.
- `"Chinmay"`, `20`, and `"CSE"` are **values**.

---

# 🧠 Creating an Object

```javascript
const student = {
    name: "Chinmay",
    age: 20,
    branch: "CSE"
};
```

---

# 💻 Accessing Properties

There are two ways.

### Dot Notation

```javascript
console.log(student.name);
```

Output

```text
Chinmay
```

---

### Bracket Notation

```javascript
console.log(student["age"]);
```

Output

```text
20
```

Use bracket notation when the property name is stored in a variable.

```javascript
let key = "branch";

console.log(student[key]);
```

Output

```text
CSE
```

---

# 💻 Adding a Property

Objects can grow anytime.

```javascript
student.college = "BIET";

console.log(student);
```

---

# 💻 Updating a Property

```javascript
student.age = 21;

console.log(student.age);
```

Output

```text
21
```

---

# 💻 Deleting a Property

```javascript
delete student.branch;

console.log(student);
```

The `branch` property is removed.

---

# 🌍 Real-Life Example

Think of a WhatsApp profile.

```text
Profile

↓

Name

Photo

Status

Phone Number
```

All these details belong to one person.

An object stores related information in one place.

---

# ⚠️ Common Mistakes

### ❌ Using Dot Notation with Variables

Wrong

```javascript
let key = "name";

console.log(student.key);
```

Output

```text
undefined
```

Correct

```javascript
console.log(student[key]);
```

---

### ❌ Forgetting Quotes in Bracket Notation

Wrong

```javascript
student[name]
```

Correct

```javascript
student["name"]
```

or

```javascript
student[key]
```

if `key` is a variable.

---

# 📝 Quick Revision

- Objects store related data.
- Data is stored as key-value pairs.
- Use `.` or `[]` to access properties.
- Properties can be added, updated, or deleted.
- Use bracket notation when the property name is dynamic.

---

# 💻 Mini Exercise

Predict the output.

```javascript
const car = {
    brand: "Toyota",
    year: 2024
};

console.log(car.brand);

car.color = "White";

console.log(car.color);
```

---

# 📌 Key Takeaways

- Objects group related information.
- They store data as key-value pairs.
- Dot notation is simple and commonly used.
- Bracket notation is useful for dynamic property names.
- Objects are one of the most important concepts in JavaScript.

---

⬅️ Previous: `05-Functions/06-IIFE.md`

➡️ Next: `02-Object-Methods.md`