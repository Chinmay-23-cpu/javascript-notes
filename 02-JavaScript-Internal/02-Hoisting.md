# Hoisting in JavaScript

> 📚 Chapter 2 of JavaScript Internals

---

# 📑 Table of Contents

- What is Hoisting?
- Why Do We Need Hoisting?
- Is Code Actually Moved?
- How Hoisting Works
- Hoisting with var
- Hoisting with let
- Hoisting with const
- Function Hoisting
- Function Expression Hoisting
- Arrow Function Hoisting
- Visual Memory Diagram
- Common Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Hoisting?

**Hoisting** is JavaScript's behavior of **setting up declarations during the Memory Creation Phase before any code is executed.**

> **Important:** Hoisting **does not move your code** to the top of the file.

It only prepares memory before execution begins.

---

# 🤔 Why Do We Need Hoisting?

Remember what we learned in **Execution Context**?

Every JavaScript program runs in two phases.

```text
Execution Context

│

├── Memory Creation Phase

└── Execution Phase
```

During the Memory Creation Phase,

JavaScript scans the entire program and prepares memory for:

- Variables
- Functions

This preparation is called **Hoisting**.

---

# ❌ Common Myth

Many beginners think JavaScript secretly changes this:

```javascript
console.log(a);

var a = 10;
```

into

```javascript
var a;

console.log(a);

a = 10;
```

**This is NOT what happens.**

Your code stays exactly where you wrote it.

JavaScript simply creates memory for declarations before execution starts.

---

# 🧠 How Hoisting Works

Consider this program.

```javascript
console.log(age);

var age = 20;
```

---

## Step 1 — Memory Creation Phase

JavaScript scans the file.

Memory becomes:

```text
age → undefined
```

Notice that the variable already exists.

---

## Step 2 — Execution Phase

First line

```javascript
console.log(age);
```

Current value:

```text
undefined
```

Output

```text
undefined
```

---

Next line

```javascript
age = 20;
```

Memory becomes

```text
age → 20
```

Program ends.

---

# 📦 Hoisting with var

Example

```javascript
console.log(city);

var city = "Delhi";
```

Memory Creation

```text
city → undefined
```

Execution

```text
console.log(city)

↓

undefined

↓

city = "Delhi"
```

Output

```text
undefined
```

No error.

---

# 📦 Hoisting with let

Example

```javascript
console.log(age);

let age = 20;
```

Output

```text
ReferenceError
```

Why?

The variable is created during the Memory Creation Phase,

but it **cannot be accessed before initialization**.

This area is called the **Temporal Dead Zone (TDZ)**.

We'll study TDZ in the next chapter.

---

# 📦 Hoisting with const

```javascript
console.log(PI);

const PI = 3.14;
```

Output

```text
ReferenceError
```

Exactly like `let`.

---

# 📦 Function Hoisting

Function declarations are fully hoisted.

Example

```javascript
greet();

function greet() {
    console.log("Hello");
}
```

Output

```text
Hello
```

Why?

Memory Creation

```text
greet → complete function
```

The entire function is already available before execution starts.

---

# 📦 Function Expression

```javascript
greet();

var greet = function () {
    console.log("Hello");
};
```

Memory

```text
greet → undefined
```

Execution

First line

```javascript
greet();
```

Current value

```text
undefined
```

Output

```text
TypeError:
greet is not a function
```

Because JavaScript tries to call `undefined()`.

---

# 📦 Arrow Function

```javascript
hello();

const hello = () => {
    console.log("Hi");
};
```

Output

```text
ReferenceError
```

Because `const` variables stay in the Temporal Dead Zone until initialized.

---

# 📊 Visual Memory Diagram

Example

```javascript
console.log(a);

function greet() {
    console.log("Hello");
}

var a = 10;
```

---

## Memory Creation Phase

```text
Memory

a → undefined

greet → function
```

---

## Execution Phase

```text
console.log(a)

↓

undefined

↓

a = 10

↓

greet() is ready to be called
```

---

# 📚 Summary Table

| Declaration | Hoisted? | Initial Value | Access Before Declaration |
|-------------|----------|---------------|---------------------------|
| `var` | ✅ Yes | `undefined` | ✅ Yes (returns `undefined`) |
| `let` | ✅ Yes | Uninitialized | ❌ ReferenceError |
| `const` | ✅ Yes | Uninitialized | ❌ ReferenceError |
| Function Declaration | ✅ Yes | Entire function | ✅ Yes |
| Function Expression | Depends on variable | Usually `undefined` with `var` | ❌ TypeError if called before assignment |
| Arrow Function | Depends on variable | Uninitialized with `let`/`const` | ❌ ReferenceError |

---

# 🌍 Real-Life Analogy

Imagine a classroom.

Before class starts,

the teacher prepares attendance.

```text
Roll No 1

Roll No 2

Roll No 3
```

Students are registered,

but they haven't answered "Present" yet.

That's exactly how hoisting works.

Memory is prepared first.

Values come later.

---

# ⚠️ Common Beginner Mistakes

## ❌ Hoisting moves code

Wrong.

JavaScript **never changes the order of your code**.

---

## ❌ let is not hoisted

Wrong.

`let` **is hoisted**.

It just cannot be accessed before initialization.

---

## ❌ const is not hoisted

Wrong.

`const` is also hoisted.

It remains uninitialized until its declaration executes.

---

## ❌ Function expressions behave like function declarations

Wrong.

Function declarations are fully hoisted.

Function expressions are not.

---

# 💼 Interview Questions

### What is hoisting?

Hoisting is JavaScript's behavior of preparing declarations during the Memory Creation Phase before executing code.

---

### Does JavaScript move code?

No.

Only declarations are prepared in memory.

The source code remains unchanged.

---

### Why does `var` print `undefined`?

Because `var` is initialized with `undefined` during the Memory Creation Phase.

---

### Why does `let` throw a ReferenceError?

Because it stays in the Temporal Dead Zone until initialized.

---

### Are functions hoisted?

Function declarations are fully hoisted.

Function expressions are not.

---

# 📝 Revision Sheet

- Hoisting happens during the Memory Creation Phase.
- JavaScript **does not move your code**.
- `var` → initialized as `undefined`.
- `let` and `const` → hoisted but uninitialized.
- Function declarations are fully hoisted.
- Function expressions depend on the variable they are assigned to.

---

# 🧪 Practice Questions

1. What is hoisting?
2. Does JavaScript move code during hoisting?
3. Why does `var` print `undefined`?
4. Why does `let` throw a ReferenceError?
5. Are functions hoisted?
6. Difference between function declaration and function expression hoisting.
7. Explain hoisting using the Memory Creation Phase.

---

# 💻 Mini Exercise

Predict the output before running the code.

```javascript
console.log(a);

var a = 10;

console.log(b);

let b = 20;

hello();

function hello() {
    console.log("Hello");
}
```

### Expected Output

```text
undefined

ReferenceError
```

> **Why doesn't `"Hello"` print?**

Because execution stops as soon as the `ReferenceError` occurs, so `hello()` is never reached.

---

# 📌 Key Takeaways

- Hoisting happens during the Memory Creation Phase.
- JavaScript does **not** move code.
- `var` is hoisted and initialized to `undefined`.
- `let` and `const` are hoisted but stay uninitialized until execution reaches their declaration.
- Function declarations are fully hoisted.
- Function expressions and arrow functions behave according to the variable (`var`, `let`, or `const`) used to store them.

---

⬅️ Previous: `01-Execution-Context.md`

➡️ Next: `03-Temporal-Dead-Zone.md`