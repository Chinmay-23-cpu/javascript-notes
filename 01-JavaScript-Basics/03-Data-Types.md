# Data Types in JavaScript

## 📖 What is a Data Type?

A **data type** defines the kind of value a variable can store.

Think of a variable as a container.

Different containers hold different things.

```text
🥤 Bottle  → Water

📦 Box     → Books

💰 Wallet  → Money

📱 Phone   → Contacts
```

Similarly,

Variables can store:

- Numbers
- Text
- True/False values
- Objects
- Arrays
- Functions
- and more...

---

# 🤔 Why Do We Need Data Types?

Imagine calculating someone's age.

```javascript
let age = 20;
```

Age is a **number**, so JavaScript knows it can perform mathematical operations.

Now imagine storing a name.

```javascript
let name = "Chinmay";
```

A name is **text**, so JavaScript treats it differently.

Data types help JavaScript understand **how values should behave**.

---

# 📚 Types of Data in JavaScript

JavaScript has **8 data types**.

They are divided into two categories.

```text
JavaScript Data Types
│
├── Primitive (Immutable)
│   ├── Number
│   ├── String
│   ├── Boolean
│   ├── Undefined
│   ├── Null
│   ├── BigInt
│   └── Symbol
│
└── Non-Primitive (Reference)
    └── Object
         ├── Array
         ├── Function
         └── Object
```

---

# 🟢 Primitive Data Types

Primitive values are **simple values**.

They are stored directly.

There are **7 primitive data types**.

---

# 1️⃣ Number

Stores integers and decimal values.

```javascript
let age = 20;

let price = 99.99;
```

Examples

```javascript
10

-5

3.14

0
```

---

# 2️⃣ String

Stores text.

Strings can be written using:

```javascript
" "

' '

` `
```

Example

```javascript
let name = "Chinmay";

let city = 'Davangere';

let language = `JavaScript`;
```

---

# 3️⃣ Boolean

Boolean values have only two possibilities.

```javascript
true

false
```

Example

```javascript
let isLoggedIn = true;

let isAdmin = false;
```

---

# 4️⃣ Undefined

A variable declared but **not assigned a value** has the value `undefined`.

```javascript
let age;

console.log(age);
```

Output

```text
undefined
```

---

# 5️⃣ Null

`null` represents an **intentional absence of a value**.

```javascript
let user = null;
```

Think of it as saying:

> "I know there is no value here."

---

# Difference Between undefined and null

```javascript
let age;

console.log(age);
```

Output

```text
undefined
```

Meaning:

"I forgot to assign a value."

---

```javascript
let user = null;
```

Meaning:

"I intentionally kept it empty."

---

# 6️⃣ BigInt

Used for very large integers that exceed the safe range of the Number type.

```javascript
let big = 1234567890123456789012345678901234567890n;
```

Notice the **`n`** at the end.

---

# 7️⃣ Symbol

Creates a unique value.

```javascript
let id = Symbol("id");
```

Mostly used in advanced JavaScript to create unique property keys.

---

# 🔵 Non-Primitive Data Types

Everything that is **not a primitive** is an **object**.

Examples:

- Objects
- Arrays
- Functions

---

# Objects

Objects store related information as key-value pairs.

```javascript
let student = {
    name: "Chinmay",
    age: 20,
    college: "BIET"
};
```

---

# Arrays

Arrays store multiple values in order.

```javascript
let colors = ["Red", "Green", "Blue"];
```

Access elements using an index.

```javascript
console.log(colors[0]);
```

Output

```text
Red
```

---

# Functions

Functions are also objects in JavaScript.

```javascript
function greet() {
    console.log("Hello");
}
```

---

# 🔍 typeof Operator

The `typeof` operator tells us the data type of a value.

Examples

```javascript
typeof 20;
```

Output

```text
number
```

---

```javascript
typeof "Hello";
```

Output

```text
string
```

---

```javascript
typeof true;
```

Output

```text
boolean
```

---

```javascript
typeof undefined;
```

Output

```text
undefined
```

---

```javascript
typeof null;
```

Output

```text
object
```

⚠️ This is a well-known historical bug in JavaScript. Although `typeof null` returns `"object"`, `null` is a primitive value.

---

```javascript
typeof {};
```

Output

```text
object
```

---

```javascript
typeof [];
```

Output

```text
object
```

Arrays are a special type of object.

---

```javascript
typeof function(){};
```

Output

```text
function
```

---

# 🌍 Real-Life Analogy

Imagine your school bag.

```text
Primitive Values

📘 One Book

✏️ One Pencil

📱 One Phone

Simple, individual items.

-----------------------------

Object

🎒 School Bag

Contains many things together.
```

---

# ⚠️ Common Beginner Mistakes

## ❌ Confusing null and undefined

```javascript
let age;
```

Not assigned.

Result:

```text
undefined
```

---

```javascript
let age = null;
```

Intentionally empty.

---

## ❌ Thinking Arrays are not Objects

```javascript
typeof [];
```

Returns

```text
object
```

---

## ❌ Forgetting Quotes Around Strings

Wrong

```javascript
let name = Chinmay;
```

Correct

```javascript
let name = "Chinmay";
```

---

# 💼 Interview Questions

### What are the primitive data types?

- Number
- String
- Boolean
- Undefined
- Null
- BigInt
- Symbol

---

### What are non-primitive data types?

Objects, Arrays, and Functions (functions are objects in JavaScript).

---

### Difference between null and undefined?

- `undefined` means a value has not been assigned.
- `null` means the value is intentionally empty.

---

### What does `typeof` do?

It returns the type of a value.

Example

```javascript
typeof "Hello"; // "string"
```

---

### Why does `typeof null` return `"object"`?

Because of a historical bug in JavaScript that has been kept for compatibility.

---

# 📝 Revision Sheet

- JavaScript has **8 data types**.
- **7 are primitive**, **1 is non-primitive (Object)**.
- Arrays and Functions are objects.
- `typeof` is used to check data types.
- `null` and `undefined` are different.
- `typeof null` returns `"object"` because of a historical bug.

---

# 🧪 Practice Questions

1. What is a data type?
2. List all primitive data types.
3. What is the difference between primitive and non-primitive values?
4. Explain `null` and `undefined`.
5. What does `typeof` do?
6. Why does `typeof null` return `"object"`?
7. Are arrays objects?
8. Are functions objects?

---

# 💻 Mini Exercise

Predict the output before running the code.

```javascript
let age = 20;
let name = "Chinmay";
let isStudent = true;
let city;
let marks = null;
let colors = ["Red", "Blue"];

console.log(typeof age);
console.log(typeof name);
console.log(typeof isStudent);
console.log(typeof city);
console.log(typeof marks);
console.log(typeof colors);
```

### Expected Output

```text
number
string
boolean
undefined
object
object
```

---

# 📌 Key Takeaways

- Every value in JavaScript has a data type.
- JavaScript has **8 data types**.
- Primitive values are simple and immutable.
- Objects can store collections of data.
- Arrays and functions are objects.
- Use `typeof` to identify most data types.
- Remember the special case: `typeof null` returns `"object"` due to a historical bug.