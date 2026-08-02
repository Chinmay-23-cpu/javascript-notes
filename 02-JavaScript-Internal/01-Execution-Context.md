# Execution Context

> 📚 Chapter 1 of JavaScript Internals

---

# 📑 Table of Contents

- What is Execution Context?
- Why Do We Need It?
- Real-Life Analogy
- How JavaScript Executes Code
- Types of Execution Context
- Global Execution Context
- Function Execution Context
- Execution Context Phases
- Memory Creation Phase
- Execution Phase
- Call Stack
- Complete Example
- Common Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Execution Context?

An **Execution Context** is the environment in which JavaScript executes your code.

It contains everything JavaScript needs while running your program:

- Variables
- Functions
- The value of `this`
- The current scope

Think of it as JavaScript's **workspace**.

Whenever JavaScript runs code, it first creates an execution context.

---

# 🤔 Why Do We Need It?

Imagine you're solving a math problem.

Before solving it, you need:

- A notebook
- A pen
- The question

Only then can you start solving.

Execution Context is JavaScript's notebook.

Without it, JavaScript has nowhere to store variables or functions.

---

# 🌍 Real-Life Analogy

Imagine a chef working in a kitchen.

Before cooking, the chef prepares the workspace.

```text
Kitchen
│
├── Vegetables
├── Knife
├── Stove
├── Plates
└── Recipe
```

After everything is ready...

Cooking begins.

JavaScript does exactly the same thing.

First it prepares the workspace.

Then it executes the code.

---

# ⚙️ How JavaScript Executes Code

Whenever a JavaScript file runs...

```text
JavaScript File
        │
        ▼
Creates Execution Context
        │
        ▼
Memory Creation Phase
        │
        ▼
Execution Phase
        │
        ▼
Program Finishes
```

Every JavaScript program follows this flow.

---

# 📚 Types of Execution Context

JavaScript mainly creates two kinds of execution contexts.

```text
Execution Context
│
├── Global Execution Context (GEC)
│
└── Function Execution Context (FEC)
```

---

# 🌍 Global Execution Context (GEC)

The **Global Execution Context** is created **only once** when your JavaScript program starts.

Example

```javascript
let name = "Chinmay";

function greet() {
    console.log("Hello");
}
```

Before running any line...

JavaScript creates the Global Execution Context.

Everything declared outside functions belongs here.

---

# ⚙️ Function Execution Context (FEC)

Whenever a function is called...

JavaScript creates a **new execution context** for that function.

Example

```javascript
function greet() {
    let message = "Hello";
    console.log(message);
}

greet();
```

Flow

```text
Program Starts
        │
        ▼
Global Execution Context
        │
        ▼
Function Called
        │
        ▼
Function Execution Context
        │
        ▼
Function Ends
        │
        ▼
Function Context Removed
```

Every function call gets its own execution context.

---

# 🧠 Two Phases of an Execution Context

Every execution context has **two phases**.

```text
Execution Context
│
├── Memory Creation Phase
│
└── Execution Phase
```

---

# 🏗️ Phase 1 — Memory Creation Phase

Before running any code...

JavaScript scans the entire file.

It prepares memory.

During this phase:

✅ Variables are created.

✅ Function declarations are stored.

No code actually runs yet.

Think of it as preparation.

---

Example

```javascript
let age = 20;

function greet() {}
```

Memory looks like:

```text
Memory

age → <uninitialized>

greet → function
```

Notice:

`age` doesn't yet have the value `20`.

That happens later.

---

# ▶️ Phase 2 — Execution Phase

Now JavaScript executes the code line by line.

Example

```javascript
let age = 20;
```

Now memory becomes

```text
age → 20
```

Functions are executed only when called.

---

# 📚 Complete Example

```javascript
let x = 10;

function greet() {
    console.log("Hello");
}

console.log(x);

greet();
```

### Step 1 — Global Execution Context Created

```text
Global Execution Context
```

---

### Step 2 — Memory Creation Phase

```text
Memory

x → <uninitialized>

greet → function
```

---

### Step 3 — Execution Phase

```javascript
let x = 10;
```

Memory

```text
x → 10
```

---

```javascript
console.log(x);
```

Output

```text
10
```

---

```javascript
greet();
```

Now JavaScript creates another execution context.

```text
Global Context

↓

Function Context

↓

console.log("Hello")

↓

Function Ends

↓

Back to Global Context
```

Output

```text
Hello
```

---

# 📚 Call Stack

JavaScript keeps track of execution contexts using a **Call Stack**.

Think of it as a stack of books.

The last book placed on top is the first one removed.

This follows the **LIFO (Last In, First Out)** principle.

---

Example

```javascript
function one() {
    two();
}

function two() {
    console.log("Hello");
}

one();
```

Call Stack

```text
Start

↓

Global

↓

one()

↓

two()

↓

console.log()

↓

console.log() finishes

↓

two() removed

↓

one() removed

↓

Global removed

↓

Program Ends
```

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking JavaScript executes code immediately

No.

It first creates the execution context.

Then it executes the code.

---

## ❌ Thinking functions run when declared

```javascript
function greet() {}
```

Nothing happens.

Functions only execute when called.

```javascript
greet();
```

---

## ❌ Thinking variables already contain values during memory creation

They don't.

Memory is only allocated.

The actual values are assigned during the execution phase.

---

# 💼 Interview Questions

### What is an Execution Context?

The environment where JavaScript executes code.

---

### How many phases does an Execution Context have?

Two.

- Memory Creation Phase
- Execution Phase

---

### What is the Global Execution Context?

The execution context created when the JavaScript program starts.

There is only one Global Execution Context per program.

---

### What is the Function Execution Context?

A new execution context created every time a function is called.

---

### What is the Call Stack?

A data structure that keeps track of execution contexts.

It follows the **Last In, First Out (LIFO)** principle.

---

# 📝 Revision Sheet

- JavaScript always creates an Execution Context before running code.
- Every execution context has:
  - Memory Creation Phase
  - Execution Phase
- Global Execution Context is created once.
- Every function call creates a new Function Execution Context.
- The Call Stack manages all execution contexts.

---

# 🧪 Practice Questions

1. What is an Execution Context?
2. Why is an Execution Context needed?
3. Name the two phases of an Execution Context.
4. What is the difference between the Global and Function Execution Context?
5. What is the Call Stack?
6. Which data structure does the Call Stack use?
7. When is a Function Execution Context created?

---

# 💻 Mini Exercise

Predict the output before running the code.

```javascript
let name = "Chinmay";

function greet() {
    console.log("Hello");
}

console.log(name);

greet();
```

### Expected Output

```text
Chinmay
Hello
```

Now explain **which execution context is active** at each step.

---

# 📌 Key Takeaways

- Execution Context is JavaScript's workspace.
- JavaScript creates an execution context before running code.
- Every execution context has two phases:
  - Memory Creation
  - Execution
- There is one Global Execution Context.
- Every function call creates a new Function Execution Context.
- The Call Stack keeps track of which execution context is currently running.

---

⬅️ Previous: `01-JavaScript-Basics/04-Operators.md`

➡️ Next: `02-Hoisting.md`