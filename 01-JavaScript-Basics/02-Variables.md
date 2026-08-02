# Variables in JavaScript

## 📖 What is a Variable?

A **variable** is a named container used to store data.

Think of it as a **box** with a label.

```text
        +------------------+
Name -->|     Chinmay      |
        +------------------+

Age ---->|       20         |
        +------------------+
```

The label is the **variable name**, and the value inside the box is the **data**.

---

# 🤔 Why Do We Need Variables?

Imagine writing this:

```javascript
console.log("Chinmay");
console.log("Chinmay");
console.log("Chinmay");
```

If your name changes, you have to update it everywhere.

Instead,

```javascript
let name = "Chinmay";

console.log(name);
console.log(name);
console.log(name);
```

Now you only change it once.

---

# 🏗️ Declaring Variables

JavaScript provides three ways to declare variables.

```javascript
var
let
const
```

Example

```javascript
var city = "Davangere";

let age = 20;

const PI = 3.14159;
```

---

# 📌 let

`let` is the modern way to declare variables.

Its value **can be changed**.

```javascript
let score = 10;

score = 25;

console.log(score);
```

Output

```text
25
```

---

# 📌 const

`const` is used for values that should never change.

```javascript
const country = "India";

console.log(country);
```

Trying to change it:

```javascript
const country = "India";

country = "USA";
```

Output

```text
TypeError
```

---

# 📌 var

`var` is the old way of declaring variables.

It still works but is generally avoided in modern JavaScript because of its different scoping behavior.

```javascript
var language = "JavaScript";

console.log(language);
```

---

# 🆚 Difference Between let, const and var

| Feature | var | let | const |
|----------|-----|-----|-------|
| Can be reassigned | ✅ Yes | ✅ Yes | ❌ No |
| Can be redeclared in same scope | ✅ Yes | ❌ No | ❌ No |
| Block scoped | ❌ No | ✅ Yes | ✅ Yes |

---

# ✍️ Variable Naming Rules

A variable name:

✅ Can contain letters

```javascript
let student;
```

---

✅ Can contain numbers (not at the beginning)

```javascript
let age1;
```

---

❌ Cannot start with a number

```javascript
let 1age = 20;
```

---

✅ Can contain `_`

```javascript
let student_name;
```

---

✅ Can contain `$`

```javascript
let $price = 100;
```

---

❌ Cannot contain spaces

Wrong

```javascript
let student age;
```

Correct

```javascript
let studentAge;
```

---

❌ Cannot use keywords

Wrong

```javascript
let if = 20;
```

---

# 🐪 Camel Case

JavaScript developers commonly use **camelCase** for variable names.

```javascript
let studentAge;

let totalMarks;

let currentBalance;
```

Avoid

```javascript
let Student_Age;

let student_age;

let STUDENTAGE;
```

---

# 💻 Examples

### Example 1

```javascript
let name = "Chinmay";

console.log(name);
```

---

### Example 2

```javascript
let age = 20;

age = 21;

console.log(age);
```

Output

```text
21
```

---

### Example 3

```javascript
const PI = 3.14;

console.log(PI);
```

---

### Example 4

```javascript
let firstName = "Chinmay";
let lastName = "Bhat";

console.log(firstName + " " + lastName);
```

Output

```text
Chinmay Bhat
```

---

# 🌍 Real-Life Analogy

Imagine three types of bottles.

```text
let
Reusable Bottle
You can refill it.

const
Sealed Bottle
Cannot be changed.

var
Old Bottle
Still works but people now prefer better bottles.
```

---

# ⚠️ Common Beginner Mistakes

## ❌ Using const when the value changes

```javascript
const marks = 90;

marks = 95;
```

Error.

Use `let` instead.

---

## ❌ Forgetting to initialize const

```javascript
const age;
```

Wrong.

```javascript
const age = 20;
```

Correct.

---

## ❌ Poor variable names

Bad

```javascript
let a;

let x;

let data;
```

Better

```javascript
let studentName;

let totalMarks;

let currentTemperature;
```

---

# 💼 Interview Questions

### What is a variable?

A variable is a named container used to store data.

---

### Difference between let and const?

- `let` can be reassigned.
- `const` cannot be reassigned after initialization.

---

### Should we use var?

In modern JavaScript, prefer `let` and `const`. `var` is mostly used when working with older codebases.

---

### Why use meaningful variable names?

They improve code readability and make programs easier to maintain.

---

# 📝 Revision Sheet

- Variables store data.
- Use `let` when the value may change.
- Use `const` when the value should stay the same.
- Avoid `var` in new projects.
- Follow camelCase naming convention.

---

# 🧪 Practice Questions

1. What is a variable?
2. Difference between `let`, `const`, and `var`.
3. Can a `const` variable be reassigned?
4. What is camelCase?
5. Is `let age1` valid?
6. Is `let 1age` valid?
7. Why should variable names be meaningful?

---

# 💻 Mini Exercise

Create the following variables:

```text
Name
Age
College
CGPA
```

Print all of them.

Expected Output

```text
Name : Chinmay
Age : 20
College : BIET
CGPA : 9.1
```

Example Solution

```javascript
let name = "Chinmay";
let age = 20;
let college = "BIET";
let cgpa = 9.1;

console.log("Name :", name);
console.log("Age :", age);
console.log("College :", college);
console.log("CGPA :", cgpa);
```

---

# 📌 Key Takeaways

- Variables are containers for storing data.
- Use `let` for changing values.
- Use `const` for fixed values.
- Avoid `var` in modern JavaScript.
- Use meaningful names and follow camelCase.