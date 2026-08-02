# Temporal Dead Zone (TDZ)

> 📚 Chapter 3 of JavaScript Internals

---

# 📑 Table of Contents

- What is the Temporal Dead Zone?
- Why Do We Need TDZ?
- How TDZ Works
- TDZ with let
- TDZ with const
- TDZ vs var
- Visual Diagram
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is the Temporal Dead Zone?

The **Temporal Dead Zone (TDZ)** is the period between:

- when a `let` or `const` variable is created in memory, and
- when it is initialized during execution.

During this time, the variable **exists**, but it **cannot be accessed**.

Trying to access it results in a **ReferenceError**.

---

# 🤔 Why Do We Need TDZ?

Imagine writing:

```javascript
console.log(age);

let age = 20;
```

If JavaScript allowed this, it could lead to bugs because `age` hasn't been assigned a value yet.

The TDZ prevents you from using variables before they are initialized.

---

# 🌍 Real-Life Analogy

Imagine a classroom.

The teacher writes your name on the attendance sheet before class starts.

```text
Attendance Sheet

✔ Chinmay

✔ Rahul

✔ Priya
```

Your name exists on the list.

But until you enter the classroom and answer **"Present!"**, the teacher cannot mark you as present.

Similarly,

- `let` and `const` variables exist in memory.
- They cannot be used until JavaScript reaches their declaration.

---

# ⚙️ How TDZ Works

Consider this code.

```javascript
console.log(age);

let age = 20;
```

---

## Step 1 — Memory Creation Phase

JavaScript creates memory.

```text
Memory

age → <uninitialized>
```

Notice:

The variable exists.

But it has **no value**.

---

## Step 2 — Execution Phase

First line

```javascript
console.log(age);
```

JavaScript checks the memory.

It finds:

```text
age → <uninitialized>
```

Result

```text
ReferenceError
```

Execution stops.

---

# 📦 TDZ with let

```javascript
console.log(name);

let name = "Chinmay";
```

Output

```text
ReferenceError
```

---

After initialization

```javascript
let name = "Chinmay";

console.log(name);
```

Output

```text
Chinmay
```

---

# 📦 TDZ with const

```javascript
console.log(PI);

const PI = 3.14;
```

Output

```text
ReferenceError
```

After initialization

```javascript
const PI = 3.14;

console.log(PI);
```

Output

```text
3.14
```

---

# 📦 TDZ with var

```javascript
console.log(city);

var city = "Delhi";
```

Output

```text
undefined
```

Why?

Because `var` is initialized with `undefined` during the Memory Creation Phase.

It does **not** have a Temporal Dead Zone.

---

# 📊 Visual Diagram

```javascript
console.log(score);

let score = 100;
```

Memory Creation

```text
score → <uninitialized>
```

↓

Execution starts

```text
console.log(score)
```

↓

```text
ReferenceError
```

↓

Program Stops

---

Now consider:

```javascript
let score = 100;

console.log(score);
```

Execution

```text
score = 100

↓

console.log(score)

↓

100
```

---

# 🆚 TDZ vs var

| Feature | var | let | const |
|---------|-----|-----|-------|
| Hoisted | ✅ Yes | ✅ Yes | ✅ Yes |
| Initial Value | `undefined` | Uninitialized | Uninitialized |
| Temporal Dead Zone | ❌ No | ✅ Yes | ✅ Yes |
| Access Before Declaration | `undefined` | ReferenceError | ReferenceError |

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking let is not hoisted

Wrong.

`let` **is hoisted**.

It simply stays in the TDZ until initialized.

---

## ❌ Thinking const is not hoisted

Wrong.

`const` is also hoisted.

It remains uninitialized until execution reaches its declaration.

---

## ❌ Confusing undefined with TDZ

```javascript
var x;
```

Output

```text
undefined
```

---

```javascript
let x;
```

After the declaration executes:

```javascript
console.log(x);
```

Output

```text
undefined
```

But **before** the declaration:

```javascript
console.log(x);

let x;
```

Output

```text
ReferenceError
```

The difference is **when** you're accessing the variable.

---

# 💼 Interview Questions

### What is the Temporal Dead Zone?

The period between memory creation and initialization where `let` and `const` variables cannot be accessed.

---

### Which variables have a TDZ?

- `let`
- `const`

---

### Does `var` have a TDZ?

No.

`var` is initialized with `undefined`.

---

### Why was TDZ introduced?

To prevent programmers from accidentally using variables before they are initialized.

---

# 📝 Revision Sheet

- TDZ applies to `let` and `const`.
- Variables exist in memory but are uninitialized.
- Accessing them during the TDZ throws a `ReferenceError`.
- `var` does not have a TDZ.
- TDZ helps prevent bugs.

---

# 🧪 Practice Questions

1. What is the Temporal Dead Zone?
2. Why does TDZ exist?
3. Which variables have a TDZ?
4. Does `var` have a TDZ?
5. What happens if you access a `let` variable before initialization?
6. Difference between TDZ and `undefined`.

---

# 💻 Mini Exercise

Predict the output.

```javascript
console.log(a);

var a = 10;
```

Output

```text
undefined
```

---

Predict the output.

```javascript
console.log(b);

let b = 20;
```

Output

```text
ReferenceError
```

---

Predict the output.

```javascript
const PI = 3.14;

console.log(PI);
```

Output

```text
3.14
```

---

# 📌 Key Takeaways

- TDZ is the period before a `let` or `const` variable is initialized.
- `let` and `const` are hoisted but remain uninitialized.
- Accessing them during the TDZ throws a `ReferenceError`.
- `var` is hoisted and initialized with `undefined`, so it has no TDZ.
- TDZ helps catch mistakes early and makes JavaScript code safer.

---

⬅️ Previous: `02-Hoisting.md`

➡️ Next: `04-Scope.md`