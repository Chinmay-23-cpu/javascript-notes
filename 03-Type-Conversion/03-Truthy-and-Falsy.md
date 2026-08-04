# Truthy and Falsy Values in JavaScript

> 📚 Chapter 3 of Type Conversion & Type Coercion

---

# 📑 Table of Contents

- What are Truthy and Falsy Values?
- Why Do We Need Them?
- Boolean Conversion
- Falsy Values
- Truthy Values
- Truthy vs True
- Real-Life Examples
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What are Truthy and Falsy Values?

In JavaScript, every value has an **inherent boolean behavior**.

When JavaScript expects a boolean (for example, inside an `if` statement), it automatically converts the value to either:

- `true`
- `false`

This process is called **Boolean Coercion**.

---

# 🤔 Why Do We Need Truthy and Falsy Values?

Imagine checking if a user entered a name.

Instead of writing

```javascript
if (username !== "") {
    console.log("Welcome");
}
```

JavaScript lets us simply write

```javascript
if (username) {
    console.log("Welcome");
}
```

Cleaner.

Shorter.

Easier to read.

---

# 🌍 Real-Life Analogy

Imagine a light switch.

```text
ON

↓

Electricity flows

↓

Bulb glows
```

```text
OFF

↓

No electricity

↓

Bulb stays off
```

Similarly,

JavaScript treats values as either

```text
ON (Truthy)

OFF (Falsy)
```

---

# 🔄 Boolean Conversion

JavaScript internally does something like

```javascript
Boolean(value)
```

Example

```javascript
Boolean("Hello");
```

Output

```text
true
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

# ❌ Falsy Values

There are only **8 falsy values** in JavaScript.

```text
false

0

-0

0n

""

null

undefined

NaN
```

Every other value is **truthy**.

---

## false

```javascript
Boolean(false);
```

Output

```text
false
```

---

## 0

```javascript
Boolean(0);
```

Output

```text
false
```

---

## -0

```javascript
Boolean(-0);
```

Output

```text
false
```

---

## 0n (BigInt Zero)

```javascript
Boolean(0n);
```

Output

```text
false
```

---

## Empty String

```javascript
Boolean("");
```

Output

```text
false
```

---

## null

```javascript
Boolean(null);
```

Output

```text
false
```

---

## undefined

```javascript
Boolean(undefined);
```

Output

```text
false
```

---

## NaN

```javascript
Boolean(NaN);
```

Output

```text
false
```

---

# ✅ Truthy Values

Everything that is **not falsy** is truthy.

Examples

```javascript
Boolean("JavaScript");
```

Output

```text
true
```

---

```javascript
Boolean(100);
```

Output

```text
true
```

---

```javascript
Boolean(-50);
```

Output

```text
true
```

---

```javascript
Boolean([]);
```

Output

```text
true
```

---

```javascript
Boolean({});
```

Output

```text
true
```

---

```javascript
Boolean(function(){});
```

Output

```text
true
```

---

# 📚 Truthy vs True

These are **not the same thing**.

Example

```javascript
let name = "Chinmay";

if (name) {
    console.log("Hello");
}
```

Output

```text
Hello
```

`name` is **not** equal to `true`.

```javascript
console.log(name === true);
```

Output

```text
false
```

It is simply **truthy**.

---

# 💻 Real-Life Examples

## Login System

```javascript
let username = "Chinmay";

if (username) {
    console.log("Login Successful");
}
```

---

## Empty Form

```javascript
let email = "";

if (!email) {
    console.log("Email Required");
}
```

---

## Shopping Cart

```javascript
let cartItems = 5;

if (cartItems) {
    console.log("Proceed to Checkout");
}
```

---

# 📊 Summary Table

| Value | Boolean Result |
|---------|---------------|
| false | false |
| 0 | false |
| -0 | false |
| 0n | false |
| "" | false |
| null | false |
| undefined | false |
| NaN | false |
| "Hello" | true |
| 100 | true |
| -5 | true |
| [] | true |
| {} | true |
| function(){} | true |

---

# ⚠️ Common Beginner Mistakes

## ❌ Thinking an empty array is falsy

```javascript
if ([]) {
    console.log("Runs");
}
```

Output

```text
Runs
```

Arrays are truthy.

---

## ❌ Thinking an empty object is falsy

```javascript
if ({}) {
    console.log("Runs");
}
```

Output

```text
Runs
```

Objects are truthy.

---

## ❌ Confusing truthy with true

```javascript
"Hello"
```

is truthy.

It is **not**

```javascript
true
```

---

# 💼 Interview Questions

### What are Truthy values?

Values that become `true` when converted to a boolean.

---

### How many falsy values exist in JavaScript?

There are **8 falsy values**:

- false
- 0
- -0
- 0n
- ""
- null
- undefined
- NaN

---

### Is an empty array truthy?

Yes.

---

### Is an empty object truthy?

Yes.

---

### What is the difference between truthy and true?

A truthy value behaves like `true` in boolean contexts, but it is not actually equal to the boolean value `true`.

---

# 📝 Revision Sheet

- JavaScript converts values to booleans when needed.
- There are only **8 falsy values**.
- Everything else is truthy.
- Empty arrays are truthy.
- Empty objects are truthy.
- Truthy does not mean equal to `true`.

---

# 🧪 Practice Questions

1. What are truthy values?
2. What are falsy values?
3. Name all eight falsy values.
4. Is `[]` truthy or falsy?
5. Is `{}` truthy or falsy?
6. What is the difference between truthy and `true`?

---

# 💻 Mini Exercise

Predict the output.

```javascript
console.log(Boolean(0));

console.log(Boolean(""));

console.log(Boolean([]));

console.log(Boolean({}));

console.log(Boolean("JavaScript"));

console.log(Boolean(null));

console.log(Boolean(undefined));

console.log(Boolean(NaN));
```

### Expected Output

```text
false
false
true
true
true
false
false
false
```

---

# 📌 Key Takeaways

- JavaScript automatically converts values to booleans when needed.
- There are only **8 falsy values**.
- Everything else is truthy.
- Empty arrays and objects are truthy.
- Truthy values are **not** the same as the boolean value `true`.

---

⬅️ Previous: `02-Type-Coercion.md`

➡️ Next: `04-Control-Flow/01-if-else.md`