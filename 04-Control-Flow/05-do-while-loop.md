# do...while Loop

> 📚 Chapter 5 of Control Flow

---

## 📖 Imagine This...

You're creating an ATM.

The ATM should **always show the menu once**.

After that, it asks:

> "Do you want to perform another transaction?"

If the user says **Yes**, show the menu again.

If **No**, exit.

Notice something?

The menu is shown **at least once**, no matter what.

That's exactly what a `do...while` loop does.

---

# 🤔 What is a do...while Loop?

A `do...while` loop is almost the same as a `while` loop.

The difference is:

> The code runs **at least one time**, even if the condition is false.

---

# 🧠 Syntax

```javascript
do {

    // code

} while (condition);
```

Read it like English.

> Do this first.

Then check the condition.

If it's true, repeat.

---

# 💻 Example 1

```javascript
let i = 1;

do {

    console.log(i);

    i++;

} while (i <= 5);
```

### Output

```text
1
2
3
4
5
```

---

# 🧠 How it Works

```text
Run Code

↓

Check Condition

↓

True?

↓

Repeat

↓

False?

↓

Stop
```

Notice the difference.

The code runs **before** checking the condition.

---

# 💻 Example 2

```javascript
let i = 10;

do {

    console.log(i);

} while (i < 5);
```

### Output

```text
10
```

Even though

```javascript
i < 5
```

is false,

the loop still runs **once**.

---

# 🌍 Real-Life Examples

### ATM Menu

```text
Show Menu

↓

Withdraw?

↓

Deposit?

↓

Exit?

↓

Another Transaction?

↓

Yes → Show Menu Again

No → Exit
```

---

### Feedback Form

```text
Show Form

↓

User Fills It

↓

Submit?

↓

If invalid

↓

Show Again
```

The form is displayed at least once.

---

# 🆚 while vs do...while

## while

Condition is checked first.

```javascript
while (condition) {

    // code

}
```

If the condition is false,

the loop runs **0 times**.

---

## do...while

Code runs first.

```javascript
do {

    // code

} while (condition);
```

Even if the condition is false,

the loop runs **1 time**.

---

# 📊 Visual Comparison

## while

```text
Condition

↓

True?

↓

Run Code

↓

Repeat
```

---

## do...while

```text
Run Code

↓

Condition

↓

True?

↓

Repeat
```

---

# 🌐 Using do...while in Websites

Imagine a popup asking users to accept cookies.

The popup should appear once.

If they haven't accepted,

show it again.

A `do...while` loop matches this idea because the popup must be shown at least once.

---

# ⚠️ Common Beginner Mistakes

## ❌ Forgetting the Semicolon

Wrong

```javascript
do {

    console.log("Hello");

} while (false)
```

Correct

```javascript
do {

    console.log("Hello");

} while (false);
```

Notice the semicolon.

---

## ❌ Thinking It Behaves Like while

No.

`do...while` always executes once before checking the condition.

---

# 💼 Interview Questions

### Difference between `while` and `do...while`?

- `while` checks the condition first.
- `do...while` executes the code first.

---

### Can a `do...while` loop execute if the condition is false?

Yes.

It always runs at least once.

---

### When should we use `do...while`?

When the code must execute at least one time before checking the condition.

---

# 📝 Quick Revision

✅ `do...while` executes the code first.

✅ The condition is checked later.

✅ It always runs at least once.

✅ Don't forget the semicolon after `while(condition);`

---

# 💻 Mini Exercise

### Predict the output

```javascript
let i = 5;

do {

    console.log(i);

    i++;

} while (i < 5);
```

---

### Predict the output

```javascript
let i = 1;

do {

    console.log(i);

    i++;

} while (i <= 3);
```

---

### Which loop would you choose?

You want to display a login screen **at least once**, even if the user is already logged in.

- `while`
- `do...while`

Why?

---

# 📌 Key Takeaways

- `do...while` is similar to `while`.
- The main difference is that it executes the code before checking the condition.
- It always runs at least once.
- Remember the semicolon after `while(condition);`

---

⬅️ Previous: `04-while-loop.md`

➡️ Next: `06-break-and-continue.md`