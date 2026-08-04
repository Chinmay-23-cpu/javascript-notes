# Parameters and Arguments

> 📚 Chapter 2 of Functions

---

## 📖 Imagine This...

Suppose you own a coffee shop.

A customer orders:

> "One Cappuccino."

The next customer says:

> "One Latte."

The coffee machine is the same.

Only the **input** changes.

Functions work in exactly the same way.

Instead of creating a new function for every situation, we pass different values to the same function.

---

# 🤔 What are Parameters?

A **parameter** is a variable that receives a value when the function is called.

Think of it as a placeholder.

```javascript
function greet(name) {
    console.log("Hello " + name);
}
```

Here,

```javascript
name
```

is a **parameter**.

---

# 🤔 What are Arguments?

An **argument** is the actual value passed to the function.

```javascript
greet("Chinmay");
```

Here,

```javascript
"Chinmay"
```

is the **argument**.

---

# 🧠 Parameter vs Argument

```javascript
function greet(name) {
    console.log("Hello " + name);
}

greet("Chinmay");
```

```text
name
│
├── Parameter

"Chinmay"
│
└── Argument
```

---

# 💻 Example 1

```javascript
function greet(name) {
    console.log("Hello " + name);
}

greet("Chinmay");
greet("Rahul");
greet("Ananya");
```

### Output

```text
Hello Chinmay
Hello Rahul
Hello Ananya
```

One function.

Different inputs.

---

# 💻 Example 2

```javascript
function add(a, b) {
    console.log(a + b);
}

add(5, 3);
```

### Output

```text
8
```

Here,

```text
Parameters

a
b
```

Arguments

```text
5
3
```

---

# 💻 Multiple Arguments

A function can have more than one parameter.

```javascript
function introduce(name, age) {

    console.log(name);

    console.log(age);

}

introduce("Chinmay", 20);
```

### Output

```text
Chinmay
20
```

---

# 💻 Missing Arguments

What happens if we forget to pass an argument?

```javascript
function greet(name) {

    console.log(name);

}

greet();
```

### Output

```text
undefined
```

Because no value was provided.

---

# 🌍 Real-Life Example

Think of ordering pizza.

```text
Pizza Machine

↓

Needs

Size

Toppings

Crust
```

You don't build a new machine every time.

You simply give it different inputs.

Functions work the same way.

---

# ⚠️ Common Beginner Mistakes

## ❌ Confusing Parameters and Arguments

Remember:

```text
Function Definition

↓

Parameter

Function Call

↓

Argument
```

---

## ❌ Passing Too Few Arguments

```javascript
function add(a, b) {

    console.log(a + b);

}

add(5);
```

Output

```text
NaN
```

Because

```text
b = undefined
```

---

## ❌ Thinking Parameter Names Matter

These are the same.

```javascript
function greet(name) {}
```

```javascript
function greet(userName) {}
```

The name is your choice.

---

# 💼 Interview Questions

### What is a parameter?

A variable used in the function definition to receive values.

---

### What is an argument?

The actual value passed when calling the function.

---

### Can a function have multiple parameters?

Yes.

---

### What happens if an argument is missing?

The corresponding parameter becomes `undefined`.

---

# 📝 Quick Revision

✅ Parameters are placeholders.

✅ Arguments are actual values.

✅ A function can accept multiple parameters.

✅ Missing arguments become `undefined`.

---

# 💻 Mini Exercise

Predict the output.

```javascript
function multiply(a, b) {

    console.log(a * b);

}

multiply(4, 5);
```

---

Predict the output.

```javascript
function greet(name) {

    console.log("Hi " + name);

}

greet();
```

---

# 📌 Key Takeaways

- Parameters receive values.
- Arguments supply values.
- One function can work with many different inputs.
- Missing arguments become `undefined`.

---

⬅️ Previous: `01-Functions.md`

➡️ Next: `03-Return-Keyword.md`