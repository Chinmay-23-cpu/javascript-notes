# for Loop

> 📚 Chapter 3 of Control Flow

---

## 📖 Imagine This...

Suppose your teacher says,

> Write "I will practice JavaScript" **100 times**.

Would you write

```javascript
console.log("I will practice JavaScript");
```

100 times?

Of course not.

This is exactly why loops exist.

A loop repeats a block of code until a condition becomes false.

---

# 🤔 What is a for Loop?

A `for` loop is used when you know **how many times** you want to repeat something.

Instead of writing the same code again and again, you write it once inside the loop.

---

# 🧠 Syntax

```javascript
for (initialization; condition; update) {

    // code to repeat

}
```

Looks confusing?

Let's understand each part.

---

## 1️⃣ Initialization

Runs **only once**.

Usually used to create a counter.

```javascript
let i = 1;
```

---

## 2️⃣ Condition

Checked **before every iteration**.

If it becomes `false`, the loop stops.

```javascript
i <= 5
```

---

## 3️⃣ Update

Runs after every iteration.

Usually increases or decreases the counter.

```javascript
i++
```

---

# 💻 Example 1

```javascript
for (let i = 1; i <= 5; i++) {

    console.log(i);

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

# 🧠 How it actually works

Let's slow it down.

### First Iteration

```text
i = 1

↓

1 <= 5 ✅

↓

Print 1

↓

i++
```

---

### Second Iteration

```text
i = 2

↓

2 <= 5 ✅

↓

Print 2

↓

i++
```

This continues until

```text
i = 6

↓

6 <= 5 ❌

↓

Loop Stops
```

---

# 💻 Example 2

Print even numbers.

```javascript
for (let i = 2; i <= 10; i += 2) {

    console.log(i);

}
```

### Output

```text
2
4
6
8
10
```

---

# 💻 Example 3

Countdown

```javascript
for (let i = 5; i >= 1; i--) {

    console.log(i);

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

### Sending Invitations

```text
Invite Student 1

Invite Student 2

Invite Student 3

...

Invite Student 100
```

Instead of writing 100 statements,

a loop repeats the same task.

---

### Printing a Table

```javascript
let number = 5;

for (let i = 1; i <= 10; i++) {

    console.log(number * i);

}
```

Output

```text
5
10
15
20
25
30
35
40
45
50
```

---

# 📊 Flow of a for Loop

```text
Initialization

      │

      ▼

 Condition

      │

 True ─────────► Execute Code

      ▲               │

      │               ▼

      └──────── Update

False

↓

Loop Ends
```

---

# 🆚 Java vs JavaScript

If you've learned Java, this will look familiar.

Java

```java
for(int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

JavaScript

```javascript
for(let i = 1; i <= 5; i++) {
    console.log(i);
}
```

The syntax is almost the same.

The main difference is:

- Java uses `System.out.println()`
- JavaScript uses `console.log()`

---

# 🌐 Using for Loops in Websites

Suppose you have an array of products.

```javascript
let products = ["Laptop", "Phone", "Tablet"];
```

You can display all products.

```javascript
for (let i = 0; i < products.length; i++) {

    console.log(products[i]);

}
```

Later, when learning the DOM, you'll use loops to:

- Create product cards
- Display comments
- Show notifications
- Build menus
- Render API data

Loops are everywhere in web development.

---

# ⚠️ Common Beginner Mistakes

## ❌ Infinite Loop

```javascript
for (let i = 1; i <= 5;) {

    console.log(i);

}
```

Forgot to update `i`.

The condition never becomes false.

---

## ❌ Wrong Condition

```javascript
for (let i = 1; i >= 5; i++)
```

Output

Nothing.

Because

```text
1 >= 5
```

is already false.

---

## ❌ Off-by-One Error

```javascript
for (let i = 1; i < 5; i++)
```

Output

```text
1
2
3
4
```

If you wanted to print `5`, the condition should be

```javascript
i <= 5
```

---

# 💼 Interview Questions

### When should we use a `for` loop?

When we know how many times we want to repeat a task.

---

### Which part of a `for` loop runs only once?

Initialization.

---

### Which part decides when the loop stops?

The condition.

---

### What causes an infinite loop?

When the condition never becomes false.

---

# 📝 Quick Revision

✅ `for` loops repeat code.

✅ Initialization runs once.

✅ Condition is checked before every iteration.

✅ Update runs after every iteration.

✅ The loop stops when the condition becomes false.

---

# 💻 Mini Exercise

Predict the output.

```javascript
for (let i = 3; i <= 7; i++) {

    console.log(i);

}
```

---

Predict the output.

```javascript
for (let i = 10; i >= 5; i -= 2) {

    console.log(i);

}
```

---

Write a loop that prints

```text
2
4
6
8
10
```

---

# 📌 Key Takeaways

- A `for` loop repeats code.
- Use it when the number of iterations is known.
- It has three parts:
  - Initialization
  - Condition
  - Update
- Forgetting the update may cause an infinite loop.
- `for` loops are heavily used in web development to display lists, products, comments, and API data.

---

⬅️ Previous: `02-switch.md`

➡️ Next: `04-while-loop.md`