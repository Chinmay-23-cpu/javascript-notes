# Return Keyword

> 📚 Chapter 3 of Functions

---

## 📖 Imagine This...

Suppose your friend asks,

> "What's 5 + 3?"

You calculate the answer.

Now what?

You have to **give the answer back**.

That's exactly what the `return` keyword does.

It sends a value back from a function.

---

# 🤔 Why do we need return?

Sometimes printing a value isn't enough.

```javascript
function add(a, b) {
    console.log(a + b);
}

add(5, 3);
```

Output

```text
8
```

The function prints the answer, but we **can't use it later**.

What if we want to store it?

```javascript
let result = add(5, 3);
```

This won't work as expected.

Instead, we use `return`.

---

# 🧠 Syntax

```javascript
function functionName() {
    return value;
}
```

---

# 💻 Example 1

```javascript
function add(a, b) {
    return a + b;
}

let result = add(5, 3);

console.log(result);
```

### Output

```text
8
```

The function returns `8`, which is stored in `result`.

---

# 💻 Example 2

```javascript
function square(num) {
    return num * num;
}

console.log(square(4));
```

### Output

```text
16
```

---

# 📌 return Ends the Function

Once JavaScript reaches `return`, the function stops immediately.

```javascript
function greet() {
    console.log("Hello");

    return;

    console.log("Welcome");
}

greet();
```

### Output

```text
Hello
```

The last `console.log()` never runs.

---

# 🌍 Real-Life Example

Imagine an ATM.

```text
Insert Card

↓

Enter PIN

↓

Withdraw Money

↓

Return Cash 💵

↓

Transaction Ends
```

Once the ATM gives you the cash, the transaction is over.

Similarly, once a function executes `return`, it ends.

---

# ⚠️ Common Mistakes

### ❌ Confusing `return` with `console.log()`

```javascript
function add(a, b) {
    console.log(a + b);
}
```

Prints the result.

---

```javascript
function add(a, b) {
    return a + b;
}
```

Returns the result so it can be used later.

---

### ❌ Writing Code After `return`

```javascript
function test() {
    return "Done";

    console.log("Hello");
}
```

The last line never executes.

---

# 📝 Quick Revision

- `return` sends a value back from a function.
- It immediately ends the function.
- Returned values can be stored in variables.
- `console.log()` prints a value.
- `return` gives a value back.

---

# 💻 Mini Exercise

Predict the output.

```javascript
function multiply(a, b) {
    return a * b;
}

let answer = multiply(4, 6);

console.log(answer);
```

---

# 📌 Key Takeaways

- Use `return` when a function needs to send back a value.
- A function stops executing after `return`.
- `return` is different from `console.log()`.
- Returned values can be reused anywhere in your program.

---

⬅️ Previous: `02-Parameters-and-Arguments.md`

➡️ Next: `04-Scope-and-Closures.md`