# Scope in JavaScript

> 📚 Chapter 4 of JavaScript Internals

---

# 📑 Table of Contents

- What is Scope?
- Why Do We Need Scope?
- Types of Scope
- Global Scope
- Function Scope
- Block Scope
- Nested Scope
- Scope Chain
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Scope?

**Scope** determines **where a variable can be accessed** in your program.

In simple words,

> Scope decides **who can use a variable**.

Think of it as defining the **visibility** of variables.

---

# 🤔 Why Do We Need Scope?

Imagine every variable in your program could be accessed from anywhere.

```javascript
let marks = 90;
```

Now imagine another part of your program accidentally changes it.

```javascript
marks = 20;
```

Your program becomes difficult to manage.

Scope helps keep variables safe by limiting where they can be accessed.

---

# 🌍 Real-Life Analogy

Imagine a school.

```text
School
│
├── Principal's Office
├── Classroom A
├── Classroom B
└── Library
```

A student inside **Classroom A** cannot simply use the teacher's files stored in the **Principal's Office**.

Similarly,

Variables belong to certain areas of your program.

Only code inside that area (or allowed areas) can access them.

---

# 📚 Types of Scope

JavaScript mainly has three types of scope.

```text
Scope
│
├── Global Scope
├── Function Scope
└── Block Scope
```

---

# 🌍 Global Scope

Variables declared outside every function and block belong to the **Global Scope**.

They can be accessed from anywhere.

Example

```javascript
let college = "BIET";

function showCollege() {
    console.log(college);
}

console.log(college);

showCollege();
```

Output

```text
BIET
BIET
```

Both the global code and the function can access `college`.

---

# ⚙️ Function Scope

Variables declared inside a function belong only to that function.

Example

```javascript
function greet() {
    let message = "Hello";

    console.log(message);
}

greet();
```

Output

```text
Hello
```

Trying to access it outside the function:

```javascript
console.log(message);
```

Output

```text
ReferenceError
```

Because `message` only exists inside `greet()`.

---

# 📦 Block Scope

A block is any code inside `{ }`.

Variables declared using `let` and `const` are block-scoped.

Example

```javascript
{
    let city = "Davangere";

    console.log(city);
}
```

Output

```text
Davangere
```

Outside the block

```javascript
console.log(city);
```

Output

```text
ReferenceError
```

---

# ⚠️ var is NOT Block Scoped

Example

```javascript
{
    var language = "JavaScript";
}

console.log(language);
```

Output

```text
JavaScript
```

Because `var` ignores block scope.

It only follows function scope.

---

# 🧠 Nested Scope

A function can be inside another function.

The inner function can access variables from the outer function.

Example

```javascript
function outer() {

    let name = "Chinmay";

    function inner() {

        console.log(name);

    }

    inner();
}

outer();
```

Output

```text
Chinmay
```

The inner function can access variables from the outer function.

---

# 🔗 Scope Chain

When JavaScript cannot find a variable in the current scope,

it searches the next outer scope.

This process continues until it reaches the global scope.

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

Search order

```text
Current Scope

↓

Outer Function

↓

Global Scope

↓

Not Found

↓

ReferenceError
```

This searching process is called the **Scope Chain**.

---

# 📊 Visual Diagram

```text
Global Scope

country

│

└──── outer()

       state

       │

       └──── inner()

              city
```

The `inner()` function can access:

✅ city

✅ state

✅ country

---

The `outer()` function can access:

✅ state

✅ country

❌ city

---

Global Scope can access:

✅ country

❌ state

❌ city

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking every variable is global

Variables declared inside functions are not accessible outside.

---

## ❌ Thinking var is block scoped

Wrong.

```javascript
{
    var x = 10;
}

console.log(x);
```

Works.

---

## ❌ Thinking outer functions can access inner variables

Wrong.

```javascript
function outer() {

    function inner() {

        let age = 20;

    }

    console.log(age);

}
```

Output

```text
ReferenceError
```

---

# 💼 Interview Questions

### What is Scope?

Scope determines where variables can be accessed.

---

### What are the three types of scope?

- Global Scope
- Function Scope
- Block Scope

---

### Is var block scoped?

No.

`var` is function-scoped.

---

### What is the Scope Chain?

The process of searching outer scopes when a variable is not found in the current scope.

---

### Can an outer function access variables inside an inner function?

No.

Only inner functions can access variables from outer functions.

---

# 📝 Revision Sheet

- Scope decides where variables are accessible.
- JavaScript has:
  - Global Scope
  - Function Scope
  - Block Scope
- `let` and `const` are block-scoped.
- `var` is function-scoped.
- Inner scopes can access outer variables.
- Outer scopes cannot access inner variables.
- JavaScript searches variables using the Scope Chain.

---

# 🧪 Practice Questions

1. What is Scope?
2. Why do we need Scope?
3. Name the three types of Scope.
4. Is `var` block-scoped?
5. Explain Function Scope.
6. Explain Block Scope.
7. What is the Scope Chain?
8. Can an outer function access variables of an inner function?

---

# 💻 Mini Exercise

Predict the output.

```javascript
let a = 10;

function one() {

    let b = 20;

    function two() {

        let c = 30;

        console.log(a);
        console.log(b);
        console.log(c);

    }

    two();

}

one();
```

### Expected Output

```text
10
20
30
```

---

Predict the output.

```javascript
function test() {

    let x = 100;

}

console.log(x);
```

### Expected Output

```text
ReferenceError
```

---

# 📌 Key Takeaways

- Scope determines where variables can be accessed.
- Global variables are accessible everywhere.
- Function variables are accessible only inside the function.
- Block variables (`let` and `const`) are accessible only inside the block.
- `var` ignores block scope and is function-scoped.
- JavaScript uses the Scope Chain to find variables.

---

⬅️ Previous: `03-Temporal-Dead-Zone.md`

➡️ Next: `05-Lexical-Environment.md`