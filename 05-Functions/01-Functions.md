# Functions in JavaScript

> 📚 Chapter 1 of Functions

---

## 📖 Imagine This...

Suppose you need to greet every user who visits your website.

Without functions, you might write:

```javascript
console.log("Welcome!");
console.log("Welcome!");
console.log("Welcome!");
```

Again and again.

Instead, we can write the code once and reuse it whenever we need it.

That's exactly what a **function** is.

---

# 🤔 What is a Function?

A **function** is a reusable block of code that performs a specific task.

Instead of writing the same code multiple times, write it once inside a function and call it whenever you need it.

---

# 🧠 Function Declaration

The most common way to create a function.

```javascript
function greet() {
    console.log("Welcome!");
}
```

Nothing happens yet.

The function only runs when you call it.

```javascript
greet();
```

### Output

```text
Welcome!
```

---

# 💻 Calling a Function Multiple Times

```javascript
function greet() {
    console.log("Welcome!");
}

greet();
greet();
greet();
```

### Output

```text
Welcome!
Welcome!
Welcome!
```

One function.

Multiple uses.

---

# 🧠 Function Expression

A function can also be stored inside a variable.

```javascript
const greet = function () {
    console.log("Welcome!");
};

greet();
```

### Output

```text
Welcome!
```

Notice the difference.

Function Declaration

```javascript
function greet() {}
```

Function Expression

```javascript
const greet = function () {};
```

---

# 🚀 Arrow Function

Arrow functions are a shorter way of writing functions.

Instead of

```javascript
function greet() {
    console.log("Welcome!");
}
```

we can write

```javascript
const greet = () => {
    console.log("Welcome!");
};
```

### Output

```text
Welcome!
```

It does the same job.

The syntax is simply shorter.

---

# 📊 Three Ways to Create a Function

```javascript
// Function Declaration

function greet() {
    console.log("Hello");
}
```

---

```javascript
// Function Expression

const greet = function () {
    console.log("Hello");
};
```

---

```javascript
// Arrow Function

const greet = () => {
    console.log("Hello");
};
```

---

# 🌍 When Should I Use Which?

### Function Declaration

Use when creating normal functions.

```javascript
function calculateTotal() {}
```

---

### Function Expression

Useful when passing functions around or assigning them to variables.

---

### Arrow Function

Mostly used in modern JavaScript and React because it's shorter and cleaner.

---

# ⚠️ Common Beginner Mistakes

## ❌ Forgetting to Call the Function

```javascript
function greet() {
    console.log("Hello");
}
```

This only creates the function.

To run it,

```javascript
greet();
```

---

## ❌ Mixing Function Declaration and Expression

Wrong

```javascript
function = greet() {}
```

Correct

```javascript
function greet() {}
```

or

```javascript
const greet = function () {};
```

---

## ❌ Forgetting the Semicolon

Function declarations don't need one.

```javascript
function greet() {}
```

Function expressions and arrow functions do.

```javascript
const greet = function () {};

const hello = () => {};
```

---

# 💼 Interview Questions

### What is a function?

A reusable block of code that performs a specific task.

---

### Difference between Function Declaration and Function Expression?

A declaration defines the function directly.

An expression stores the function inside a variable.

---

### What is an Arrow Function?

A shorter syntax for writing functions introduced in ES6.

---

# 📝 Quick Revision

✅ Functions help avoid repeating code.

✅ A function runs only when it's called.

✅ There are three common ways to create functions:

- Function Declaration
- Function Expression
- Arrow Function

✅ Arrow functions are shorter and commonly used in modern JavaScript.

---

# 💻 Mini Exercise

Predict the output.

```javascript
function greet() {
    console.log("Hello");
}

greet();
```

---

Convert this function into an arrow function.

```javascript
function sayBye() {
    console.log("Bye");
}
```

---

# 📌 Key Takeaways

- Functions are reusable blocks of code.
- They improve readability and reduce repetition.
- Function declarations are the most common.
- Function expressions store functions in variables.
- Arrow functions provide a shorter syntax and are widely used in modern JavaScript.

---

⬅️ Previous: `04-Control-Flow/06-Loop-Control-and-Logical-Operators.md`

➡️ Next: `02-Parameters-and-Arguments.md`