# Loop Control & Logical Operators

> 📚 Chapter 6 of Control Flow

---

## 📖 Imagine This...

You're searching for your friend in a classroom.

You enter one room after another.

- As soon as you find your friend, you stop searching. (**break**)
- If one classroom is locked, you skip it and check the next one. (**continue**)
- You also check:

> Is he wearing a blue shirt **AND** carrying a bag?

That's where logical operators come in.

---

# 🧠 break

`break` immediately stops the loop.

Once JavaScript encounters `break`, it exits the loop completely.

### Example

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 5) {
        break;
    }

    console.log(i);

}
```

### Output

```text
1
2
3
4
```

When `i` becomes `5`, the loop ends.

---

## 🌍 Real-Life Example

Imagine looking for your keys.

```text
Drawer 1 ❌

Drawer 2 ❌

Drawer 3 ✅

↓

Stop Searching
```

Once you find the keys,

you don't continue checking the remaining drawers.

---

# 🧠 continue

`continue` skips the current iteration and moves to the next one.

The loop **does not stop**.

### Example

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 3) {
        continue;
    }

    console.log(i);

}
```

### Output

```text
1
2
4
5
```

Only `3` is skipped.

---

## 🌍 Real-Life Example

Imagine taking attendance.

```text
Roll 1 ✔

Roll 2 ✔

Roll 3 Absent

↓

Skip

↓

Roll 4 ✔
```

You don't stop taking attendance.

You simply move to the next student.

---

# 🆚 break vs continue

| break | continue |
|--------|----------|
| Stops the loop completely | Skips only the current iteration |
| Execution ends | Execution continues |

---

# 🧠 Logical Operators

Logical operators combine multiple conditions.

JavaScript has three logical operators.

```text
&&   AND

||   OR

!    NOT
```

---

# AND (&&)

`&&` returns `true` only when **both conditions are true**.

### Example

```javascript
let age = 20;
let hasLicense = true;

if (age >= 18 && hasLicense) {

    console.log("You can drive.");

}
```

### Output

```text
You can drive.
```

---

### Real-Life Example

To enter an exam hall,

you need

```text
Hall Ticket

AND

College ID
```

Missing either one means you can't enter.

---

# OR (||)

`||` returns `true` if **at least one condition is true**.

### Example

```javascript
let isWeekend = false;
let isHoliday = true;

if (isWeekend || isHoliday) {

    console.log("No College!");

}
```

### Output

```text
No College!
```

---

### Real-Life Example

You can pay using

- Cash

OR

- UPI

OR

- Card

Only one payment method is enough.

---

# NOT (!)

`!` reverses a boolean value.

### Example

```javascript
let isLoggedIn = false;

console.log(!isLoggedIn);
```

### Output

```text
true
```

---

### Real-Life Example

```text
Door Open

↓

!Door Open

↓

Door Closed
```

---

# Combining Conditions

Logical operators are commonly used with `if`.

Example

```javascript
let marks = 85;
let attendance = 80;

if (marks >= 35 && attendance >= 75) {

    console.log("Eligible for Exam");

}
```

---

Another example

```javascript
let username = "";

if (!username) {

    console.log("Username Required");

}
```

Notice how **Truthy & Falsy Values** are useful here.

---

# ⚠️ Common Beginner Mistakes

## ❌ Using & instead of &&

Wrong

```javascript
if (age > 18 & hasLicense)
```

Correct

```javascript
if (age > 18 && hasLicense)
```

---

## ❌ Thinking break skips one iteration

No.

`break` ends the entire loop.

---

## ❌ Thinking continue ends the loop

No.

It only skips one iteration.

The loop continues.

---

# 💼 Interview Questions

### Difference between break and continue?

- `break` exits the loop.
- `continue` skips the current iteration.

---

### When should we use &&?

When **all conditions** must be true.

---

### When should we use ||?

When **at least one condition** should be true.

---

### What does ! do?

It reverses a boolean value.

---

# 📝 Quick Revision

✅ `break` stops the loop.

✅ `continue` skips one iteration.

✅ `&&` → Both conditions must be true.

✅ `||` → At least one condition must be true.

✅ `!` → Reverses a boolean.

---

# 💻 Mini Exercise

### Predict the output

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 4) {
        break;
    }

    console.log(i);

}
```

---

### Predict the output

```javascript
for (let i = 1; i <= 5; i++) {

    if (i % 2 === 0) {
        continue;
    }

    console.log(i);

}
```

---

### Predict the output

```javascript
let age = 20;
let hasID = false;

console.log(age >= 18 && hasID);

console.log(age >= 18 || hasID);

console.log(!hasID);
```

---

# 📌 Key Takeaways

- `break` exits the loop immediately.
- `continue` skips the current iteration.
- `&&` requires all conditions to be true.
- `||` requires at least one condition to be true.
- `!` reverses a boolean value.
- Logical operators are commonly used with `if` statements and loops.

---

⬅️ Previous: `05-do-while-loop.md`

➡️ Next: `05-Functions/01-Introduction-to-Functions.md`