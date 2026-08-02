# Operators in JavaScript

## 📖 What is an Operator?

An **operator** is a symbol that performs an operation on one or more values (called operands).

Example:

```javascript
let sum = 10 + 5;
```

Here,

```text
10      → Operand

+       → Operator

5       → Operand
```

The operator performs the addition and returns:

```text
15
```

---

# 🤔 Why Do We Need Operators?

Imagine writing a program to calculate marks.

```javascript
let maths = 90;
let science = 85;

let total = maths + science;
```

Without operators, calculations and comparisons would not be possible.

Operators allow us to:

- Perform calculations
- Compare values
- Assign values
- Combine conditions
- Make decisions

---

# 📚 Types of Operators

JavaScript provides many types of operators.

```text
Operators
│
├── Arithmetic
├── Assignment
├── Comparison
├── Logical
├── Unary
├── Ternary
├── Nullish Coalescing
└── Optional Chaining
```

---

# ➕ Arithmetic Operators

Arithmetic operators perform mathematical operations.

| Operator | Meaning |
|----------|---------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Modulus (Remainder) |
| ** | Exponentiation |

---

## Addition (+)

```javascript
let a = 10;
let b = 5;

console.log(a + b);
```

Output

```text
15
```

---

## Subtraction (-)

```javascript
console.log(10 - 3);
```

Output

```text
7
```

---

## Multiplication (*)

```javascript
console.log(6 * 4);
```

Output

```text
24
```

---

## Division (/)

```javascript
console.log(20 / 5);
```

Output

```text
4
```

---

## Modulus (%)

Returns the remainder after division.

```javascript
console.log(10 % 3);
```

Output

```text
1
```

Useful for checking even and odd numbers.

```javascript
let number = 12;

console.log(number % 2 === 0);
```

Output

```text
true
```

---

## Exponentiation (**)

Raises a number to a power.

```javascript
console.log(2 ** 3);
```

Output

```text
8
```

---

# 📝 Assignment Operators

Assignment operators assign values to variables.

| Operator | Example | Equivalent |
|----------|----------|-----------|
| = | x = 5 | Assign value |
| += | x += 2 | x = x + 2 |
| -= | x -= 2 | x = x - 2 |
| *= | x *= 2 | x = x * 2 |
| /= | x /= 2 | x = x / 2 |
| %= | x %= 2 | x = x % 2 |

Example

```javascript
let marks = 80;

marks += 10;

console.log(marks);
```

Output

```text
90
```

---

# ⚖️ Comparison Operators

Comparison operators compare two values and return a **boolean** (`true` or `false`).

| Operator | Meaning |
|----------|---------|
| == | Equal (loose equality) |
| === | Strict Equal |
| != | Not Equal |
| !== | Strict Not Equal |
| > | Greater Than |
| < | Less Than |
| >= | Greater Than or Equal |
| <= | Less Than or Equal |

---

## Loose Equality (==)

Compares values after type coercion.

```javascript
console.log(5 == "5");
```

Output

```text
true
```

---

## Strict Equality (===)

Compares both value **and** data type.

```javascript
console.log(5 === "5");
```

Output

```text
false
```

✅ Always prefer `===` unless you have a specific reason to use `==`.

---

## Not Equal (!=)

```javascript
console.log(10 != 20);
```

Output

```text
true
```

---

## Strict Not Equal (!==)

```javascript
console.log(10 !== "10");
```

Output

```text
true
```

---

# 🔗 Logical Operators

Logical operators combine multiple conditions.

| Operator | Meaning |
|----------|---------|
| && | AND |
| \|\| | OR |
| ! | NOT |

---

## AND (&&)

Returns `true` only if **both** conditions are true.

```javascript
let age = 20;
let hasLicense = true;

console.log(age >= 18 && hasLicense);
```

Output

```text
true
```

---

## OR (||)

Returns `true` if **at least one** condition is true.

```javascript
let weekend = false;
let holiday = true;

console.log(weekend || holiday);
```

Output

```text
true
```

---

## NOT (!)

Reverses a boolean value.

```javascript
console.log(!true);
```

Output

```text
false
```

---

# ➕ Unary Operators

Unary operators work on a single operand.

## Increment (++)

```javascript
let count = 5;

count++;

console.log(count);
```

Output

```text
6
```

---

