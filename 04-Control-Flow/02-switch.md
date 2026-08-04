# switch Statement

> 📚 Chapter 2 of Control Flow

---

## 📖 Imagine This...

You're building a food ordering app.

The user chooses:

- Pizza
- Burger
- Pasta
- Sandwich

Depending on the choice, you display a different price.

You could write multiple `if...else` statements...

But when there are many fixed choices, `switch` makes the code much cleaner.

---

# 🤔 What is switch?

A `switch` statement is another way of making decisions.

Instead of checking many `else if` conditions, JavaScript compares **one value** against multiple possible cases.

Think of it like a menu.

```text
Choose a drink

1 → Coffee ☕

2 → Tea 🍵

3 → Juice 🧃

4 → Water 💧
```

JavaScript checks the selected option and runs the matching block.

---

# 🧠 Syntax

```javascript
switch (value) {

    case option1:
        // code
        break;

    case option2:
        // code
        break;

    default:
        // code

}
```

---

# 💻 Example 1

```javascript
let day = 2;

switch (day) {

    case 1:
        console.log("Monday");
        break;

    case 2:
        console.log("Tuesday");
        break;

    case 3:
        console.log("Wednesday");
        break;

    default:
        console.log("Invalid Day");

}
```

### Output

```text
Tuesday
```

---

# 💻 Example 2

```javascript
let fruit = "Apple";

switch (fruit) {

    case "Apple":
        console.log("₹120/kg");
        break;

    case "Mango":
        console.log("₹150/kg");
        break;

    default:
        console.log("Fruit not available");

}
```

### Output

```text
₹120/kg
```

---

# 📌 What does `break` do?

`break` tells JavaScript:

> "Stop here and come out of the switch."

Without it,

JavaScript keeps executing the next cases.

Example

```javascript
let day = 1;

switch (day) {

    case 1:
        console.log("Monday");

    case 2:
        console.log("Tuesday");

    case 3:
        console.log("Wednesday");

}
```

### Output

```text
Monday
Tuesday
Wednesday
```

This is called **Fall Through**.

---

Now with `break`:

```javascript
switch (day) {

    case 1:
        console.log("Monday");
        break;

    case 2:
        console.log("Tuesday");
        break;

    case 3:
        console.log("Wednesday");
        break;

}
```

### Output

```text
Monday
```

---

# 📌 What is `default`?

`default` works like the final `else`.

It runs when none of the cases match.

```javascript
let month = 15;

switch (month) {

    case 1:
        console.log("January");
        break;

    case 2:
        console.log("February");
        break;

    default:
        console.log("Invalid Month");

}
```

### Output

```text
Invalid Month
```

---

# 💻 Multiple Cases

Sometimes multiple options should execute the same code.

Example

```javascript
let day = "Saturday";

switch (day) {

    case "Saturday":
    case "Sunday":
        console.log("Weekend");
        break;

    default:
        console.log("Weekday");

}
```

### Output

```text
Weekend
```

---

# 🌍 Real-Life Examples

### ATM Language Selection

```text
1 → English

2 → Hindi

3 → Kannada

4 → Telugu
```

---

### Traffic Signal

```javascript
let signal = "Red";

switch (signal) {

    case "Red":
        console.log("Stop");
        break;

    case "Yellow":
        console.log("Get Ready");
        break;

    case "Green":
        console.log("Go");
        break;

}
```

---

# 🤔 When should I use switch?

✅ Use `switch` when:

- Comparing **one variable**
- Against **many fixed values**

Example

```javascript
switch (role)
```

---

❌ Don't use `switch` for conditions like:

```javascript
if (age > 18)
```

`switch` is not designed for range comparisons.

---

# ⚠️ Common Beginner Mistakes

## ❌ Forgetting `break`

Without `break`, JavaScript continues into the next case.

This is the most common mistake.

---

## ❌ Using Conditions Inside `case`

Wrong

```javascript
case age > 18:
```

`case` compares values, not conditions.

Use `if...else` instead.

---

## ❌ Forgetting `default`

Always add a `default` case.

It handles unexpected values gracefully.

---

# 💼 Interview Questions

### When should we use `switch` instead of `if...else`?

Use `switch` when comparing one value against many fixed options.

---

### What happens if `break` is omitted?

JavaScript continues executing the following cases (fall through).

---

### What is the purpose of `default`?

It runs when no case matches.

---

# 📝 Quick Revision

✅ `switch` compares one value with multiple cases.

✅ `break` stops execution.

✅ `default` runs if no case matches.

✅ Multiple cases can share the same block.

✅ Use `switch` for fixed values, not ranges.

---

# 💻 Mini Exercise

Predict the output.

```javascript
let color = "Blue";

switch (color) {

    case "Red":
        console.log("Stop");
        break;

    case "Blue":
        console.log("Ocean");
        break;

    default:
        console.log("Unknown");

}
```

---

Predict the output.

```javascript
let num = 1;

switch (num) {

    case 1:
        console.log("One");

    case 2:
        console.log("Two");

    default:
        console.log("Done");

}
```

(Hint: There is no `break`.)

---

# 📌 Key Takeaways

- `switch` is an alternative to multiple `else if` statements.
- It compares one value against multiple cases.
- Always use `break` unless you intentionally want fall through.
- `default` acts like the final `else`.
- Use `switch` only when comparing fixed values.

---

⬅️ Previous: `01-if-else.md`

➡️ Next: `03-for-loop.md`