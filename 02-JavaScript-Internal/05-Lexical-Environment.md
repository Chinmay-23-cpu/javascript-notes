# Lexical Environment

> 📚 Chapter 5 of JavaScript Internals

---

# 📑 Table of Contents

- What is a Lexical Environment?
- Why Do We Need It?
- Lexical Means...
- Components of a Lexical Environment
- Scope vs Lexical Environment
- Lexical Environment in Nested Functions
- Scope Chain
- Visual Diagram
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is a Lexical Environment?

A **Lexical Environment** is the environment where JavaScript stores:

- Variables
- Functions
- A reference to its outer (parent) environment

Simply put,

> Every function remembers **where it was created**.

That memory is called its **Lexical Environment**.

---

# 🤔 Why Do We Need It?

Imagine this code.

```javascript
let country = "India";

function greet() {
    console.log(country);
}

greet();
```

How does `greet()` know what `country` is?

The answer is:

Because it remembers the environment in which it was created.

---

# 📚 What Does "Lexical" Mean?

The word **Lexical** means:

> Based on where something is **written in the source code**.

Not where it is called.

Example

```javascript
function outer() {

    let name = "Chinmay";

    function inner() {

        console.log(name);

    }

}
```

`inner()` is written inside `outer()`.

So it automatically remembers everything inside `outer()`.

---

# 🧠 Components of a Lexical Environment

Every Lexical Environment contains two things.

```text
Lexical Environment

│

├── Environment Record
│      (Variables & Functions)

│

└── Reference to Outer Environment
```

---

## Environment Record

Stores:

- Variables
- Functions

Example

```javascript
let age = 20;

function greet() {}
```

Environment Record

```text
age → 20

greet → function
```

---

## Outer Environment Reference

Every function remembers its parent.

Example

```javascript
function outer() {

    function inner() {

    }

}
```

Memory

```text
inner

↓

Reference

↓

outer

↓

Reference

↓

Global
```

---

# 🌍 Real-Life Analogy

Imagine a family tree.

```text
Grandfather

↓

Father

↓

Son
```

The son knows who his father is.

The father knows who his grandfather is.

Similarly,

Each function knows its parent environment.

---

# ⚙️ Lexical Environment in Nested Functions

Example

```javascript
let country = "India";

function outer() {

    let state = "Karnataka";

    function inner() {

        let city = "Davangere";

        console.log(city);

        console.log(state);

        console.log(country);

    }

    inner();

}

outer();
```

Output

```text
Davangere

Karnataka

India
```

How?

JavaScript searches step by step.

```text
Current Environment

↓

Outer Environment

↓

Global Environment
```

This search follows the **Lexical Environment**.

---

# 🆚 Scope vs Lexical Environment

Many beginners confuse these two.

| Scope | Lexical Environment |
|--------|---------------------|
| Decides where variables can be accessed | Stores variables and reference to parent environment |
| A programming concept | Internal JavaScript mechanism |
| Used by developers | Used by the JavaScript engine |

Think of it like this:

- **Scope** = The rule.
- **Lexical Environment** = The implementation of that rule.

---

# 🔗 Scope Chain

Example

```javascript
let a = 1;

function one() {

    let b = 2;

    function two() {

        let c = 3;

        console.log(a);
        console.log(b);
        console.log(c);

    }

    two();

}

one();
```

Search order

```text
Current Environment

↓

Outer Environment

↓

Global Environment

↓

ReferenceError
```

This is called the **Scope Chain**.

---

# 📊 Visual Diagram

```text
Global Environment

a = 1

│

└──── one()

       b = 2

       │

       └──── two()

              c = 3
```

`two()` can access

✅ c

✅ b

✅ a

---

`one()` can access

✅ b

✅ a

❌ c

---

Global can access

✅ a

❌ b

❌ c

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking functions remember where they are called

Wrong.

Functions remember **where they are created**, not where they are called.

---

## ❌ Confusing Scope and Lexical Environment

Scope is the rule.

Lexical Environment is how JavaScript stores and finds variables.

---

## ❌ Thinking JavaScript searches randomly

Wrong.

JavaScript always searches in this order:

```text
Current

↓

Parent

↓

Grandparent

↓

Global
```

---

# 💼 Interview Questions

### What is a Lexical Environment?

A structure that stores variables, functions, and a reference to its outer environment.

---

### What does lexical mean?

It means "based on where something is written in the source code."

---

### Why does an inner function access outer variables?

Because it remembers its parent Lexical Environment.

---

### Difference between Scope and Lexical Environment?

Scope defines where variables are accessible.

Lexical Environment is the internal mechanism JavaScript uses to implement scope.

---

### What is the Scope Chain?

The process of searching outer lexical environments when a variable is not found in the current one.

---

# 📝 Revision Sheet

- Every function gets its own Lexical Environment.
- A Lexical Environment stores variables and functions.
- It also stores a reference to its parent environment.
- Functions remember where they are created.
- JavaScript searches variables using the Scope Chain.

---

# 🧪 Practice Questions

1. What is a Lexical Environment?
2. What does "lexical" mean?
3. What are the two components of a Lexical Environment?
4. Difference between Scope and Lexical Environment.
5. Why can an inner function access outer variables?
6. What is the Scope Chain?

---

# 💻 Mini Exercise

Predict the output.

```javascript
let language = "JavaScript";

function outer() {

    let version = "ES6";

    function inner() {

        console.log(language);

        console.log(version);

    }

    inner();

}

outer();
```

### Expected Output

```text
JavaScript

ES6
```

Explain **how JavaScript finds both variables** using the Lexical Environment.

---

# 📌 Key Takeaways

- Every function has a Lexical Environment.
- It stores variables, functions, and a reference to its parent environment.
- Functions remember where they are created.
- JavaScript searches variables from the current environment outward.
- The Lexical Environment is the foundation of the Scope Chain and Closures.

---

⬅️ Previous: `04-Scope.md`

➡️ Next: `06-Strict-Mode.md`