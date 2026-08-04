# if...else Statement

> 📚 Chapter 1 of Control Flow

---

## 📖 Imagine This...

You're building a login page.

If the password is correct,

➡️ Allow the user to log in.

Otherwise,

➡️ Show **"Invalid Password"**.

How does JavaScript make this decision?

Using an **if...else** statement.

---

# 🤔 What is if...else?

An `if...else` statement allows JavaScript to make decisions.

It checks a condition.

- If the condition is **true**, one block of code runs.
- If the condition is **false**, another block runs.

Think of it as asking a question.

```text
Is it raining?

      │
      ▼

    Yes? ─────► Take an umbrella ☔

      │

      ▼

     No ─────► Enjoy your walk 😄
```

---

# 🧠 Syntax

```javascript
if (condition) {

    // Runs if the condition is true

} else {

    // Runs if the condition is false

}
```

---

# 💻 Example 1

```javascript
let age = 20;

if (age >= 18) {
    console.log("You can vote.");
} else {
    console.log("You cannot vote.");
}
```

### Output

```text
You can vote.
```

---

# 💻 Example 2

```javascript
let marks = 35;

if (marks >= 35) {
    console.log("Pass");
} else {
    console.log("Fail");
}
```

### Output

```text
Pass
```

---

# 💻 Example 3

```javascript
let isLoggedIn = false;

if (isLoggedIn) {
    console.log("Welcome!");
} else {
    console.log("Please log in.");
}
```

### Output

```text
Please log in.
```

Notice that `isLoggedIn` is already a boolean.

So we don't write

```javascript
if (isLoggedIn === true)
```

Simply writing

```javascript
if (isLoggedIn)
```

is enough.

---

# 📚 else if

Sometimes there are more than two possibilities.

Example:

A grading system.

```javascript
let marks = 82;

if (marks >= 90) {

    console.log("Grade A");

} else if (marks >= 75) {

    console.log("Grade B");

} else if (marks >= 50) {

    console.log("Grade C");

} else {

    console.log("Fail");

}
```

### Output

```text
Grade B
```

JavaScript checks the conditions **from top to bottom**.

As soon as one condition becomes `true`, it stops checking the rest.

---

# 📊 Flow of if...else

```text
           Condition

               │

        ┌──────┴──────┐

      True          False

        │              │

Run if block     Run else block
```

---

# 🌍 Real-Life Examples

### ATM Machine

```text
Enough Balance?

      │

   Yes ▼ No

Withdraw   Show "Insufficient Balance"
```

---

### College Attendance

```text
Attendance >= 75%

       │

   Yes ▼ No

Write Exam   Not Eligible
```

---

### Login System

```javascript
let password = "admin123";

if (password === "admin123") {
    console.log("Login Successful");
} else {
    console.log("Wrong Password");
}
```

---

# ⚠️ Common Beginner Mistakes

## ❌ Using = instead of ===

Wrong

```javascript
if (age = 18)
```

`=` assigns a value.

Correct

```javascript
if (age === 18)
```

`===` compares values.

---

## ❌ Forgetting Curly Braces

```javascript
if (age >= 18)
    console.log("Adult");
```

This works for one line, but it's safer to always use braces.

```javascript
if (age >= 18) {
    console.log("Adult");
}
```

---

## ❌ Checking Boolean Variables Incorrectly

Instead of

```javascript
if (isLoggedIn === true)
```

Write

```javascript
if (isLoggedIn)
```

It is cleaner and more common.

---

# 💼 Interview Questions

### Difference between `if` and `if...else`?

- `if` runs code only when the condition is true.
- `if...else` handles both true and false cases.

---

### What is `else if` used for?

When you have multiple conditions to check.

---

### Does JavaScript check every `else if`?

No.

It stops as soon as one condition is true.

---

# 📝 Quick Revision

✅ `if` checks a condition.

✅ `else` runs when the condition is false.

✅ `else if` is used for multiple conditions.

✅ Conditions are checked from top to bottom.

✅ Use `===` for comparisons.

---

# 💻 Mini Exercise

Predict the output.

```javascript
let temperature = 32;

if (temperature > 35) {

    console.log("Very Hot");

} else if (temperature > 25) {

    console.log("Pleasant Weather");

} else {

    console.log("Cold");

}
```

---

Predict the output.

```javascript
let username = "";

if (username) {

    console.log("Welcome");

} else {

    console.log("Please Enter Username");

}
```

(Hint: Think about **Truthy and Falsy Values**.)

---

# 📌 Key Takeaways

- `if...else` is used to make decisions.
- `else if` helps check multiple conditions.
- JavaScript stops checking once it finds a true condition.
- Prefer `===` over `==`.
- Boolean variables can be used directly in conditions.

---

⬅️ Previous: `03-Type-Conversion/03-Truthy-and-Falsy.md`

➡️ Next: `02-switch.md`