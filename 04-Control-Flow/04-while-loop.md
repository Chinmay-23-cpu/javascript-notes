# while Loop

> 📚 Chapter 4 of Control Flow

---

## 📖 Imagine This...

You're building a game.

The player has **3 lives**.

As long as the player still has lives left, the game continues.

When the lives become **0**, the game ends.

You don't know exactly **how many actions** the player will take.

You only know **when to stop**.

This is the perfect situation for a `while` loop.

---

# 🤔 What is a while Loop?

A `while` loop keeps running **as long as a condition is true**.

Unlike a `for` loop, you don't usually use it when you know the exact number of iterations.

---

# 🧠 Syntax

```javascript
while (condition) {

    // code

}
```

Very simple.

Read it like English.

> **While the condition is true, keep running this code.**

---

# 💻 Example 1

```javascript
let i = 1;

while (i <= 5) {

    console.log(i);

    i++;

}
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
i = 1

↓

Is 1 <= 5 ?

↓

Yes ✅

↓

Print 1

↓

Increase i

↓

Repeat
```

When

```text
i = 6
```

The condition becomes false.

The loop stops.

---

# 💻 Example 2

Countdown

```javascript
let count = 5;

while (count > 0) {

    console.log(count);

    count--;

}
```

### Output

```text
5
4
3
2
1
```

---

# 🌍 Real-Life Examples

### Login System

Keep asking for the password until it's correct.

```text
Wrong Password

↓

Try Again

↓

Wrong Password

↓

Try Again

↓

Correct Password

↓

Login Successful
```

---

### Download Progress

```text
Downloading...

10%

25%

50%

75%

100%

Download Complete
```

The loop continues until progress reaches 100%.

---

### Game

```text
Lives > 0 ?

↓

Yes

↓

Continue Playing

↓

Lose One Life

↓

Check Again
```

---

# 🆚 for vs while

## for Loop

Use when you know the number of repetitions.

```javascript
for (let i = 1; i <= 10; i++) {

    console.log(i);

}
```

---

## while Loop

Use when you only know the stopping condition.

```javascript
let battery = 100;

while (battery > 0) {

    battery--;

}
```

---

# 🌐 Using while in Websites

Imagine checking whether a user has entered a valid OTP.

```text
Wrong OTP

↓

Ask Again

↓

Wrong OTP

↓

Ask Again

↓

Correct OTP

↓

Continue
```

You don't know how many attempts the user will take.

A `while` loop is a natural fit.

---

# ⚠️ Common Beginner Mistakes

## ❌ Forgetting to Update the Variable

```javascript
let i = 1;

while (i <= 5) {

    console.log(i);

}
```

The condition is always true.

The loop never ends.

---

Correct

```javascript
let i = 1;

while (i <= 5) {

    console.log(i);

    i++;

}
```

---

## ❌ Wrong Condition

```javascript
let i = 10;

while (i < 5) {

    console.log(i);

}
```

The condition is false from the beginning.

The loop never runs.

---

# 💼 Interview Questions

### When should we use a `while` loop?

When we don't know the exact number of iterations, but we know the condition that should stop the loop.

---

### What's the biggest mistake beginners make with `while` loops?

Forgetting to update the variable, causing an infinite loop.

---

### Does a `while` loop always execute at least once?

No.

If the condition is false initially, it doesn't run even once.

---

# 📝 Quick Revision

✅ `while` repeats code while a condition is true.

✅ Best when the number of iterations is unknown.

✅ Always update the variable inside the loop.

✅ If the condition is false initially, the loop never executes.

---

# 💻 Mini Exercise

### Predict the output

```javascript
let i = 3;

while (i <= 6) {

    console.log(i);

    i++;

}
```

---

### Predict the output

```javascript
let i = 5;

while (i < 5) {

    console.log(i);

}
```

---

### Write a `while` loop that prints

```text
10
8
6
4
2
```

---

# 📌 Key Takeaways

- `while` loops repeat code based on a condition.
- Use them when you don't know how many times the loop will run.
- The condition is checked **before** every iteration.
- Don't forget to update the loop variable.
- A `while` loop may execute **zero times**.

---

⬅️ Previous: `03-for-loop.md`

➡️ Next: `05-do-while-loop.md`