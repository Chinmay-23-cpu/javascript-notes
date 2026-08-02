# Introduction to JavaScript

## 📖 What is JavaScript?

JavaScript (JS) is a **high-level, interpreted programming language** used to make web pages **interactive** and **dynamic**.

Without JavaScript, websites would only display static content.

### Examples of what JavaScript can do:

- Respond to button clicks
- Validate form inputs
- Display popups and alerts
- Create animations
- Build games
- Fetch data from servers
- Update web pages without reloading

---

# ❓ Why Learn JavaScript?

JavaScript is one of the most popular programming languages because it can be used almost everywhere.

It is used for:

- 🌐 Frontend Development
- ⚙️ Backend Development (Node.js)
- 📱 Mobile Applications
- 💻 Desktop Applications
- 🧩 Browser Extensions
- 🎮 Games
- 🤖 AI Applications
- 🔗 APIs

---

# 🏗️ The Three Building Blocks of a Website

| Technology | Purpose |
|------------|----------|
| HTML | Structure of the webpage |
| CSS | Styling of the webpage |
| JavaScript | Makes the webpage interactive |

### Easy Analogy

```text
HTML       → Skeleton 🦴

CSS        → Clothes 👕

JavaScript → Brain 🧠
```

Without JavaScript, a webpage cannot react to user actions.

---

# ⚙️ How JavaScript Works

```text
User opens website
        │
        ▼
Browser downloads HTML
        │
        ▼
Browser downloads CSS
        │
        ▼
Browser downloads JavaScript
        │
        ▼
JavaScript executes
        │
        ▼
The webpage becomes interactive
```

---

# 🌍 Where Can JavaScript Run?

Originally, JavaScript could only run inside web browsers.

Examples:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

Today, JavaScript can also run outside the browser using **Node.js**.

---

# 👋 Your First JavaScript Program

```javascript
console.log("Hello World!");
```

### Output

```text
Hello World!
```

---

# 💬 Comments

Comments are ignored by JavaScript.

They are used to explain code.

## Single-line Comment

```javascript
// This is a comment
```

## Multi-line Comment

```javascript
/*
This is a
multi-line comment
*/
```

---

# 🔠 Case Sensitivity

JavaScript is **case-sensitive**.

```javascript
let age = 20;
let Age = 30;

console.log(age);
console.log(Age);
```

### Output

```text
20
30
```

These are two different variables.

---

# 🔑 Keywords

Keywords are reserved words that already have a meaning in JavaScript.

Examples:

```javascript
let
const
if
else
for
while
return
function
class
new
```

❌ Wrong

```javascript
let if = 20;
```

---

# 🏷️ Identifiers

Identifiers are names given by programmers to variables, functions, classes, etc.

### Good Examples

```javascript
let studentAge;
let totalMarks;

function calculateArea() {}
```

### Bad Example

```javascript
let x;
```

Meaningful names make code easier to read.

---

# 📚 Real-Life Example

Imagine a library.

```text
Book ID 101 → Harry Potter

Book ID 102 → Atomic Habits
```

The IDs help identify the correct book.

Similarly, variables use identifiers to store and access data.

---

# ⚠️ Common Beginner Mistakes

## ❌ JavaScript and Java are the same language

They are completely different programming languages.

---

## ❌ Writing `Console.log()`

```javascript
Console.log("Hello");
```

Correct:

```javascript
console.log("Hello");
```

JavaScript is case-sensitive.

---

## ❌ Forgetting Semicolons

Modern JavaScript automatically inserts semicolons in many cases (Automatic Semicolon Insertion), so code often works without them.

However, using semicolons consistently is considered a good practice.

---

# 💼 Interview Questions

### 1. What is JavaScript?

JavaScript is a high-level programming language used to make websites interactive.

---

### 2. Is JavaScript interpreted or compiled?

Modern JavaScript engines use **Just-In-Time (JIT) compilation**, combining compilation and interpretation for better performance.

---

### 3. Can JavaScript run without a browser?

Yes.

Using **Node.js**, JavaScript can run outside the browser.

---

# 📝 Revision Sheet

Remember these five points:

- JavaScript makes webpages interactive.
- HTML provides structure.
- CSS provides styling.
- JavaScript provides behavior.
- JavaScript can run in browsers and Node.js.

---

# 🧪 Practice Questions

1. What is JavaScript?
2. Why is JavaScript used?
3. Differentiate HTML, CSS, and JavaScript.
4. What are comments?
5. What are identifiers?
6. What are keywords?
7. Is JavaScript case-sensitive?
8. Can JavaScript run without a browser?

---

# 💻 Mini Exercise

Create a file named `intro.js`.

Write a JavaScript program to print:

```text
Hello!

My name is Chinmay.

I am learning JavaScript.
```

Expected solution:

```javascript
console.log("Hello!");
console.log("My name is Chinmay.");
console.log("I am learning JavaScript.");
```

---

# 📌 Key Takeaways

- JavaScript adds interactivity to web pages.
- HTML, CSS, and JavaScript work together to build websites.
- JavaScript is case-sensitive.
- Comments improve code readability.
- Node.js allows JavaScript to run outside the browser.