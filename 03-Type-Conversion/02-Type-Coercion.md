# Type Coercion in JavaScript

> 📚 Chapter 2 of Type Conversion & Type Coercion

---

# 📑 Table of Contents

- What is Type Coercion?
- Why Do We Need It?
- Type Conversion vs Type Coercion
- String Coercion
- Number Coercion
- Boolean Coercion
- Equality Coercion
- Weird JavaScript Examples
- Common Beginner Mistakes
- Interview Questions
- Revision Sheet
- Practice Questions
- Key Takeaways

---

# 📖 What is Type Coercion?

**Type Coercion** is the automatic conversion of one data type into another by JavaScript.

Unlike Type Conversion, **you don't do it manually**.

JavaScript decides when conversion is needed.

Example

```javascript
console.log("5" + 2);
```

Output

```text
52
```

JavaScript automatically converts:

```text
2

↓

"2"
```

Result

```text
"52"
```

This automatic conversion is called **Type Coercion**.

---

# 🤔 Why Do We Need Type Coercion?

Imagine writing

```javascript
let score = "100";

console.log(score + 20);
```

JavaScript notices that one value is a string.

So it converts the number into a string.

```text
"100"

+

20

↓

"100"

+

"20"

↓

"10020"
```

---

# 🌍 Real-Life Analogy

Imagine two people speaking different languages.

```text
English + Kannada
```

To communicate,

one person changes their language.

Similarly,

JavaScript changes the data type automatically so both values can work together.

---

# 🆚 Type Conversion vs Type Coercion

| Type Conversion | Type Coercion |
|-----------------|---------------|
| Done manually | Done automatically |
| Programmer decides | JavaScript decides |
| Uses Number(), String(), Boolean() | Happens during operations |

Example

```javascript
Number("10");
```

Conversion.

---

```javascript
"10" + 5;
```

Coercion.

---

# ➕ String Coercion

Whenever the **+ operator** sees a string,

it usually converts the other value into a string.

Example

```javascript
console.log("5" + 2);
```

Output

```text
52
```

---

```javascript
console.log("Hello " + "World");
```

Output

```text
Hello World
```

---

```javascript
console.log("Age : " + 20);
```

Output

```text
Age : 20
```

---

# ➖ Number Coercion

The operators

```text
-

*

/

%

**
```

expect numbers.

So JavaScript converts strings into numbers.

Example

```javascript
console.log("10" - 5);
```

Output

```text
5
```

---

```javascript
console.log("6" * 3);
```

Output

```text
18
```

---

```javascript
console.log("20" / 4);
```

Output

```text
5
```

---

```javascript
console.log("10" % 3);
```

Output

```text
1
```

---

# ✅ Boolean Coercion

Booleans become numbers during arithmetic.

```text
true → 1

false → 0
```

Example

```javascript
console.log(true + true);
```

Output

```text
2
```

---

```javascript
console.log(true + 5);
```

Output

```text
6
```

---

```javascript
console.log(false + 5);
```

Output

```text
5
```

---

# ⚖️ Equality Coercion

The loose equality operator

```javascript
==
```

allows coercion.

Example

```javascript
console.log(5 == "5");
```

Output

```text
true
```

Because JavaScript converts

```text
"5"

↓

5
```

---

Strict equality

```javascript
===
```

does **not** perform type coercion.

```javascript
console.log(5 === "5");
```

Output

```text
false
```

---

# 🤯 Weird JavaScript Examples

## Example 1

```javascript
console.log("5" + 2);
```

Output

```text
52
```

---

## Example 2

```javascript
console.log("5" - 2);
```

Output

```text
3
```

---

## Example 3

```javascript
console.log("5" * "2");
```

Output

```text
10
```

---

## Example 4

```javascript
console.log(true + true);
```

Output

```text
2
```

---

## Example 5

```javascript
console.log(false + 10);
```

Output

```text
10
```

---

## Example 6

```javascript
console.log(null + 1);
```

Output

```text
1
```

Because

```text
null

↓

0
```

---

## Example 7

```javascript
console.log(undefined + 1);
```

Output

```text
NaN
```

---

## Example 8

```javascript
console.log([] + []);
```

Output

```text
""
```

Both arrays become empty strings.

---

## Example 9

```javascript
console.log([] + {});
```

Output

```text
"[object Object]"
```

---

## Example 10

```javascript
console.log([] == 0);
```

Output

```text
true
```

JavaScript performs several coercion steps internally.

This is one reason why `==` can be confusing.

---

# 📊 Summary Table

| Expression | Result |
|------------|--------|
| `"5" + 2` | `"52"` |
| `"5" - 2` | `3` |
| `"5" * 2` | `10` |
| `"20" / 4` | `5` |
| `true + true` | `2` |
| `false + 5` | `5` |
| `null + 1` | `1` |
| `undefined + 1` | `NaN` |
| `5 == "5"` | `true` |
| `5 === "5"` | `false` |

---

# ⚠️ Common Beginner Mistakes

## ❌ Using `==`

```javascript
5 == "5";
```

Works because of coercion.

Prefer

```javascript
5 === "5";
```

---

## ❌ Thinking + always adds numbers

Wrong.

If one operand is a string,

`+` performs string concatenation.

---

## ❌ Forgetting form inputs are strings

```javascript
let age = "20";

console.log(age + 5);
```

Output

```text
205
```

Convert it first if you need arithmetic.

---

# 💼 Interview Questions

### What is Type Coercion?

Automatic conversion of one data type into another by JavaScript.

---

### Difference between Type Conversion and Type Coercion?

Conversion is manual.

Coercion is automatic.

---

### Why does `"5" + 2` return `"52"`?

Because JavaScript converts the number into a string.

---

### Why does `"5" - 2` return `3`?

Because the `-` operator expects numbers.

---

### Why should we prefer `===`?

Because it compares both value and data type without coercion.

---

# 📝 Revision Sheet

- Type Coercion is automatic.
- `+` often performs string concatenation.
- `-`, `*`, `/`, `%` convert values into numbers.
- `true` becomes `1`.
- `false` becomes `0`.
- Prefer `===` over `==`.

---

# 🧪 Practice Questions

1. What is Type Coercion?
2. Difference between Conversion and Coercion.
3. Why does `"5" + 2` return `"52"`?
4. Why does `"5" - 2` return `3`?
5. What is the difference between `==` and `===`?
6. Why does `true + true` return `2`?

---

# 💻 Mini Exercise

Predict the output.

```javascript
console.log("10" + 5);

console.log("10" - 5);

console.log(true + 1);

console.log(false + 5);

console.log(null + 5);

console.log(undefined + 5);

console.log(5 == "5");

console.log(5 === "5");
```

### Expected Output

```text
105
5
2
5
5
NaN
true
false
```

---

# 📌 Key Takeaways

- Type Coercion is automatic.
- `+` concatenates if one operand is a string.
- Arithmetic operators convert values to numbers.
- `true` becomes `1`.
- `false` becomes `0`.
- Prefer `===` to avoid unexpected coercion.

---

⬅️ Previous: `01-Type-Conversion.md`

➡️ Next: `03-Truthy-and-Falsy.md`