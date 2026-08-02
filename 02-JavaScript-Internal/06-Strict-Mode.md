# Strict Mode in JavaScript

> 📚 Chapter 6 of JavaScript Internals

---

# 📑 Table of Contents

- What is Strict Mode?
- Why Do We Need It?
- How to Enable Strict Mode
- Rules in Strict Mode
- Common Errors Prevented
- Strict Mode in Functions
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Strict Mode?

**Strict Mode** is a special mode in JavaScript that helps you write **safer and cleaner code**.

It changes some JavaScript behaviors by:

- Preventing common mistakes
- Throwing errors for unsafe code
- Making debugging easier

Think of it as JavaScript becoming **more strict** about the rules.

---

# 🤔 Why Do We Need Strict Mode?

In normal JavaScript, some mistakes are silently ignored.

Example

```javascript
name = "Chinmay";

console.log(name);
```

Output

```text
Chinmay
```

Even though we never declared `name`.

This creates a global variable accidentally.

Strict Mode prevents this mistake.

---

# 🌍 Real-Life Analogy

Imagine two classrooms.

### Normal Classroom

The teacher is very relaxed.

Students can break a few rules without getting into trouble.

---

### Strict Classroom

The teacher checks everything carefully.

Even small mistakes are corrected immediately.

Strict Mode works the same way.

It catches mistakes as soon as they happen.

---

# ⚙️ How to Enable Strict Mode

Add this line at the top of your JavaScript file.

```javascript
"use strict";
```

Example

```javascript
"use strict";

let name = "Chinmay";

console.log(name);
```

---

# 📚 Strict Mode in a Function

Strict Mode can also be enabled inside a single function.

```javascript
function greet() {

    "use strict";

    let message = "Hello";

    console.log(message);

}
```

Only this function will follow Strict Mode.

---

# 🚫 Prevents Accidental Global Variables

Without Strict Mode

```javascript
age = 20;

console.log(age);
```

Output

```text
20
```

---

With Strict Mode

```javascript
"use strict";

age = 20;
```

Output

```text
ReferenceError
```

Because `age` was never declared.

---

# 🚫 Duplicate Parameter Names

Without Strict Mode

```javascript
function add(a, a) {

    return a + a;

}
```

This is allowed in non-strict mode (though it's a bad idea).

---

With Strict Mode

```javascript
"use strict";

function add(a, a) {

    return a + a;

}
```

Output

```text
SyntaxError
```

Parameter names must be unique.

---

# 🚫 Deleting Variables

```javascript
"use strict";

let age = 20;

delete age;
```

Output

```text
SyntaxError
```

Variables cannot be deleted.

---

# 📚 Makes Silent Errors Visible

Sometimes JavaScript ignores mistakes.

Strict Mode turns many of them into errors.

This makes debugging much easier.

---

# 📊 Without vs With Strict Mode

| Without Strict Mode | With Strict Mode |
|---------------------|------------------|
| Allows accidental global variables | Throws an error |
| Ignores some mistakes | Reports mistakes |
| Easier to write bad code | Encourages better code |
| Less safe | More safe |

---

# ⚠️ Common Beginner Mistakes

## ❌ Forgetting to declare variables

Wrong

```javascript
"use strict";

name = "Chinmay";
```

Correct

```javascript
"use strict";

let name = "Chinmay";
```

---

## ❌ Thinking Strict Mode changes JavaScript syntax

Wrong.

It doesn't create a new language.

It simply enforces stricter rules.

---

## ❌ Placing "use strict" in the wrong position

Correct

```javascript
"use strict";

let age = 20;
```

Wrong

```javascript
let age = 20;

"use strict";
```

To apply to the whole script, `"use strict"` should appear before other statements.

---

# 💼 Interview Questions

### What is Strict Mode?

A mode that enables stricter error checking and prevents unsafe JavaScript behavior.

---

### How do you enable Strict Mode?

```javascript
"use strict";
```

---

### Why should we use Strict Mode?

It helps catch bugs early, prevents accidental mistakes, and encourages cleaner code.

---

### Can Strict Mode be enabled inside a function?

Yes.

It only affects that function.

---

# 📝 Revision Sheet

- Strict Mode makes JavaScript safer.
- Enable it using `"use strict";`.
- It prevents accidental global variables.
- It catches many common programming mistakes.
- It can be enabled for an entire file or a single function.

---

# 🧪 Practice Questions

1. What is Strict Mode?
2. Why was Strict Mode introduced?
3. How do you enable Strict Mode?
4. What happens if you assign a value to an undeclared variable?
5. Can Strict Mode be enabled inside a function?

---

# 💻 Mini Exercise

Predict the output.

```javascript
"use strict";

age = 20;

console.log(age);
```

### Expected Output

```text
ReferenceError
```

---

Predict the output.

```javascript
"use strict";

let age = 20;

console.log(age);
```

### Expected Output

```text
20
```

---

# 📌 Key Takeaways

- Strict Mode helps write safer JavaScript.
- Enable it using `"use strict";`.
- It prevents accidental global variables.
- It catches common programming mistakes early.
- It improves code quality and debugging.

---

⬅️ Previous: `05-Lexical-Environment.md`

➡️ Next: `03-Type-Conversion/01-Type-Conversion.md`