## Decrement (--)

```javascript
let count = 5;

count--;

console.log(count);
```

Output

```text
4
```

---

# 🧠 Prefix vs Postfix

```javascript
let x = 5;

console.log(++x);
```

Output

```text
6
```

The value is increased **before** being used.

---

```javascript
let x = 5;

console.log(x++);
console.log(x);
```

Output

```text
5
6
```

The value is used first, then increased.

---

# ❓ Ternary Operator

The ternary operator is a short form of `if...else`.

Syntax

```javascript
condition ? valueIfTrue : valueIfFalse;
```

Example

```javascript
let age = 18;

let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

Output

```text
Adult
```

---

# ❓ Nullish Coalescing (??)

Returns the right-hand value only when the left-hand value is `null` or `undefined`.

```javascript
let username = null;

console.log(username ?? "Guest");
```

Output

```text
Guest
```

---

# ❓ Optional Chaining (?.)

Safely accesses nested properties.

```javascript
let student = {};

console.log(student.address?.city);
```

Output

```text
undefined
```

Without optional chaining, trying to access a missing nested property could throw an error.

---

# 📊 Operator Precedence

Some operators execute before others.

Example

```javascript
console.log(2 + 3 * 4);
```

Output

```text
14
```

Because multiplication happens before addition.

Use parentheses to make your intention clear.

```javascript
console.log((2 + 3) * 4);
```

Output

```text
20
```

---

# 🌍 Real-Life Examples

### Arithmetic

Calculating shopping bill.

```javascript
let total = 500 + 250;
```

---

### Comparison

Checking voting eligibility.

```javascript
let age = 20;

console.log(age >= 18);
```

---

### Logical

Checking login permission.

```javascript
let loggedIn = true;
let isAdmin = false;

console.log(loggedIn && isAdmin);
```

---

# ⚠️ Common Beginner Mistakes

## ❌ Using `==` instead of `===`

```javascript
5 == "5";
```

Returns

```text
true
```

Use

```javascript
5 === "5";
```

Result

```text
false
```

---

## ❌ Confusing `=` and `===`

```javascript
let x = 10;
```

Assigns a value.

```javascript
x === 10;
```

Checks equality.

---

## ❌ Forgetting Operator Precedence

```javascript
2 + 3 * 4;
```

Result

```text
14
```

Not

```text
20
```

---

# 💼 Interview Questions

### What is an operator?

A symbol that performs an operation on one or more operands.

---

### Difference between `==` and `===`?

- `==` compares values after type coercion.
- `===` compares both value and type.

---

### What is the modulus operator used for?

It returns the remainder after division and is commonly used to check even or odd numbers.

---

### Difference between prefix and postfix increment?

- `++x` increments first, then returns the value.
- `x++` returns the current value first, then increments.

---

### What does the ternary operator do?

It provides a shorter way to write simple `if...else` statements.

---

# 📝 Revision Sheet

- Operators perform operations on values.
- Prefer `===` over `==`.
- `&&` requires both conditions to be true.
- `||` requires at least one condition to be true.
- `!` reverses a boolean.
- `%` returns the remainder.
- `??` handles `null` and `undefined`.
- `?.` safely accesses nested properties.
- Parentheses improve readability and avoid precedence confusion.

---

# 🧪 Practice Questions

1. What is an operator?
2. Name the different types of operators in JavaScript.
3. Difference between `==` and `===`.
4. What is the modulus operator used for?
5. Explain prefix and postfix increment.
6. What is the ternary operator?
7. What is optional chaining?
8. What is nullish coalescing?
9. What is operator precedence?

---

# 💻 Mini Exercise

Predict the output before running the code.

```javascript
let a = 10;
let b = 3;

console.log(a + b);
console.log(a % b);
console.log(a > b);
console.log(a === "10");
console.log(a == "10");
console.log(++a);
console.log(b++);
console.log(b);
```

### Expected Output

```text
13
1
true
false
true
11
3
4
```

---

# 📌 Key Takeaways

- Operators allow JavaScript to perform calculations, comparisons, and logical operations.
- Use `===` for strict equality checks.
- Learn the difference between `++x` and `x++`.
- Use `??` to provide default values for `null` or `undefined`.
- Use `?.` to safely access nested properties.
- Understand operator precedence to avoid unexpected results.