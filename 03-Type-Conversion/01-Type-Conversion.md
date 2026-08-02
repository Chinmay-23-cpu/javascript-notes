# Type Conversion in JavaScript

> 📚 Chapter 1 of Type Conversion & Type Coercion

---

# 📑 Table of Contents

- What is Type Conversion?
- Why Do We Need It?
- Implicit vs Explicit Conversion
- String Conversion
- Number Conversion
- Boolean Conversion
- Common Conversion Methods
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Type Conversion?

**Type Conversion** is the process of converting a value from one data type to another.

For example,

```javascript
let age = "20";
```

Here, `age` is a **string**.

If we want to perform mathematical operations, we need to convert it into a **number**.

```javascript
let age = Number("20");

console.log(age);
```

Output

```text
20
```

Now `age` is a number.

---

# 🤔 Why Do We Need Type Conversion?

Imagine you get data from a form.

```javascript
let age = "20";
```

Even though it looks like a number,

it's actually a **string**.

If you write

```javascript
console.log(age + 5);
```

Output

```text
205
```

Instead of

```text
25
```

So we convert it first.

```javascript
age = Number(age);

console.log(age + 5);
```

Output

```text
25
```

---

# 🌍 Real-Life Analogy

Imagine a person travels to another country.

Their money must be exchanged.

```text
💵 Dollars

↓

Currency Exchange

↓

💶 Euros
```

The value remains the same.

Only the type changes.

Type Conversion works in the same way.

---

# 📚 Types of Conversion

JavaScript supports two kinds of conversion.

```text
Type Conversion

│

├── Explicit Conversion (Manual)

└── Implicit Conversion (Automatic)
```

This chapter focuses on **Explicit Conversion**.

We'll study **Implicit Conversion (Type Coercion)** in the next chapter.

---

# ✋ Explicit Conversion

Explicit conversion means **you convert the value yourself**.

Example

```javascript
Number("25")
```

JavaScript converts it because **you asked it to**.

---

# 🔢 Number Conversion

Convert a value into a number.

Syntax

```javascript
Number(value)
```

Example

```javascript
let age = "20";

let result = Number(age);

console.log(result);
```

Output

```text
20
```

---

### More Examples

```javascript
Number("100");
```

Output

```text
100
```

---

```javascript
Number(true);
```

Output

```text
1
```

---

```javascript
Number(false);
```

Output

```text
0
```

---

```javascript
Number(null);
```

Output

```text
0
```

---

```javascript
Number(undefined);
```

Output

```text
NaN
```

---

```javascript
Number("Hello");
```

Output

```text
NaN
```

---

# 📝 What is NaN?

`NaN` stands for

```text
Not a Number
```

It means JavaScript tried to convert something into a number but couldn't.

Example

```javascript
Number("JavaScript");
```

Output

```text
NaN
```

---

# 🔤 String Conversion

Convert values into strings.

Syntax

```javascript
String(value)
```

Example

```javascript
String(100);
```

Output

```text
"100"
```

---

```javascript
String(true);
```

Output

```text
"true"
```

---

```javascript
String(null);
```

Output

```text
"null"
```

---

# ✅ Boolean Conversion

Convert values into boolean values.

Syntax

```javascript
Boolean(value)
```

---

```javascript
Boolean(1);
```

Output

```text
true
```

---

```javascript
Boolean(0);
```

Output

```text
false
```

---

```javascript
Boolean("");
```

Output

```text
false
```

---

```javascript
Boolean("Hello");
```

Output

```text
true
```

---

```javascript
Boolean(null);
```

Output

```text
false
```

---

```javascript
Boolean(undefined);
```

Output

```text
false
```

---

# 📚 Summary Table

| Conversion | Example | Result |
|------------|---------|--------|
| Number | `Number("25")` | `25` |
| Number | `Number(true)` | `1` |
| Number | `Number(false)` | `0` |
| Number | `Number("Hello")` | `NaN` |
| String | `String(50)` | `"50"` |
| String | `String(true)` | `"true"` |
| Boolean | `Boolean(1)` | `true` |
| Boolean | `Boolean(0)` | `false` |
| Boolean | `Boolean("")` | `false` |
| Boolean | `Boolean("Hello")` | `true` |

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking `"20"` is a number

Wrong.

```javascript
let age = "20";
```

This is a string.

---

## ❌ Confusing NaN

```javascript
Number("Hello");
```

Returns

```text
NaN
```

This doesn't mean JavaScript crashed.

It means the conversion failed.

---

## ❌ Forgetting to convert form input

Form inputs usually return strings.

Always convert them if you need numbers.

---

# 💼 Interview Questions

### What is Type Conversion?

The process of converting one data type into another.

---

### What is Explicit Type Conversion?

When the programmer manually converts a value using functions like `Number()`, `String()`, or `Boolean()`.

---

### What does `Number("Hello")` return?

```text
NaN
```

---

### What does NaN mean?

It stands for **Not a Number** and indicates a failed numeric conversion.

---

# 📝 Revision Sheet

- Type Conversion changes one data type into another.
- Explicit Conversion is done manually.
- Use:
  - `Number()`
  - `String()`
  - `Boolean()`
- `NaN` means conversion to a number failed.
- Form input values are usually strings.

---

# 🧪 Practice Questions

1. What is Type Conversion?
2. What is Explicit Conversion?
3. What is `NaN`?
4. What does `Number(true)` return?
5. What does `Boolean("")` return?
6. What does `String(false)` return?

---

# 💻 Mini Exercise

Predict the output.

```javascript
console.log(Number("100"));
console.log(Number(true));
console.log(Number(false));
console.log(Number("Hello"));

console.log(String(500));

console.log(Boolean(""));
console.log(Boolean("JavaScript"));
```

### Expected Output

```text
100
1
0
NaN
"500"
false
true
```

---

# 📌 Key Takeaways

- Type Conversion changes the data type of a value.
- Explicit Conversion is performed manually.
- `Number()`, `String()`, and `Boolean()` are the main conversion functions.
- `NaN` means JavaScript could not convert a value into a number.
- Always convert form input values when numeric operations are needed.

---

⬅️ Previous: `02-JavaScript-Internals/06-Strict-Mode.md`

➡️ Next: `02-Type-Coercion.md`